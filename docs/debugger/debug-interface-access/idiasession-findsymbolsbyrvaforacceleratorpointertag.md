---
title: IDiaSession::findSymbolsByRVAForAcceleratorPointerTag | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a073cc45-0c7b-417e-b5fc-a3b08beccdbc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5bcf399dcf80cb574b6018dde5ffa44e72a4c988
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839214"
---
# <a name="idiasessionfindsymbolsbyrvaforacceleratorpointertag"></a>IDiaSession::findSymbolsByRVAForAcceleratorPointerTag
이 메서드 해당 태그 값을 지정 합니다 지정된 된 상대 가상 주소에서 지정 된 부모 가속기 스텁 함수에 포함 된 기호의 열거형을 반환 합니다.

## <a name="syntax"></a>구문

```C++
HRESULT findSymbolsByRVAForAcceleratorPointerTag ( 
   IDiaSymbol*           parent,
   DWORD                 tagValue,
   DWORD                 rva,
   IDiaEnumSymbols**     ppResult
);
```

#### <a name="parameters"></a>매개 변수
 `parent`

[in] `IDiaSymbol` 검색할 Accelerator 스텁 함수에 해당 하는 합니다.

 `tagValue`

[in] 포인터 태그 값입니다.

 `rva`

[in] 상대 가상 주소입니다.

 `ppResult`

[out] 에 대 한 포인터는 `IDiaEnumSymbols` 결과 사용 하 여 초기화 된 인터페이스 포인터입니다.

## <a name="return-value"></a>반환 값
 성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.

## <a name="remarks"></a>설명
 경우에이 메서드를 호출는 `IDiaSymbol` Accelerator 스텁 함수에 해당 하는 인터페이스입니다.

## <a name="see-also"></a>참고 항목
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)