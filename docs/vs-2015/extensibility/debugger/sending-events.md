---
title: 이벤트 전송 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], sending events
ms.assetid: 064231e7-59b5-4437-8240-a23c0a7ec2a9
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 98247b894d2db628d508713875ba0ea7d0642729
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "58983642"
---
# <a name="sending-events"></a>이벤트 보내기
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

디버거가 디버그 엔진 (DE) 사이의 통신 메커니즘은 DCOM을 기반으로 하는 이벤트 모델. 이벤트를 COM 개체로 보내고 각 이벤트에 다음을 지정 하는 매개 변수:  
  
- 이벤트를 호출 하는 DE 합니다.  
  
- 설명 내용입니다.  
  
- 프로세스, 프로그램 및 스레드 정보 이벤트가 발생의 컨텍스트를 식별 하는 합니다. 프로세스는 독일에서 전송 되는 이벤트에 대 한 전송 되지 않습니다.  
  
- 동기 또는 비동기 이벤트 인지 여부를 나타내는 이벤트 형식입니다.  
  
  모든 디버그 이벤트 메서드를 사용 하 여 보내집니다 [IDebugEventCallback2::Event](../../extensibility/debugger/reference/idebugeventcallback2-event.md)합니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [이벤트 원본](../../extensibility/debugger/event-sources-visual-studio-sdk.md)  
 이벤트의 두 원본에 설명 합니다: 디버그 엔진 (DE) 및 세션 디버그 관리자 (SDM).  
  
 [지원되는 이벤트 형식](../../extensibility/debugger/supported-event-types.md)  
 현재 지원 되는 이벤트 형식에 설명 합니다: 비동기 및 동기입니다.  
  
 [이벤트 설명](../../extensibility/debugger/event-descriptions.md)  
 이벤트 및 용도 대 한 이유를 정의합니다.  
  
## <a name="related-sections"></a>관련 단원  
 [사용자 지정 디버그 엔진 만들기](../../extensibility/debugger/creating-a-custom-debug-engine.md)  
 DE 디버깅 서비스를 제공 하도록 인터프리터 또는 운영 체제를 사용 하 여 작동 하는 방법을 설명 합니다.
