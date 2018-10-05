---
title: 열거자 | Microsoft Docs
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
- source control plug-ins, enumerators
ms.assetid: a60030c5-e1d1-47e1-84bb-cbfe838ab479
caps.latest.revision: 20
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6dcbd3dea8ad932aec5890bc085873ce3d20a8f0
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47556448"
---
# <a name="enumerators"></a>열거자
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [열거자](https://docs.microsoft.com/visualstudio/extensibility/enumerators)합니다.  
  
이 섹션에서는 소스 제어 플러그 인에 대해 알아야 하는 원본 제어 플러그 인 API 데이터 형식 열거자를 나열 합니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [명령 코드](../extensibility/command-code-enumerator.md)  
 에 대 한 옵션을 열거 합니다 [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md) 하 고 [SccPopulateList](../extensibility/sccpopulatelist-function.md) 함수입니다.  
  
 [메시지](../extensibility/message-enumerator.md)  
 인쇄 콜백에 대 한 사용 플래그 열거 [LPTEXTOUTPROC](../extensibility/lptextoutproc.md)합니다.  
  
 [파일 상태 코드](../extensibility/file-status-code-enumerator.md)  
 소스 제어에서 파일의 상태를 지정 하는 명명 된 상수 값을 포함 합니다.  
  
 [디렉터리 상태 코드](../extensibility/directory-status-code-enumerator.md)  
 소스 제어에서 디렉터리의 상태를 지정 하는 명명 된 상수 값을 포함 합니다.  
  
## <a name="related-sections"></a>관련 단원  
 [소스 제어 플러그 인 만들기](../extensibility/internals/creating-a-source-control-plug-in.md)  
 소스 제어 플러그 인 SDK를 정의 하 고 포함 된 리소스에 설명 합니다.  
  
 [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)  
 지정 된 명령에 대 한 고급 옵션에 대 한 사용자를 묻습니다.  
  
 [SccPopulateList](../extensibility/sccpopulatelist-function.md)  
 현재 상태에 대 한 파일 목록을 검사합니다. 또한에서는 합니다 `pfnPopulate` 파일에 대 한 조건과 일치 하지 않는 경우 호출자에 게 알리도록 함수는 `nCommand`합니다.  
  
 [LPTEXTOUTPROC](../extensibility/lptextoutproc.md)  
 사용 되는 콜백 함수를 설명 [SccOpenProject](../extensibility/sccopenproject-function.md) IDE를 통해 플러그 인 소스 제어 메시지를 표시 합니다.  
  
 [소스 제어 플러그 인](../extensibility/source-control-plug-ins.md)  
 원본 제어 플러그 인 API에 있는 모든 요소의 전체 목록을 제공합니다.
