---
title: IDebugThread2::CanSetNextStatement | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugThread2::CanSetNextStatement
helpviewer_keywords:
- IDebugThread2::CanSetNextStatement
ms.assetid: 7014af80-ff4f-4790-a34b-0528918d1fa3
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 40cf5eba5cfb5a7e960ed8905141d4058d926d39
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47556831"
---
# <a name="idebugthread2cansetnextstatement"></a>IDebugThread2::CanSetNextStatement
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [IDebugThread2::CanSetNextStatement](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugthread2-cansetnextstatement)합니다.  
  
지정 된 스택 프레임에 현재 명령 포인터를 설정할 수 있는지 여부를 결정 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp#  
HRESULT CanSetNextStatement (   
   IDebugStackFrame2*  pStackFrame,  
   IDebugCodeContext2* pCodeContext  
);  
```  
  
```csharp  
int CanSetNextStatement (   
   IDebugStackFrame2  pStackFrame,  
   IDebugCodeContext2 pCodeContext  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pStackFrame`  
 사용 하도록 예약 됩니다. null 값으로 설정 합니다. Null 값 이면 현재 스택 프레임을 사용 합니다.  
  
 `pCodeContext`  
 [in] [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) 실행 될 코드 위치를 설명 하는 개체 및 컨텍스트.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.  
  
## <a name="remarks"></a>설명  
 이 메서드가 반환 하는 경우 `S_OK`를 호출 합니다 [SetNextStatement](../../../extensibility/debugger/reference/idebugthread2-setnextstatement.md) 실제로 다음 문 설정 하는 방법입니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [SetNextStatement](../../../extensibility/debugger/reference/idebugthread2-setnextstatement.md)
