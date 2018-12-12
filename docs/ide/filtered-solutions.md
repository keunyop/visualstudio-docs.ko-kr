---
title: 프로젝트 하위 집합 로드
ms.date: 12/04/2018
ms.topic: conceptual
ms.prod: visual-studio-dev16
ms.technology: vs-ide-general
helpviewer_keywords:
- filtered solution
- solution filtering
author: gewarren
ms.author: stsu
manager: douge
ms.openlocfilehash: 655644e936bdfb1382e70d746f589b8fcfabf488
ms.sourcegitcommit: ae46be4a2b2b63da7e7049e9ed67cd80897c8102
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52897222"
---
# <a name="filtered-solutions-in-visual-studio"></a>Visual Studio의 필터링된 솔루션

**Visual Studio 2019 Preview 1의 새로운 기능**

대규모 개발팀은 종종 여러 프로젝트가 포함된 하나의 대형 솔루션을 사용하여 공동 작업을 진행합니다. 그러나 개별 개발자는 일반적으로 이러한 프로젝트의 소규모 하위 집합에서 작업합니다. 대형 솔루션을 열 때 성능을 향상하기 위해 Visual Studio 2019 Preview 1에서는 *솔루션 필터링*이 도입되었습니다. 솔루션 필터링을 사용하면 선택한 프로젝트만 로드된 솔루션을 열 수 있습니다. 솔루션에서 프로젝트의 하위 집합을 로드하면 솔루션 로드, 빌드 및 테스트 실행 시간이 단축되고 검토에 집중할 수 있습니다.

다음과 같은 기능이 제공됩니다.

- 프로젝트를 로드하지 않고 솔루션을 열어 더 빠르게 코드로 이동할 수 있습니다. 솔루션이 열리면 로드할 프로젝트를 선택할 수 있습니다.

- 솔루션을 다시 열면 Visual Studio는 이전 세션에서 로드된 프로젝트를 기억하여 해당 프로젝트만 로드합니다.

- 하나 이상의 프로젝트 로드 구성을 저장하거나 팀 동료와 구성을 공유하는 솔루션 필터 파일을 만들 수 있습니다.

## <a name="open-a-filtered-solution"></a>필터링된 솔루션 열기

일부 프로젝트만 로드된 솔루션을 열려면 다음 단계를 따릅니다.

1. 메뉴 모음에서 **파일** > **열기** > **프로젝트/솔루션**을 선택합니다.

2. **새 프로젝트** 대화 상자에서 솔루션을 선택한 다음, **프로젝트를 로드하지 않음**을 선택합니다.

   ![[프로젝트를 로드하지 않음]이 선택된 Visual Studio 프로젝트 열기 대화 상자](media/filtered-solutions/do-not-load-projects.png)

3. **열기**를 선택합니다.

   일부 프로젝트가 언로드된 솔루션이 열립니다.

4. **솔루션 탐색기**에서 로드하려면 프로젝트를 선택(프로젝트를 둘 이상 선택하려면 **Ctrl** 키를 누른 상태로 클릭)한 다음, 프로젝트를 마우스 오른쪽 단추로 클릭하고 **프로젝트 다시 로드**를 선택합니다.

   ![Visual Studio 솔루션 탐색기에서 여러 프로젝트를 다시 로드](media/filtered-solutions/reload-project.png)

   Visual Studio는 다음에 로컬로 솔루션을 열 때 이전에 로드된 프로젝트를 기억합니다.

## <a name="toggle-unloaded-project-visibility"></a>언로드된 프로젝트 표시 설정/해제

**솔루션 탐색기**에서 다음 방법 중 하나를 사용하여 솔루션의 모든 프로젝트를 표시하도록 선택할 수도 있고 로드된 프로젝트만 표시하도록 선택할 수도 있습니다.

- 솔루션을 마우스 오른쪽 단추로 클릭하고 **언로드된 프로젝트 표시** 또는 **언로드된 프로젝트 숨기기**를 선택합니다.

- **모든 파일 표시** 단추를 선택하여 언로드된 프로젝트의 표시 유형을 전환합니다.

   ![Visual Studio 솔루션 탐색기의 [모든 파일 표시] 단추](media/filtered-solutions/show-all-files.PNG)

## <a name="solution-filter-files"></a>솔루션 필터 파일

프로젝트 로드 구성을 공유하거나 소스 제어에 커밋하려면 솔루션 필터 파일을 만들면 됩니다(*.slnf* 확장이 있음). 솔루션 필터 파일을 열면 지정된 프로젝트만 로드되고 언로드된 프로젝트는 모두 숨겨진 솔루션이 Visual Studio에서 열립니다. 언로드된 프로젝트를 표시하도록 [전환](#toggle-unloaded-project-visibility)할 수 있습니다.

솔루션 필터 파일은 **솔루션 탐색기**에서 솔루션 옆의 아이콘에 추가 깔때기형 문자 모양이 있기 때문에 일반 솔루션 파일과 시각적으로 구분됩니다. 필터 이름과 로드된 프로젝트 수도 솔루션 이름 옆에 표시됩니다.

![Visual Studio 솔루션 탐색기에서 열린 솔루션 필터 파일](media/filtered-solutions/solution-filter.PNG)

> [!NOTE]
> 솔루션 필터 파일을 만든 후 원래 솔루션에 새 프로젝트가 추가되면 **솔루션 탐색기**에서 언로드된 프로젝트로 표시됩니다.

### <a name="create-a-solution-filter-file"></a>솔루션 필터 파일 만들기

1. **솔루션 탐색기**에서 솔루션을 마우스 오른쪽 단추로 클릭하고 **솔루션 필터로 저장**을 선택합니다.

   ![Visual Studio 솔루션 탐색기의 [솔루션 필터로 저장] 메뉴](media/filtered-solutions/save-as-solution-filter.png)

2. 솔루션 필터 파일의 이름과 위치를 선택합니다.

만들어진 솔루션 필터 파일은 쉽게 액세스할 수 있도록 **최근에 사용한 프로젝트 및 솔루션** 목록에 추가됩니다.

![Visual Studio에서 최근에 사용한 항목 열기](media/filtered-solutions/open-recent.png)

## <a name="see-also"></a>참고 항목

- [솔루션 탐색기에서 파일 중첩 사용자 지정](file-nesting-solution-explorer.md)
- [Visual Studio 성능 최적화](optimize-visual-studio-performance.md)