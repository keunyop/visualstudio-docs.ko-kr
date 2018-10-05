---
title: 함수 뷰 - 샘플링 데이터 | Microsoft 문서
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- sampling profiling method,Functions View
- Functions view
ms.assetid: 029d5ebb-e551-46b0-b64e-2c553d9dbb8e
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3813c306c2240e7b9db0e8e3d5cbf5929cf0cf91
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47542017"
---
# <a name="functions-view---sampling-data"></a>함수 뷰 - 샘플링 데이터
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [함수 뷰-샘플링 데이터](https://docs.microsoft.com/visualstudio/profiling/functions-view-sampling-data)입니다.  
  
샘플링 프로필 방법의 함수 보고서 뷰는 프로파일링 생성 중에 샘플링된 함수를 나열합니다.  
  
> [!NOTE]
>  Windows 8 및 Windows Server 2012의 강화된 보안 기능을 위해 Visual Studio 프로파일러가 이러한 플랫폼에서 데이터를 수집하는 방법을 상당히 변경해야 했습니다. Windows 스토어 앱에는 새로운 수집 기술도 필요합니다. [Windows 8 및 Windows Server 2012 응용 프로그램의 성능 도구](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md)를 참조하세요.  
  
|열|설명|  
|------------|-----------------|  
|**프로세스 ID**|프로파일링 실행의 PID(프로세스 ID)입니다.|  
|**프로세스 이름**|프로세스의 이름입니다.|  
|**모듈 이름**|함수가 포함된 모듈의 이름입니다.|  
|**모듈 경로**|함수가 포함된 모듈의 경로입니다.|  
|**소스 파일**|이 함수의 정의가 포함된 소스 파일입니다.|  
|**함수 이름**|함수의 정규화된 이름입니다.|  
|**함수 줄 번호**|소스 파일에서 이 함수가 시작되는 줄 번호입니다.|  
|**함수 주소**|함수의 주소입니다.|  
|**포괄 샘플**|이 함수가 실행될 때 수집된 총 샘플 수(즉, 이 함수가 호출 스택에 있을 때 수집된 샘플 수)입니다. 이 수에는 해당 함수에 의해 호출된 함수를 실행할 때 수집된 샘플이 포함됩니다.|  
|**포괄 샘플 비율(%)**|프로파일링 실행 시, 이 함수의 포괄 샘플이었던 모든 샘플의 비율입니다.|  
|**전용 샘플**|이 함수 본문의 코드가 실행될 때(즉, 이 함수가 호출 스택의 맨 위에 있을 때) 수집된 총 샘플 수입니다. 해당 함수가 호출한 함수에서 수집된 샘플은 포함되지 않습니다.|  
|**전용 샘플 비율(%)**|프로파일링 실행 시, 이 함수의 전용 샘플이었던 모든 샘플의 비율입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [방법: 보고서 뷰 열 사용자 지정](../profiling/how-to-customize-report-view-columns.md)   
 [함수 뷰 - 계측](../profiling/functions-view-dotnet-memory-instrumentation-data.md)   
 [함수 뷰 - 샘플링](../profiling/functions-view-dotnet-memory-sampling-data.md)   
 [함수 뷰](../profiling/functions-view-instrumentation-data.md)


