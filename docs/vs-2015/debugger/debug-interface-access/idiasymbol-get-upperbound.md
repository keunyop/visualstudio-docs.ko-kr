---
title: IDiaSymbol::get_upperBound | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_upperBound method
ms.assetid: a77dcafa-ea3f-45da-826d-8f9b4489a03f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f965cddfa9d5d071bd08e4473cff49c82703d7ec
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63386899"
---
# <a name="idiasymbolgetupperbound"></a>IDiaSymbol::get_upperBound
FORTRAN 배열 차원의 상한을 나타내는 기호를 검색 합니다.

## <a name="syntax"></a>구문

```C++
HRESULT get_upperBound ( 
   IDiaSymbol** pRetVal
);
```

#### <a name="parameters"></a>매개 변수
 `pRetVal`

[out] 반환 된 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md) FORTRAN 배열 차원의 상한을 나타내는 개체입니다.

## <a name="return-value"></a>반환 값
 성공 하면 반환 `S_OK`이 고, 그렇지 않으면 반환 `S_FALSE` 또는 오류 코드입니다.

> [!NOTE]
> 반환 값이 `S_FALSE` 속성 기호를 사용할 수 없는 것을 의미 합니다.

## <a name="see-also"></a>참고 항목
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)