---
title: IDiaSymbol::get_isPointerToMemberFunction | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
ms.assetid: aa9b5599-9602-41be-ab50-d84b90bee72f
caps.latest.revision: 6
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b666aa19e574702655178790b8aa0463a0d5c2d5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62836549"
---
# <a name="idiasymbolgetispointertomemberfunction"></a>IDiaSymbol::get_isPointerToMemberFunction
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

이 기호는 멤버 함수에 대 한 포인터 인지 여부를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
HRESULT get_isPointerToMemberFunction(   
   BOOL* pRetVal);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pRetVal`  
 [out] 에 대 한 포인터를 `BOOL` 이 기호는 멤버 함수에 대 한 포인터 인지 여부를 지정 하는 합니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`이 고, 그렇지 않으면 반환 `S_FALSE` 또는 오류 코드입니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
