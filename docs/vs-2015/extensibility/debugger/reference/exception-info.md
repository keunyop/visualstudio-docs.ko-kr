---
title: EXCEPTION_INFO | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- EXCEPTION_INFO
helpviewer_keywords:
- EXCEPTION_INFO structure
ms.assetid: d046957a-b97d-420b-b46b-c67cbaef709e
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 152ddae9ad5c3c6b6119c146d428024bc2e26a95
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47551149"
---
# <a name="exceptioninfo"></a>EXCEPTION_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [EXCEPTION_INFO](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/exception-info)합니다.  
  
디버그 중인 프로그램에서 throw 된 런타임 오류 또는 예외를 설명 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp#  
typedef struct tagEXCEPTION_INFO {   
   IDebugProgram2* pProgram;  
   BSTR            bstrProgramName;  
   BSTR            bstrExceptionName;  
   DWORD           dwCode;  
   EXCEPTION_STATE dwState;  
   GUID            guidType;  
} EXCEPTION_INFO;  
```  
  
```csharp  
public struct EXCEPTION_INFO {   
   public IDebugProgram2 pProgram;  
   public string         bstrProgramName;  
   public string         bstrExceptionName;  
   public uint           dwCode;  
   public uint           dwState;  
   public Guid           guidType;  
};  
```  
  
## <a name="members"></a>멤버  
 pProgram  
 합니다 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) 예외가 발생 한 프로그램을 나타내는 개체입니다.  
  
 bstrProgramName  
 예외가 발생 한 프로그램의 이름입니다.  
  
 bstrExceptionName  
 예외의 이름입니다.  
  
 dwCode  
 예외 또는 런타임 오류에 대 한 id 코드입니다.  
  
 dwState  
 값을 [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md) 예외 상태를 정의 하는 열거형입니다.  
  
 guidType  
 GUID 언어 식별자를 `guidLang` 또는 `guidEng`합니다.  
  
## <a name="remarks"></a>설명  
 이 구조에 대 한 매개 변수로 전달 되는 [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md) 하며 [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md) 메서드. 이 구조에 전달 되는 [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) 채워야 하는 방법입니다.  
  
## <a name="requirements"></a>요구 사항  
 헤더: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>참고 항목  
 [구조체 및 공용 구조체](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)   
 [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md)   
 [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)
