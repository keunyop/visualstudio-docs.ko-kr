---
title: 방화벽 또는 프록시 서버 뒤에 Mac용 Visual Studio 설치 및 사용
description: 이 문서에서는 Mac용 Visual Studio(및 Xamarin을 포함하는 해당 워크로드)가 회사 환경에서 작동할 수 있도록 방화벽의 허용 목록에 추가해야 하는 호스트 목록을 제공합니다.
ms.topic: troubleshooting
ms.assetid: 79C0F1A3-0C13-4E55-A820-1138A4082B77
author: asb3993
ms.author: amburns
ms.date: 10/23/2018
ms.openlocfilehash: 70ac8defdcea9cccd8a3b3f9be71d38fb78c9c50
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62997966"
---
# <a name="install-and-use-visual-studio-for-mac-behind-a-firewall-or-proxy-server"></a>방화벽 또는 프록시 서버 뒤에 Mac용 Visual Studio 설치 및 사용

사용자 또는 사용자 조직에서 방화벽 또는 프록시 서버와 같은 보안 조치를 사용하는 경우 Mac용 Visual Studio와 Azure 서비스를 설치 및 사용할 때 최상의 경험을 얻으려면 특정 포트 및 프로토콜을 열고 특정 도메인 URL을 “허용 목록”에 추가하는 것이 좋습니다.

- [**Mac용 Visual Studio 설치**](#install-visual-studio-for-mac): 이 표에는 Mac용 Visual Studio의 모든 기능과 워크로드에 액세스할 수 있도록 허용 목록에 추가할 URL이 나와 있습니다.

- [**Mac용 Visual Studio 사용**](#use-visual-studio-for-mac): 이 표에는 원하는 모든 서비스 및 기능에 액세스할 수 있도록 허용 목록에 추가할 URL이 나와 있습니다.

## <a name="install-visual-studio-for-mac"></a>Mac용 Visual Studio 설치

Mac용 Visual Studio 설치 관리자는 다양한 도메인 및 다운로드 서버에서 다운로드하므로, 구성에서 다음 도메인과 URL을 신뢰할 수 있는 것으로 추가하는 것이 좋습니다.

### <a name="microsoft-domains"></a>Microsoft 도메인

| 도메인| 용도 |
| ----------------------------------- |---------------------------|
| *.live.com| 자격 증명 관리 |
| app.vssps.visualstudio.com| 설치 관리자 메타데이터|
| vortex.data.microsoft.com | 크래시 및 오류 보고 |
| az667904.vo.msecnd.net| 크래시 및 오류 보고 |
| xamarin.com | 설치 관리자 메타데이터|
| xampubdl.blob.core.windows.net| 설치 관리자 패키지|
| download.visualstudio.microsoft.com | 설치 관리자 패키지|
| xamarin.azureedge.net | 설치 관리자 패키지|
| developer.xamarin.com | 설치 관리자 패키지|
| dc.services.visualstudio.com| 크래시 보고 |

### <a name="third-party-domains"></a>타사 도메인

| 도메인| 용도 |
| --------------------------|-------------------------|
| dl.google.com | Android SDK |
| download.oracle.com | Java SDK|
| api.apple-cloudkit.com| Apple 보안 서비스 |

## <a name="use-visual-studio-for-mac"></a>Mac용 Visual Studio 사용

프록시 또는 방화벽 뒤에 있는 동안 Mac용 Visual Studio에서 필요한 모든 기능에 액세스할 수 있으려면 다음 도메인 및 포트를 허용 목록에 추가하는 것이 좋습니다.

### <a name="general"></a>일반

| 도메인 | 포트|용도|
| ----------------------|------------------|------------------|
| go.microsoft.com | 80/443|Microsoft URL 확인 |
| vsstartpage.blob.core.windows.net| 80/443| 시작 페이지 데이터|
| software.xamarin.com |  80/443|업데이트 프로그램 서비스|
| addins.monodevelop.com | 80/443| 확장 서비스 |
| visualstudio-devdiv-c2s.msedge.net | 80/443| 실험적 기능 및 알림 |
| targetednotifications.azurewebsites.net|  80/443| 전체 알림 목록을 특정 유형의 컴퓨터/사용 시나리오에만 적용 가능한 목록으로 필터링하는 데 사용됩니다.|

### <a name="identity"></a>클레임

| 도메인 | 포트|용도|
| ----------------------|------------------|------------------|
| login.microsoftonline.com | 80/443| ID 공급자|
| secure.aadcdn.microsoftonline-p.com | 80/443|ID 공급자|
| dc.services.visualstudio.com| 80/443|크래시 보고|
| management.azure.com|80/443| Azure 서비스 API |

### <a name="nuget"></a>NuGet

| 도메인 | 포트|용도|
| ----------------------|------------------|------------------|
| api.nuget.org | 80/443|NuGet API|
| secure.aadcdn.microsoftonline-p.com |80/443| ID 공급자|

### <a name="android-projects"></a>Android 프로젝트

| 도메인| 용도|
| ------------------------------------|------------------------------------|
| time.android.com| Android Emulator의 시간 서버 |
| connectivitycheck.gstatic.com | Android Emulator의 연결|
| cloudconfig.googleapis.com| Android Emulator의 API|

## <a name="see-also"></a>참고 항목

- [방화벽 또는 프록시 서버 배후에서 Visual Studio 2017과 Azure 서비스 설치 및 사용](/visualstudio/install/install-and-use-visual-studio-behind-a-firewall-or-proxy-server)
- [Windows에서 유사한 문제 해결](/visualstudio/install/troubleshooting-network-related-errors-in-visual-studio)
