---
title: IDiaStackWalkHelper::searchForReturnAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkHelper2::searchForReturnAddress method
ms.assetid: 904223b1-6e26-4980-b310-d0b222cdbbbd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 87518257d9cab91976f69dd03c9026b0800a0680
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62837903"
---
# <a name="idiastackwalkhelpersearchforreturnaddress"></a>IDiaStackWalkHelper::searchForReturnAddress
가장 가까운 함수 반환 주소를 지정한 스택 프레임을 검색합니다.

## <a name="syntax"></a>구문

```C++
HRESULT searchForReturnAddress( 
   IDiaFrameData*  frame,
   ULONGLONG*      returnAddress
);
```

#### <a name="parameters"></a>매개 변수
 `frame`

[in] [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md) 현재 스택 프레임을 나타내는 개체입니다.

 `returnAddress`

[out] 가장 가까운 함수 반환 주소를 반환합니다.

## <a name="return-value"></a>반환 값
 성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.

## <a name="see-also"></a>참고 항목
- [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)