---
title: IDebugSessionProviderEx:StartDebugSession | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugSessionProviderEx:StartDebugSession
apilocation:
- scrobj.dll
ms.assetid: 247337ca-476c-4aa7-8500-d84fd1d98176
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fb120a9acca91014d7b8213a3ed0bd1ab575e118
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62934693"
---
# <a name="idebugsessionproviderexstartdebugsession"></a>IDebugSessionProviderEx:StartDebugSession
지정된 된 응용 프로그램을 사용 하 여 디버그 세션을 시작합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp
HRESULT StartDebugSession(  
   IRemoteDebugApplication*  pda  
   BOOL  fQuery  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pda`  
 [in] 디버그 응용 프로그램을 지정합니다.  
  
 `fQuery`  
 [in] True 이면 쿼리를 나타냅니다.  
  
## <a name="return-value"></a>반환 값  
 이 메서드는 `HRESULT`를 반환합니다. 가능한 값에는 다음 표에 있는 값이 포함되지만, 이에 국한되는 것은 아닙니다.  
  
|값|설명|  
|-----------|-----------------|  
|`S_OK`|메서드가 성공했으며|  
  
## <a name="remarks"></a>설명  
 이 메서드는 지정된 된 응용 프로그램을 사용 하 여 디버그 세션을 시작합니다. 디버거를 호출 해야 `IRemoteDebugApplication::ConnectDebugger` 이 호출에서 반환 하기 전에 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDebugSessionProviderEx 인터페이스](../../winscript/reference/idebugsessionproviderex-interface.md)   
 [IRemoteDebugApplication::ConnectDebugger](../../winscript/reference/iremotedebugapplication-connectdebugger.md)