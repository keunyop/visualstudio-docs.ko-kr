---
title: IDebugExpressionEvaluator2::PreloadModules | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugExpressionEvaluator2::PreloadModules
- PreloadModules
ms.assetid: bcf9b968-ee14-4a92-88ad-926268a44e03
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d6d7236f19032fa0767a050ac84afe4b4e1585f0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62540253"
---
# <a name="idebugexpressionevaluator2preloadmodules"></a>IDebugExpressionEvaluator2::PreloadModules
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

지정 된 기호 공급자로 지정 된 모듈을 미리 로드 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp#  
HRESULT PreloadModules (  
   IDebugSymbolProvider* pSym  
);  
```  
  
```csharp  
int PreloadModules (  
   IDebugSymbolProvider pSym  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pSym`  
 [in] 기호 공급자는 모듈을 미리 설치 됩니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.  
  
## <a name="remarks"></a>설명  
 이 선택적 메서드는 호스팅 프로세스 연결을 할 때 사용 됩니다. EE ' 준비 ' 연결의 일부로 기회를 제공 합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는이 메서드를 구현 하는 방법을 보여 줍니다는 **ExpressionEvaluatorPackage** 노출 하는 개체를 [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md) 인터페이스입니다.  
  
```cpp#  
STDMETHODIMP ExpressionEvaluatorPackage::PreloadModules  
(  
    IDebugSymbolProvider *pSym  
)  
{  
    HRESULT hr = NOERROR;  
    RuntimeMemberDescriptor  * prtMemberDesc;  
    RuntimeClassDescriptor *prtClassDesc;  
    CComPtr<IDebugClassField> pClassField;  
    IfFalseGo(pSym,E_INVALIDARG);  
  
    prtMemberDesc = &(g_rgRTLangMembers[StandardModuleAttributeCtor]);  
    prtClassDesc = &(g_rgRTLangClasses[prtMemberDesc->rtParent]);  
    pSym->GetClassTypeByName(prtClassDesc->wszClassName, nmCaseSensitive, &pClassField);  
  
    pClassField = NULL;  
    prtMemberDesc = &(g_rgRTLangMembers[LoadAssembly]);  
    prtClassDesc = &(g_rgRTLangClasses[prtMemberDesc->rtParent]);  
    pSym->GetClassTypeByName(prtClassDesc->wszClassName, nmCaseSensitive, &pClassField);  
  
Error:  
    return hr;  
}  
```  
  
## <a name="see-also"></a>참고 항목  
 [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md)
