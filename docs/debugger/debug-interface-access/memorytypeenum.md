---
title: MemoryTypeEnum | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MemoryTypeEnum enumeration
ms.assetid: 8778c047-edeb-4495-8f9f-3f8bbb297099
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 19776c8d4ef72149c575d6835e9265e9cdb33727
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62855121"
---
# <a name="memorytypeenum"></a>MemoryTypeEnum
메모리 액세스의 형식을 지정 합니다.

## <a name="syntax"></a>구문

```C++
enum MemoryTypeEnum {
    MemTypeCode,
    MemTypeData,
    MemTypeStack,
    MemTypeAny = -1
};
```

#### <a name="parameters"></a>매개 변수
`MemTypeCode` 액세스는 메모리 에서만 코드입니다.

`MemTypeData` 데이터 또는 스택 메모리 액세스 합니다.

`MemTypeStack` 만 스택 메모리를 액세스 합니다.

`MemTypeAny` 모든 종류의 메모리에 액세스합니다.

## <a name="remarks"></a>설명
이 열거형의 값에 전달 되는 [IDiaStackWalkHelper::readMemory](../../debugger/debug-interface-access/idiastackwalkhelper-readmemory.md) 다양 한 유형의 메모리에 대 한 액세스를 제한 하는 방법이 있습니다.

## <a name="requirements"></a>요구 사항
헤더: cvconst.h

## <a name="see-also"></a>참고 항목
- [열거형 및 구조체](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaStackWalkHelper::readMemory](../../debugger/debug-interface-access/idiastackwalkhelper-readmemory.md)
