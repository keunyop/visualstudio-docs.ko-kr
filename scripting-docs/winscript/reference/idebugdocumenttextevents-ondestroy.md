---
title: IDebugDocumentTextEvents::onDestroy | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentTextEvents.onDestroy
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugDocumentTextEvents::onDestroy
ms.assetid: 1b7eb341-6bad-403f-9821-19112f8732f3
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 137329e48f6cb36e36f0196fa226303468eec88a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62946754"
---
# <a name="idebugdocumenttexteventsondestroy"></a>IDebugDocumentTextEvents::onDestroy
기본 문서 소멸 된 더 이상 유효 하지 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```cpp
HRESULT onDestroy();  
```  
  
#### <a name="parameters"></a>매개 변수  
 이 메서드는 매개 변수 없이 합니다.  
  
## <a name="return-value"></a>반환 값  
 이 메서드는 `HRESULT`를 반환합니다. 가능한 값에는 다음 표에 있는 값이 포함되지만, 이에 국한되는 것은 아닙니다.  
  
|값|설명|  
|-----------|-----------------|  
|`S_OK`|메서드가 성공했으며|  
  
## <a name="remarks"></a>설명  
 이 메서드는 기본 문서 소멸 된을 더 이상 유효 하지 나타냅니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDebugDocumentTextEvents 인터페이스](../../winscript/reference/idebugdocumenttextevents-interface.md)