---
title: Visual Studio의 내게 필요한 옵션 팁과 요령
description: Visual Studio IDE(통합 개발 환경)가 장애인을 포함하여 모든 사용자에 대해 보다 쉽게 액세스할 수 있도록 도와주는 팁과 요령에 대해 자세히 알아봅니다.
ms.date: 02/21/2019
ms.topic: conceptual
helpviewer_keywords:
- accessibility [Visual Studio]
ms.assetid: 6b491d88-f79e-4686-8841-857624bdcfda
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e86791e77d5c8f6eb1e6b88ac663e1f11cc53e1e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62793352"
---
# <a name="accessibility-tips-and-tricks-for-visual-studio"></a>Visual Studio의 내게 필요한 옵션 팁과 요령

> [!TIP]
> 접근성 업데이트에 대한 자세한 내용은 [Visual Studio 2017 버전 15.3의 접근성 향상](https://devblogs.microsoft.com/visualstudio/accessibility-improvements-in-visual-studio-2017-version-15-3/) 블로그 게시물을 참조하세요.

Visual Studio에는 화면 판독기 및 기타 보조 기술과 호환되는 내게 필요한 옵션 기능이 있습니다. 이 항목에서는 키보드만 사용하여 작업을 수행하는 데 사용할 수 있는 일반적인 바로 가기 키 조합을 나열하고, 표시 여부를 개선하기 위해 고대비 테마를 사용하는 방법에 대한 정보를 포함합니다. 또한 주석을 사용하여 사용자 코드에 대한 유용한 정보를 노출하는 방법 및 빌드 및 중단점 이벤트에 대한 소리 큐를 설정하는 방법을 보여줍니다.

> [!NOTE]
> 이 토픽은 Windows의 Visual Studio에 적용됩니다. Mac용 Visual Studio는 [Mac용 Visual Studio의 접근성](/visualstudio/mac/accessibility)을 참조하세요.

## <a name="save-your-ide-settings"></a>IDE 설정 저장

 창 레이아웃, 키보드 매핑 구성표 및 기타 기본 설정을 저장하여 IDE 환경을 사용자 지정할 수 있습니다. 자세한 내용은 [Visual Studio IDE 개인 설정](../../ide/personalizing-the-visual-studio-ide.md)을 참조하세요.

## <a name="modify-your-ide-for-high-contrast-viewing"></a>고대비 보기를 위한 IDE 수정

일부 사용자의 경우 어떤 색을 보기 어렵습니다. 사용자 코드로 대비하지만 일반적인 "고대비" 테마를 사용하지 않으려는 경우 이제 "파랑(추가 대비)" 테마를 제공합니다.

  ![파랑 테마 및 파랑 추가 대비 테마 비교](media/blue-extra-contrast-theme.png)

## <a name="use-annotations-to-reveal-useful-information-about-your-code"></a>주석을 사용하여 코드에 대한 유용한 정보 노출

Visual Studio 편집기에는 스크루드라이버와 전구 아이콘, 오류 및 경고 "물결선", 책갈피 등과 같은 코드 줄에서 특정 시점에 특성 및 기능에 대해 알려주는 여러 텍스트 "도구 영역"이 포함되어 있습니다. "줄 주석 표시" 명령을 사용하여 이러한 도구 영역 간을 검색한 다음, 탐색할 수 있도록 설정할 수 있습니다.

  ![줄 주석 표시 명령 집합 사용](media/show-line-annotations-command-set.png)

## <a name="access-toolbars-by-using-shortcut-key-combinations"></a>바로 가기 키 조합을 사용하여 도구 모음 액세스

Visual Studio IDE에는 대부분의 도구 창에 있는 것과 같은 도구 모음이 있습니다. 다음 바로 가기 키 조합을 사용하여 도구 모음에 액세스할 수 있습니다.

|기능|설명|키 조합|
|-------------|-----------------| - |
|IDE 도구 모음|표준 도구 모음에서 첫 번째 단추를 선택합니다.|**Alt**, **Ctrl** + **Tab**|
|도구 창 도구 모음|포커스를 도구 창의 도구 모음으로 이동합니다. <br> <br> **참고:** 이 기능은 대부분의 도구 창에서 작동하지만 포커스가 도구 창에 있을 때만 작동합니다. 또한 Alt 키 전에 Shift 키를 선택해야 합니다. 팀 탐색기와 같은 일부 도구 창에서는 Alt 키를 선택하기 전에 잠시 Shift 키를 누르고 있어야 합니다.|**Shift** + **Alt**|
|도구 모음|다음 도구 모음의 첫 번째 항목으로 이동합니다(포커스가 도구 모음에 있을 때).|**Ctrl** + **Tab**|

### <a name="other-useful-shortcut-key-combinations"></a>기타 유용한 바로 가기 키 조합

일부 기타 유용한 바로 가기 키 조합은 다음과 같습니다.

|기능|설명|키 조합|
|-------------|-----------------| - |
|IDE|고대비를 켜고 끕니다. <br> <br> **참고:** 표준 Windows 바로 가기|**왼쪽 Alt+왼쪽 Shift+PrtScn**|
|대화 상자|대화 상자에서 확인란 옵션을 선택 또는 선택 취소합니다. <br> <br> **참고:** 표준 Windows 바로 가기|**스페이스바**|
|상황에 맞는 메뉴|상황에 맞는(마우스 오른쪽 단추 클릭) 메뉴를 엽니다. <br> <br> **참고:** 표준 Windows 바로 가기|**Shift** + **F10**|
|메뉴|액셀러레이터 키를 사용하여 메뉴 항목에 빠르게 액세스합니다. **Alt** 키를 선택한 다음, 메뉴에서 밑줄이 표시된 문자를 선택하여 명령을 활성화합니다. 예를 들어 Visual Studio에서 [프로젝트 열기] 대화 상자를 보려면 **Alt** + **F** + **O** + **P**를 선택합니다.  <br><br> **참고:** 표준 Windows 바로 가기|**Alt** + **[문자]**|
|검색 상자|Visual Studio의 검색 기능을 사용합니다.|**Ctrl** + **Q**|
|도구 상자 창|도구 상자 탭 간에 이동합니다.|**Ctrl** + **위쪽 화살표**<br /><br /> 를 갖는<br /><br /> **Ctrl** + **아래쪽 화살표**|
|도구 상자 창|폼 또는 디자이너에 도구 상자의 컨트롤을 추가합니다.|**Enter**|
|옵션 대화 상자: 환경 > 키보드|**바로 가기 키 누르기** 옵션에 입력된 키 조합을 삭제합니다.|**백스페이스**|

> [!NOTE]
> 표시되는 대화 상자와 메뉴 명령은 활성 설정이나 버전에 따라 도움말에서 설명하는 것과 다를 수 있습니다.

## <a name="use-the-sound-applet-to-set-build-and-breakpoint-cues"></a>소리 애플릿을 사용하여 빌드 및 중단점 큐 설정

Windows에서 소리 애플릿을 사용하여 Visual Studio 프로그램 이벤트에 소리를 할당할 수 있습니다. 특히 다음 프로그램 이벤트에 소리를 할당할 수 있습니다.

* 중단점 적중
* 빌드 취소
* 빌드 실패
* 빌드 성공

방법은 다음과 같습니다.

1. Windows 10을 실행하는 컴퓨터의 **검색** 상자에서 **시스템 소리 변경**을 입력합니다.

   ![Windows 10에서 검색 상자](media/type-here-to-search.png)

   (또는 Cortana를 사용하도록 설정한 경우 "Hey Cortana" 및 "시스템 소리 변경"이라고 차례로 말합니다.)

2. **시스템 소리 변경**을 두 번 클릭합니다.

   ![Windows 10에서 검색 결과](media/change-system-sounds.png)

3. **소리** 대화 상자에서 **소리** 탭을 클릭합니다. <br><br>
   그런 다음 **프로그램 이벤트**에서 **Microsoft Visual Studio**로 스크롤하여 사용자가 선택한 이벤트에 적용하려는 소리를 선택합니다.

   ![Windows 10에서 소리 애플릿의 소리 탭](media/sound-applet.png)

4. **확인**을 클릭합니다.

## <a name="see-also"></a>참고 항목

* [Visual Studio의 접근성 기능](../../ide/reference/accessibility-features-of-visual-studio.md)
* [방법: Visual Studio에서 메뉴 및 도구 모음 사용자 지정](../../ide/how-to-customize-menus-and-toolbars-in-visual-studio.md)
* [Visual Studio IDE 개인 설정](../../ide/personalizing-the-visual-studio-ide.md)
* [Microsoft Accessibility](https://www.microsoft.com/Accessibility)
* [접근성(Mac용 Visual Studio)](/visualstudio/mac/accessibility)