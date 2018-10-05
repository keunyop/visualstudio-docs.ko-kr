---
title: IDebugProgram3::ExecuteOnThread | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IDebugProgram3::ExecuteOnThread
ms.assetid: 2f5211e3-7a3f-47bf-9595-dfc8b4895d0d
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8ad46418897f4cdd2521209dd6643362e81bfcb6
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47554482"
---
# <a name="idebugprogram3executeonthread"></a>IDebugProgram3::ExecuteOnThread
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [IDebugProgram3::ExecuteOnThread](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprogram3-executeonthread)합니다.  
  
디버거가 프로그램을 실행합니다. 스레드는 스레드를 사용자가 프로그램을 실행 하는 경우 보고 디버거 정보를 제공 해에 반환 됩니다.  
  
## <a name="syntax"></a>구문  
  
```cpp#  
HRESULT ExecuteOnThread(  
   [in] IDebugThread2* pThread)  
```  
  
```csharp  
int ExecuteOnThread(  
   IDebugThread2 pThread  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pThread`  
 [in] [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) 개체입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.  
  
## <a name="remarks"></a>설명  
 세 가지 다른 디버거 실행 중지 후 다시 시작할 수 있습니다.  
  
-   실행: 이전 단계를 취소 하 고 등 다음 중단점까지 실행 합니다.  
  
-   단계는 이전 단계를 취소 하 고 새 단계가 완료 될 때까지 실행 합니다.  
  
-   계속: 다시 실행 하 고 이전 단계를 활성 상태 유지 합니다.  
  
 스레드 전달할 `ExecuteOnThread` 취소 단계를 결정 하는 경우에 유용 합니다. 를 실행 스레드의 실행을 알 수 없는 경우 모든 단계를 취소 합니다. 스레드의 지식을 바탕으로 활성 스레드에서 단계를 취소 해야 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [실행](../../../extensibility/debugger/reference/idebugprogram2-execute.md)   
 [IDebugProgram3](../../../extensibility/debugger/reference/idebugprogram3.md)
