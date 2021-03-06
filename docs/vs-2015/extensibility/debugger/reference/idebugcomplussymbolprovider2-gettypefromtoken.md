---
title: IDebugComPlusSymbolProvider2::GetTypeFromToken | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugComPlusSymbolProvider2::GetTypeFromToken
- GetTypeFromToken
ms.assetid: 4452bc5d-0225-40e0-a467-c472a5c7c4ee
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1fa5e258390040fc70c0538c929a166984c3a7b0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62540581"
---
# <a name="idebugcomplussymbolprovider2gettypefromtoken"></a>IDebugComPlusSymbolProvider2::GetTypeFromToken
해당 토큰을 지정 하는 형식을 검색 합니다.

## <a name="syntax"></a>구문

```cpp
HRESULT GetTypeFromToken(
    ULONG32       appDomain,
    GUID          guidModule,
    DWORD         tdToken,
    IDebugField** ppField
);
```

```csharp
int GetTypeFromToken(
    uint            appDomain,
    Guid            guidModule,
    uint            tdToken,
    out IDebugField ppField
);
```

#### <a name="parameters"></a>매개 변수
`appDomain`

 [in] 응용 프로그램 도메인의 식별자입니다.

`guidModule`

 [in] 모듈의 고유 식별자입니다.

`tdToken`

 [in] 검색할 형식의 토큰입니다.

`ppField`

 [out] 나타내는 형식을 반환 합니다 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)합니다.

## <a name="return-value"></a>반환 값
성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.

## <a name="example"></a>예제
다음 예제에서는이 메서드를 구현 하는 방법을 보여 줍니다는 **CDebugSymbolProvider** 노출 하는 개체를 [IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md) 인터페이스입니다.

```cpp
HRESULT CDebugSymbolProvider::GetTypeFromToken(
    ULONG32 ulAppDomainID,
    GUID guidModule,
    DWORD tdToken,
    IDebugField **ppField)
{
    HRESULT hr = E_FAIL;

    METHOD_ENTRY( CDebugDynamicFieldSymbol::GetTypeFromToken );

    ASSERT(IsValidObjectPtr(this, CDebugSymbolProvider));
    ASSERT(IsValidWritePtr(ppField, IDebugField*));

    Module_ID idModule(ulAppDomainID, guidModule);

    IfFailGo( this->CreateClassType(idModule, tdToken, ppField) );

Error:

    METHOD_EXIT( CDebugDynamicFieldSymbol::GetTypeFromToken, hr );

    return hr;
}
```

## <a name="see-also"></a>참고 항목
- [IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md)
