---
title: IDebugProgramDestroyEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramDestroyEvent2
helpviewer_keywords:
- IDebugProgramDestroyEvent2
ms.assetid: ddf127ca-c4a5-4071-90ca-68faf2f57dbd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7c0f4e3f11ad10787e8627ba0250ff1480dfb994
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62917192"
---
# <a name="idebugprogramdestroyevent2"></a>IDebugProgramDestroyEvent2
이 인터페이스는 프로그램 실행이 완료 하는 경우 디버그 엔진 (DE)에서 세션 디버그 관리자 (SDM)에 전송 됩니다.

## <a name="syntax"></a>구문

```
IDebugProgramDestroyEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>구현자 참고 사항
 DE 또는 사용자 지정 포트 공급자 프로그램 종료 되었습니다 며 디버깅에 사용할 수 있는 더 이상 보고서에이 인터페이스를 구현 합니다. 합니다 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) 이 인터페이스와 동일한 개체에서 인터페이스를 구현 해야 합니다. SDM 사용 [QueryInterface](/cpp/atl/queryinterface) 액세스는 `IDebugEvent2` 인터페이스입니다.

## <a name="notes-for-callers"></a>호출자에 대 한 정보
 DE 또는 사용자 지정 포트 공급자 만들고이 이벤트 개체는 프로그램의 종료를 보고할를 보냅니다. DE를 사용 하 여이 이벤트를 전송 합니다 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) 디버깅 중인 프로그램에 연결할 때 SDM에서 제공 하는 콜백 함수. 사용자 지정 포트 공급자 사용 하 여이 이벤트를 전송 합니다 [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md) 인터페이스입니다.

## <a name="methods-in-vtable-order"></a>Vtable 순서의 메서드
 다음 표에서 메서드의 `IDebugProgramDestroyEvent2`합니다.

|메서드|설명|
|------------|-----------------|
|[GetExitCode](../../../extensibility/debugger/reference/idebugprogramdestroyevent2-getexitcode.md)|프로그램의 종료 코드를 가져옵니다.|

## <a name="requirements"></a>요구 사항
 헤더: msdbg.h

 네임스페이스: Microsoft.VisualStudio.Debugger.Interop

 어셈블리: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>참고 항목
- [Core 인터페이스](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)