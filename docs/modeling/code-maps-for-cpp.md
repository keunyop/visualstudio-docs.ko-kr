---
title: 간의 종속성 확인 C++ 소스 파일과 헤더 파일
ms.date: 05/16/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3904ff08496257d18589e36e5878f49404bbdf7c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62422183"
---
# <a name="code-maps-for-c-projects"></a>에 대 한 코드 맵 C++ 프로젝트

C++ 프로젝트에 대해 보다 완전한 맵을 만들려면 해당 프로젝트에 대해 찾아보기 정보 컴파일러 옵션(**/FR**)을 설정합니다. 그렇지 않으면 메시지가 표시되고 이 옵션을 설정하라는 메시지가 나타납니다. **확인**을 선택하면 현재 맵에 대해서만 옵션이 설정됩니다. 이후 모든 맵에 대해 메시지를 숨기도록 선택할 수 있습니다.

Visual C++ 프로젝트가 포함된 솔루션을 열 때 IntelliSense 데이터베이스를 업데이트하는 데 시간이 걸릴 수 있습니다. 이 시간 동안 있습니다 못할 헤더에 대 한 코드 맵을 만드는 데 (*.h* 또는 `#include`) IntelliSense 데이터베이스가 업데이트를 완료할 때까지 파일입니다. Visual Studio 상태 표시줄에서 업데이트 진행률을 모니터링할 수 있습니다.

- 모든 소스 파일과 헤더 파일 솔루션 간 종속성을 보려면 선택 **아키텍처** > **포함 파일의 그래프 생성**합니다.

   ![네이티브 코드의 종속성 그래프](../modeling/media/dependencygraphgeneral_nativecode.png)

- 현재 열려 있는 파일과 관련 소스 파일 및 헤더 파일 간의 종속성을 확인하려면 소스 파일이나 헤더 파일을 열고 파일 내 임의의 위치에서 파일 바로 가기 메뉴를 연 다음 **포함 파일의 그래프 생성**을 선택합니다.

   ![.h 파일의 첫 번째 수준 종속성 그래프](../modeling/media/dependencygraph_native_firstlevel.png)

## <a name="troubleshoot-code-maps-for-c-and-c-code"></a>C에 대 한 코드 맵 문제 해결 및 C++ 코드

다음 항목은 C 및 C++ 코드에서 지원되지 않습니다.

- 기본 형식은 부모 계층 구조가 포함된 맵에 나타나지 않습니다.

- 대부분의 **표시** 메뉴 항목은 C 및 C++ 코드에 사용할 수 없습니다.

C에 대 한 코드 맵을 만들 때 이러한 문제가 발생할 수 있습니다 하 고 C++ 코드:

|**문제**|**가능한 원인**|**해결**|
|-|-|-|
|코드 맵을 생성하지 못했습니다.|솔루션에 프로젝트가 성공적으로 만들어지지 않습니다.|발생한 빌드 오류를 수정하고 맵을 재생성합니다.|
|코드 맵을 생성 하려고 할 때 visual Studio가 응답 하지 않는 합니다 **아키텍처** 메뉴.|프로그램 데이터베이스 파일(.pdb)이 손상될 수 있습니다.<br /><br /> .pdb 파일에는 형식, 메서드 및 소스 파일 정보와 같은 디버깅 정보가 저장됩니다.|솔루션을 다시 빌드한 다음 다시 시도합니다.|
|IntelliSense 검색 데이터베이스에 대한 특정 설정을 사용할 수 없습니다.|Visual Studio에서 특정 IntelliSense 설정을 사용할 수 있습니다 **옵션** 대화 상자.|설정을 사용할 수 있도록 설정합니다.<br /><br /> 참조 [옵션, 텍스트 편집기, C /C++고급](../ide/reference/options-text-editor-c-cpp-advanced.md)합니다.|
|**알 수 없는 메서드** 라는 메시지가 메서드 노드에 나타납니다.<br /><br /> 이 문제는 메서드의 이름을 확인할 수 없기 때문에 발생합니다.|이진 파일에 기본 재배치 테이블이 없을 수 있습니다.|링커에서 **/FIXED:NO** 옵션을 설정합니다.|
||프로그램 데이터베이스 파일(.pdb)이 빌드되지 않았을 수 있습니다.<br /><br /> .pdb 파일에는 형식, 메서드 및 소스 파일 정보와 같은 디버깅 정보가 저장됩니다.|링커에서 **/DEBUG** 옵션을 설정합니다.|
||.pdb 파일을 열 수 없거나 예상되는 위치에서 찾을 수 없습니다.|.pdb 파일이 예상되는 위치에 있는지 확인합니다.|
||디버그 정보가 .pdb 파일에서 제거되었습니다.|**/PDBSTRIPPED** 옵션이 링커에서 사용된 경우 전체 .pdb 파일을 대신 포함합니다.|
||호출자가 함수가 아니며 이진 파일의 썽크이거나 데이터 섹션의 포인터입니다.|호출자가 썽크이면 썽크를 방지하기 위해 `_declspec(dllimport)`를 사용해 봅니다.|

## <a name="see-also"></a>참고자료

- [코드 맵 사용 하 여 종속성 매핑](../modeling/map-dependencies-across-your-solutions.md)