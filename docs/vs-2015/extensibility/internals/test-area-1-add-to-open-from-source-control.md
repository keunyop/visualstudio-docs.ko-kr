---
title: '테스트 영역 1: 소스 제어에서 열기에 추가 | Microsoft Docs'
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
- source control [Visual Studio SDK], adding and opening solutions
- source control plug-ins, adding and opening solutions
ms.assetid: 5b3b5b08-5e9b-41be-ac72-c63957faed22
caps.latest.revision: 21
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 06cf33af8d642e9bee5e72306620449458258d43
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47553717"
---
# <a name="test-area-1-add-toopen-from-source-control"></a>테스트 영역 1: 소스 제어에서 열기 / 추가
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [테스트 영역 1: 소스 제어에서 열기를 추가](https://docs.microsoft.com/visualstudio/extensibility/internals/test-area-1-add-to-open-from-source-control)합니다.  
  
이 소스 제어 플러그 인 테스트 영역에서는 소스 제어에서 프로젝트 또는 솔루션을 배치 하 고 소스 제어에서 검색 합니다.  
  
## <a name="command-menu-access"></a>명령 메뉴 액세스  
 다음 [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] 통합된 개발 환경 메뉴 경로 테스트 사례에서 사용 됩니다.  
  
-   에 대 한 [!INCLUDE[vsvss](../../includes/vsvss-md.md)]소스 제어에서 열기,: **파일**, **엽니다**를 **프로젝트**/**솔루션**; 확인 합니다 에서[!INCLUDE[vsvss](../../includes/vsvss-md.md)] 위치입니다.  
  
-   다른 원본 제어 플러그 인에 대 한 소스 제어에서 열기: **파일**를 **소스 제어**합니다 **소스 제어에서 열기**합니다.  
  
-   소스 제어에 추가 합니다. **파일**, **소스 제어**, **소스 제어 파일에 솔루션 추가**, **소스 제어**, **추가 소스 제어에 프로젝트를 선택한**합니다.  
  
-   바로 가기 메뉴 (프로젝트/솔루션) **소스 제어에 솔루션 추가**합니다.  
  
-   소스 제어에서 추가: **파일**를 **소스 제어**합니다 **소스 제어에서 프로젝트 추가**합니다.  
  
-   에 대 한 [!INCLUDE[vsvss](../../includes/vsvss-md.md)], 추가 원본의 제어도 제공 됩니다 **파일**, **추가**를 **기존 프로젝트**; 조회에 [!INCLUDE[vsvss](../../includes/vsvss-md.md)] 위치 합니다.  
  
    > [!NOTE]
    >  이 테스트에서는 로컬 파일을 로컬 IIS (웹 서버)의 경로 사용할 수 있습니다.  
  
## <a name="expected-behavior"></a>예상된 된 동작  
  
-   각 지원 되는 프로젝트 형식에 대 한 사용자 "추가" 및 "열 에서" 소스 제어에 있어야 합니다.  
  
-   해당 소스 제어에 프로젝트를 추가 하는 경우 \< *ProjectName*>.vspscc 파일 (프로젝트 힌트 파일)이 생성 됩니다. 제외 파일 목록 및 연결 정보를 포함합니다. 프로젝트에 특정 정보가 포함 되어 있으므로이 파일을 삭제 하지 마세요.  
  
-   솔루션을 해당 소스 제어에 추가 될 때 \< *SolutionName*>.vssscc (triple S) 파일이 만들어집니다. 텍스트 파일에는 연결 정보 및 프로젝트 힌트 파일에 유사한 제외 파일 목록에 포함 되어 있습니다. 이 파일은 임시적 이며 원본 제어 데이터베이스에만 존재 합니다.  
  
-   소스 제어에서 솔루션을 열면를 \< *SolutionName*>.vsscc double 개 파일이 소스 제어 데이터베이스에만 존재 하는 임시 파일에 로컬로 만들어집니다. 이 파일 솔루션 연결 폴더에서 솔루션 파일의 경로 포함합니다. 이 파일에는 임시 이며 로컬 복사본을 "소스 제어에서 열기" 작업이 완료 되 면 삭제 됩니다.  
  
-   프로젝트를 소스 제어에 추가한 후에 (체크 아웃, Get, 및 등)에 모든 원본 제어 작업을 수행할 수 있습니다.  
  
## <a name="test-cases"></a>테스트 사례  
 다음은 추가 대 한 특정 테스트 사례 간 테스트 영역 소스 제어에서에서 열기.  
  
### <a name="case-1a-add-solution-to-source-control"></a>1a 사례: 소스 제어에 솔루션 추가  
 이 테스트 사례는 소스 제어에 솔루션 추가에 중점을 둡니다.  
  
|작업|테스트 단계|확인 하려면 예상된 결과|  
|------------|----------------|--------------------------------|  
|클라이언트 프로젝트를 소스 제어를 포함 하는 솔루션 추가|1.  클라이언트 프로젝트를 만듭니다.<br />2.  소스 제어에 솔루션 추가 (**파일**를 **소스 제어**합니다 **소스 제어에 솔루션 추가**).|솔루션/프로젝트는 소스 제어에 추가 되었습니다.|  
|파일 시스템 또는 로컬 IIS 웹 프로젝트를 소스 제어를 포함 하는 솔루션 추가|1.  파일 시스템 또는 로컬 IIS 웹 프로젝트를 만듭니다 (찾아보기 단추를 사용 하 여 프로젝트의 위치를 가리키도록 웹 프로젝트의 유형을 만들어집니다 경로 결정).<br />2.  소스 제어에 솔루션 추가 (**파일**를 **소스 제어**합니다 **소스 제어에 솔루션 추가**).|솔루션/프로젝트는 소스 제어에 추가 되었습니다.|  
|원격 사이트 웹 프로젝트를 소스 제어를 포함 하는 솔루션 추가|1.  원격 사이트 웹 프로젝트를 만듭니다.<br />2.  소스 제어에 솔루션 추가 (**파일**를 **소스 제어**합니다 **소스 제어에 솔루션 추가**).<br />3.  클릭 **확인** FrontPage 액세스 경고 대화 상자에서.|솔루션은 소스 제어에 추가 되었습니다.<br /><br /> 원격 사이트 프로젝트를 소스 제어에 없습니다. (자체 IIS 서버에서 원격 사이트 프로젝트를 제어할 수 있어야 합니다.)|  
|단일 프로젝트 솔루션을 사용 하 여 소스 제어에 추가할 **소스 제어에 선택한 프로젝트 추가**합니다.|1.  단일 프로젝트 솔루션을 만듭니다.<br />2.  선택 항목으로 소스 제어에 솔루션만 추가 (**파일**를 **소스 제어**합니다 **소스 제어에 선택한 프로젝트 추가**). 이 단계에 성공 하면 다음 단계를 계속 합니다.<br />3.  추가 프로젝트를 소스 제어 선택 (**파일**, **소스 제어**합니다 **소스 제어에 선택한 프로젝트 추가**).<br />4.  클릭 **예** 동일한 위치에 프로젝트를 추가 합니다.<br />5.  클릭 **체크 아웃** 에 **편집 하기 위해 체크 아웃** 대화 상자.|`Result from Step 2:`<br /><br /> 프로젝트 및 프로젝트 내에서 모든 파일 체크 아웃 원본 제어 표시기 있고 도구 설명을 "하지: 소스 제어" 아래에 표시 됩니다.<br /><br /> `Result from Step 5:`<br /><br /> 프로젝트 및 솔루션 파일은 소스 제어에서 같은 폴더입니다.|  
|소스 제어에 솔루션 추가 취소|1.  단일 프로젝트 솔루션을 만듭니다.<br />2.  소스 제어에 프로젝트 및 솔루션을 추가 하려고 합니다. 이 단계에 성공 하면 다음 단계를 계속 합니다.<br />3.  소스 제어 시스템에서 취소 합니다.|`Result from Step 2:`<br /><br /> 집합 프로젝트 위치 원본 제어 대화 상자를 한 번만 표시 됩니다.<br /><br /> `Result from Step 3:`<br /><br /> 프로젝트 추가 취소 했습니다, 프로젝트/솔루션은 소스 제어에서 및 모든 추가 소스 제어 메뉴를 계속 사용할 수 있습니다.|  
  
### <a name="case-1b-open-solution-from-source-control"></a>1b 사례입니다. 소스 제어에서 솔루션 열기  
 이 테스트 사례는 소스 제어에서 솔루션 열기에 중점을 둡니다.  
  
|작업|테스트 단계|확인 하려면 예상된 결과|  
|------------|----------------|--------------------------------|  
|소스 제어에서 클라이언트 프로젝트에 포함 된 솔루션|1.  클라이언트 프로젝트를 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다.<br />3.  솔루션을 닫습니다.<br />4.  새 위치로 소스 제어에서 솔루션을 엽니다.|솔루션/프로젝트를 소스 제어에서 열.|  
|로컬 또는 소스 제어에서 IIS 웹 프로젝트에 포함 된 솔루션|1.  로컬 또는 IIS 웹 프로젝트를 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다.<br />3.  솔루션을 닫습니다.<br />4.  새 위치로 소스 제어에서 솔루션을 엽니다.|솔루션/프로젝트를 소스 제어에서 열.|  
|소스 제어에서 원격 사이트 웹 프로젝트가 포함 된 솔루션을 열으십시오|1.  원격 사이트 웹 프로젝트를 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다. 이 단계에 성공 하면 다음 단계를 계속 합니다.<br />3.  솔루션을 닫습니다.<br />4.  새 위치로 소스 제어에서 솔루션을 엽니다.|`Result from Step 2:`<br /><br /> 원격 사이트 웹 소스 제어에 있지 않습니다.<br /><br /> `Result from Step 4:`<br /><br /> 솔루션 소스 제어에서 열립니다.<br /><br /> 소스 제어 것만 원격 사이트 프로젝트를 로드 합니다.|  
  
### <a name="case-1c-add-solution-from-source-control"></a>사례 1 c: 소스 제어에서 솔루션을 추가 합니다.  
 이 테스트 사례는 소스 제어에서 솔루션을 추가에 중점을 둡니다.  
  
|작업|테스트 단계|확인 하려면 예상된 결과|  
|------------|----------------|--------------------------------|  
|빈 솔루션에 추가-단일 프로젝트 솔루션|1.  단일 프로젝트 솔루션을 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다.<br />3.  솔루션을 닫습니다.<br />4.  두 번째 빈 솔루션을 만듭니다.<br />5.  소스 제어에서 이전에 제어 솔루션 추가 (**파일**를 **소스 제어**를 **소스 제어에서 프로젝트 추가**).|추가 된 프로젝트에 나타납니다 **솔루션 탐색기** 및 체크 인 합니다.|  
|단일 프로젝트를 사용 하 여 솔루션에 추가-단일 프로젝트|1.  단일 프로젝트를 사용 하 여 솔루션을 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다.<br />3.  솔루션을 닫습니다.<br />4.  두 번째 빈 솔루션을 만듭니다.<br />5.  소스 제어에서 이전에 제어 솔루션 추가 (**파일**를 **소스 제어**를 **소스 제어에서 프로젝트 추가**).|추가 된 프로젝트에 나타납니다 **솔루션 탐색기** 및 체크 인 합니다.|  
|솔루션에 추가-솔루션을 선택 하 여 소스 제어에 추가 합니다.|1.  프로젝트와 솔루션을 만듭니다.<br />2.  선택 항목으로 소스 제어에 솔루션만을 추가 합니다. 이 단계에 성공 하면 다음 단계를 계속 합니다.<br />3.  솔루션을 닫습니다.<br />4.  새 솔루션을 만듭니다.<br />5.  소스 제어에서 이전에 제어 솔루션 추가 (**파일**를 **소스 제어**를 **소스 제어에서 프로젝트 추가**).|`Result from Step 2:`<br /><br /> 프로젝트를 소스 제어에 없습니다.<br /><br /> `Result from Step 5:`<br /><br /> 첫 번째 솔루션의 솔루션 항목 있으면 표시 되지 않습니다 있도록 소스 제어에서 다시 추가 될 수 없습니다. 있습니다.<br /><br /> 첫 번째 솔루션에서 프로젝트를 사용할 수 없는 상태로 나타납니다.|  
  
## <a name="see-also"></a>참고 항목  
 [소스 제어 플러그 인에 대한 테스트 가이드](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)
