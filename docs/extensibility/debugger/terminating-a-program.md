---
title: 프로그램 종료 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- programs, termination events
- debugging [Debugging SDK], terminating a program
ms.assetid: eedda0a3-5e05-44fe-841d-a2f4866ac72d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 729d37c36782cd1786124c94796f610931473f0c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62912751"
---
# <a name="terminating-a-program"></a>프로그램 종료
다음 섹션에서는 하나의 스레드를 사용 하 여 단일 프로그램 종료를 설명합니다.

## <a name="termination-process"></a>종료 프로세스

1. DE 보냅니다는 [IDebugThreadDestroyEvent2](../../extensibility/debugger/reference/idebugthreaddestroyevent2.md) 을 올바른 [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md)합니다.

2. DE 보냅니다는 [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) 을 올바른 [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md)합니다.

   IDE는 디자인 모드로 전환 됩니다. 디버그 엔진 또는 런타임 환경 호출 [IDebugPortNotify2::RemoveProgramNode](../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md) 포트에서 프로그램을 제거 하도록 합니다.

## <a name="see-also"></a>참고자료
- [디버거 이벤트 호출](../../extensibility/debugger/calling-debugger-events.md)