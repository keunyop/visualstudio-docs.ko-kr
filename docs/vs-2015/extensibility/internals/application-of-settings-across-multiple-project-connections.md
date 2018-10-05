---
title: 여러 프로젝트 연결 간 설정 적용 | Microsoft Docs
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
- source control plug-ins, application of settings
ms.assetid: 2116d3d0-c46c-4d0a-b482-08a178584f46
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: cc2be78900e7bef33be138dfc8ed9dc1531af7c8
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47542967"
---
# <a name="application-of-settings-across-multiple-project-connections"></a>여러 프로젝트 연결 간 설정 적용
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [응용 프로그램의 설정에서 여러 프로젝트 연결](https://docs.microsoft.com/visualstudio/extensibility/internals/application-of-settings-across-multiple-project-connections)합니다.  
  
소스 제어 플러그 인 원본 제어 플러그 인 API 1.2를 사용 하 여 빌드된 여러 프로젝트 또는 여러 연결 컨텍스트 간에 동일한 소스 제어 작업을 실행 하 일괄 처리 작업을 사용할 수입니다. 중복 제거, 프로젝트별 사용자 환경에서 대화 상자에 일괄 처리를 사용할 수 있습니다.  
  
 사용자는 원본 제어 플러그 인 API 1.1 (예를 들어 두 웹 프로젝트에서 다른 파일 공유 컴퓨터)를 사용 하 여 빌드된 둘 이상의 연결을 소스 제어 플러그 인에 속하는 여러 항목을 선택 하 고 체크 아웃, 사용자에 게 동일한 대화 상자 표시 반복적으로 합니다. 사용자가 클릭 하는 경우에 이런 합니다 **모든 항목에 적용** IDE에는 각 연결 컨텍스트에 대 한 상태로 다시 설정 하기 때문에 대화 상자에서 확인란 합니다.  
  
## <a name="new-capability-flag"></a>새 기능 플래그  
 `SccBeginBatch` 집합 함수는 `SCC_CAP_BATCH` 를 일괄 처리 작업이 진행에서 중임을 나타내는 플래그  
  
## <a name="new-functions"></a>새 함수  
 새 함수를 다음 일괄 처리 작업을 지원합니다.  
  
-   [SccBeginBatch](../../extensibility/sccbeginbatch-function.md)  
  
-   [SccEndBatch](../../extensibility/sccendbatch-function.md)  
  
 `SCCBeginBatch` 함수 그룹의 원본 제어 작업을 시작 합니다. `SccEndBatch` 그룹을 닫습니다. 그룹을 중첩할 수 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [소스 제어 플러그 인 API 버전 1.2의 새로운 기능](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)
