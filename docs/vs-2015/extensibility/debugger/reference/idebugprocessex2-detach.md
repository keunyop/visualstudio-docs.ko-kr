---
title: IDebugProcessEx2::Detach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcessEx2::Detach
helpviewer_keywords:
- IDebugProcessEx2::Detach method
ms.assetid: 66d54c2c-9302-47c8-9975-f30ed988ab29
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b79f1f80f9b6849c37fc9b6c4c8669f1397f0227
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62538150"
---
# <a name="idebugprocessex2detach"></a>IDebugProcessEx2::Detach
이 메서드는 세션에서 프로세스를 디버깅 이상는 프로세스에 알립니다.

## <a name="syntax"></a>구문

```cpp
HRESULT Detach( 
   IDebugSession2* pSession
);
```

```csharp
int Detach(
   IDebugSession2 pSession
);
```

#### <a name="parameters"></a>매개 변수
 `pSession`

 [in] 이 프로세스에서 분리 하려면 세션을 고유 하 게 식별 하는 값입니다.

## <a name="return-value"></a>반환 값
 성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.

## <a name="remarks"></a>설명
 인터페이스에 전달 된 `pSession` 쿠키로 서만 처리할지,이 프로세스에 연결 하는 원래 세션 디버그 관리자를 고유 하 게 식별 하는 값은 제공 된 인터페이스의 메서드는 작동 합니다.

## <a name="see-also"></a>참고 항목
- [IDebugProcessEx2](../../../extensibility/debugger/reference/idebugprocessex2.md)