---
title: IDebugReference2::Compare | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReference2::Compare
helpviewer_keywords:
- IDebugReference2::Compare
ms.assetid: 3361c495-2673-4b7c-82e3-dee74e1fa58d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d3ca4e944125f6673ca66accdb78742f693def77
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62869128"
---
# <a name="idebugreference2compare"></a>IDebugReference2::Compare
다른 하나의 참조를 비교합니다. 나중에 사용하기 위해 예약되어 있습니다.

## <a name="syntax"></a>구문

```cpp
HRESULT Compare ( 
   REFERENCE_COMPARE dwCompare,
   IDebugReference2* pReference
);
```

```csharp
int Compare ( 
   enum_REFERENCE_COMPARE dwCompare,
   IDebugReference2       pReference
);
```

#### <a name="parameters"></a>매개 변수
 `dwCompare`

 [in] 값을 [REFERENCE_COMPARE](../../../extensibility/debugger/reference/reference-compare.md) 는 비교 연산을 수행 하려면 예를 들어, 보다 크거나 같음, 작음,를 지정 하는 열거형입니다.

 `pReference`

 [in] [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) 비교에 대 한 참조를 나타내는 개체입니다.

## <a name="return-value"></a>반환 값
 항상 `E_NOTIMPL`를 반환합니다.

## <a name="see-also"></a>참고 항목
- [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)
- [REFERENCE_COMPARE](../../../extensibility/debugger/reference/reference-compare.md)