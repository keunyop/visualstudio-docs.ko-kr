---
title: Visual Studio 수정
titleSuffix: ''
description: Visual Studio를 수정하는 방법을 단계별로 알아봅니다.
ms.custom: H1Hack27Feb2017,seodec18
ms.date: 03/30/2018
ms.topic: conceptual
helpviewer_keywords:
- modify Visual Studio
- change visual studio
- changing Visual Studio
- customize Visual Studio
ms.assetid: 3399ea7b-a291-4a9e-80a1-b861a21afa1d
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: a08a14d8d07248efdcac759852a38777745e9a51
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62951584"
---
# <a name="modify-visual-studio-by-adding-or-removing-workloads-and-components"></a>워크로드와 구성 요소를 추가하거나 제거하여 Visual Studio 수정

::: moniker range="vs-2019"

Visual Studio를 쉽게 수정할 수 있어 원하는 때에 원하는 대로 포함할 수 있습니다. 이렇게 하려면 Visual Studio 설치 관리자를 열어 워크로드 및 구성 요소를 추가하거나 제거합니다.

::: moniker-end

::: moniker range="vs-2017"

수행하려는 작업에 맞게 Visual Studio를 쉽게 개인 설정할 수 있을 뿐만 아니라 더 쉽게 사용자 지정할 수도 있습니다. 그러면 새로운 Visual Studio 설치 관리자를 시작하고 원하는 대로 변경하면 됩니다.

::: moniker-end

방법은 다음과 같습니다.

## <a name="modify-workloads"></a>작업 수정

 작업에는 사용 중인 프로그래밍 언어 또는 플랫폼에 필요한 기능이 포함되어 있습니다. 작업을 사용하여 원하는 시기에 원하는 작업을 지원하도록 Visual Studio를 수정할 수 있습니다.

>[!IMPORTANT]
>Visual Studio를 설치, 업데이트 또는 수정하려면 관리 권한이 있는 계정으로 로그온해야 합니다. 자세한 내용은 [사용자 권한 및 Visual Studio](../ide/user-permissions-and-visual-studio.md)를 참조하세요.

::: moniker range="vs-2017"

1. 컴퓨터에서 Visual Studio 설치 관리자를 찾습니다.

     예를 들어 Windows 10을 실행하는 컴퓨터에서 **시작**을 선택한 다음, **Visual Studio 설치 관리자**로 나열되는 **V** 문자로 스크롤합니다.

     ![Visual Studio 설치 관리자](media/vs2017-locate-the-visual-studio-installer.PNG "Microsoft Visual Studio 설치 관리자 찾기")

     >[!NOTE]
     >일부 컴퓨터에서는 Visual Studio 설치 관리자가 **Microsoft Visual Studio 설치 관리자**로 문자 **“M”** 아래에 나열될 수 있습니다.<br/><br/> 또는 다음 위치에서 Visual Studio 설치 관리자를 찾을 수 있습니다.`C:\Program Files (x86)\Microsoft Visual Studio\Installer\vs_installer.exe`

1. 설치 관리자를 클릭하거나 탭한 다음, **수정**을 선택합니다.

     ![Visual Studio 실행 또는 수정](media/modify-visual-studio.png "Visual Studio 2017 수정")

     보류 중인 업데이트가 있는 경우 수정 단추는 다른 위치에 있습니다. 이러한 방식으로 Visual Studio를 업데이트하지 않고 수정할 수 있습니다. **자세히**를 클릭한 다음, **수정**을 선택합니다.

     ![Visual Studio 업데이트 또는 수정](media/modify-or-update-visual-studio.png "Visual Studio 2017 업데이트 또는 수정")

1. **작업** 화면에서 설치하거나 제거할 작업을 선택하거나 선택 취소합니다.

    ![Visual Studio 2017 설치 대화 상자](media/vs2017-modify-workloads.PNG "Visual Studio 2017에서 작업 선택")

1. **수정**을 다시 선택합니다.

1. 새 워크로드 및 구성 요소가 설치된 후 **시작**을 선택합니다.

::: moniker-end

::: moniker range="vs-2019"

1. 컴퓨터에서 Visual Studio 설치 관리자를 찾습니다.

     예를 들어 Windows 10을 실행하는 컴퓨터에서 **시작**을 선택한 다음, **Visual Studio 설치 관리자**로 나열되는 **V** 문자로 스크롤합니다.

     ![Visual Studio 설치 관리자 열기](media/vs2019-visual-studio-installer.png "Visual Studio 설치 관리자 열기")

     > [!NOTE]
     > 다음 위치에서 Visual Studio 설치 관리자를 찾을 수도 있습니다.
     >
     > `C:\Program Files (x86)\Microsoft Visual Studio\Installer\vs_installer.exe`

    계속하기 전에 설치 관리자를 업데이트해야 할 수 있습니다. 그렇다면 지시를 따르세요.

1. 설치 관리자에서 설치한 Visual Studio의 버전을 찾은 다음, **수정**을 선택합니다.

     ![Visual Studio 업데이트 또는 수정](media/vs-2019/vs-installer-modify.png "Visual Studio 2017 업데이트 또는 수정")

1. **워크로드** 탭에서 설치하거나 제거할 워크로드를 선택하거나 선택 취소합니다.

    ![Visual Studio 2019 설정 대화 상자](media/vs-2019/vs-installer-modify-workloads.png "Visual Studio 2019에서 작업 선택")

1. 기본 **다운로드하는 동안 설치** 옵션 또는 **모두 다운로드한 후 설치** 옵션을 허용할지 여부를 선택합니다.

    ![Visual Studio 2019 설치 옵션](media/vs-2019/vs-installer-choose-install-or-download.png "다운로드하는 동안 설치하거나 먼저 다운로드하고 나중에 설치하도록 선택")

    "모두 다운로드한 후 설치" 옵션은 먼저 다운로드한 다음, 나중에 설치하려는 경우에 유용합니다.

1. **수정**을 선택합니다.

1. 새 워크로드 및 구성 요소가 설치된 후 Visual Studio 설치 관리자에서 **시작**을 선택합니다.

::: moniker-end

## <a name="modify-individual-components"></a>개별 구성 요소 수정

Visual Studio 설치를 사용자 지정하기 위해 워크로드를 설치하지 않으려면 Visual Studio 설치 관리자에서 **개별 구성 요소** 탭을 선택하고 원하는 항목을 선택한 다음, 표시되는 메시지를 따릅니다.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>참고 항목

* [Visual Studio 업데이트](update-visual-studio.md)
* [Visual Studio의 네트워크 기반 설치 업데이트](update-a-network-installation-of-visual-studio.md)
* [Visual Studio 제거](uninstall-visual-studio.md)
