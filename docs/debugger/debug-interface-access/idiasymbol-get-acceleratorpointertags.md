---
title: IDiaSymbol::get_acceleratorPointerTags | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
ms.assetid: 30e13cee-e511-49ec-affd-99b0097071b2
caps.latest.revision: 6
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c1724ee3e81ac00ed048f323105842361ec22bc7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62827296"
---
# <a name="idiasymbolgetacceleratorpointertags"></a>IDiaSymbol::get_acceleratorPointerTags
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

에 해당 하는 모든 가속기 포인터 태그 값을 반환 된 C++ AMP 액셀러레이터 스텁 함수입니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
HRESULT get_acceleratorPointerTags(   
   DWORD          cnt,  
   DWORD*         pcnt,  
   DWORD*         pPointerTags);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `cnt`  
 [in] 출력 배열의 크기 `pPointerTags`합니다.  
  
 `pcnt`  
 [out] Accelerator 포인터 태그의 수는 C++ AMP 액셀러레이터 스텁 함수입니다.  
  
 `pPointerTags`  
 [out] A `DWORD` accelerator 포인터 태그 값으로 채워진 배열 포인터를 C++ AMP 액셀러레이터 스텁 함수입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`이 고, 그렇지 않으면 반환 `S_FALSE` 또는 오류 코드입니다.  
  
## <a name="remarks"></a>설명  
 이 메서드가 호출 되는 `IDiaSymbol` 에 해당 하는 인터페이스를 C++ AMP 액셀러레이터 스텁 함수입니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
