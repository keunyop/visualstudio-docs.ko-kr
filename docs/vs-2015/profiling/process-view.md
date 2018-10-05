---
title: 프로세스 뷰 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.view.process
helpviewer_keywords:
- performance tools reports, process view
- Process view
- performance tools, process view
- Profiling Tools,process view
- Profiling Tools,process report
ms.assetid: 6d4e2a5d-9f17-4ece-a6f1-75836e1fc382
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b6d0c560cdd40651763837bba4e87372eba76007
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47551182"
---
# <a name="process-view"></a>프로세스 뷰
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [프로세스 뷰](https://docs.microsoft.com/visualstudio/profiling/process-view)합니다.  
  
프로세스 뷰에는 프로파일링 실행 중에 실행된 프로세스와 스레드에 대한 프로파일링 데이터가 표시됩니다.  
  
 프로세스는 이름별로 나열됩니다. 스레드는 스레드를 만든 프로세스의 자식 노드로 나열됩니다. 스레드는 스레드를 시작한 함수 또는 레이블 **[ntdll.dll]**(기호를 사용할 수 없는 경우)로 명명됩니다.  
  
 열을 추가 또는 제거하려면 뷰를 오른쪽 단추로 클릭한 다음 **열 추가/제거**를 선택합니다. 또한 열 이름을 클릭하여 데이터를 정렬할 수도 있습니다. 자세한 내용은 [방법: 보고서 뷰 열 사용자 지정](../profiling/how-to-customize-report-view-columns.md)을 참조하세요.  
  
 프로세스 뷰의 열은 샘플링 및 계측 방법을 사용하여 생성되는 데이터와 .NET 메모리 데이터를 포함하는 데이터에 대해 동일합니다. 다음 표에서는 열 값에 대해 설명합니다.  
  
|열|설명|  
|------------|-----------------|  
|**고유 ID**|프로파일러에서 생성한 프로세스 또는 스레드의 고유한 식별자입니다.|  
|**ID**|시스템에서 생성한 프로세스 또는 스레드의 식별자입니다.|  
|**이름**|프로세스 또는 스레드의 이름입니다.|  
|**시작 시간**|프로파일링 시작에서 프로세스 또는 스레드 시작까지의 시간(밀리초) 또는 프로세서 주기 수입니다.|  
|**종료 시간**|프로파일링 시작에서 프로세스 또는 스레드 끝까지의 시간(밀리초) 또는 프로세서 주기 수입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [샘플링 방법 데이터 뷰](../profiling/profiler-sampling-method-data-views.md)   
 [계측 방법 데이터 뷰](../profiling/instrumentation-method-data-views.md)   
 [.NET 메모리 데이터 뷰](../profiling/dotnet-memory-data-views.md)


