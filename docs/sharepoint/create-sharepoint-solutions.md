---
title: SharePoint 솔루션 만들기 | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 2b3138e148ea44371c7bd9b5fb82c583cd00e832
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63436419"
---
# <a name="create-sharepoint-solutions"></a>SharePoint 솔루션 만들기
  SharePoint 애플리케이션을 SharePoint Designer에서 만드는 대신 Visual Studio에서 만들 수 있습니다. Visual Studio에서는 고급 디버깅 도구, IntelliSense, 문 완성, 프로젝트 템플릿 등의 기능이 제공되므로 SharePoint 개발을 신속하게 수행할 수 있습니다. 또한 Visual Studio는 고급 .NET Framework 기반 도구 및 언어를 활용합니다. Visual Basic 또는 Visual C#을 사용하여 SharePoint 프로젝트를 개발할 수 있으며 JavaScript를 사용하여 SharePoint 프로젝트용 앱을 개발할 수 있습니다.

 SharePoint 2013 및 SharePoint 추가 기능에 대한 자세한 내용은 [SharePoint 2013](https://products.office.com/previous-versions/microsoft-sharepoint-2013) 및 [SharePoint용 앱 빌드](/sharepoint/dev/sp-add-ins/sharepoint-add-ins)를 참조하세요.

> [!NOTE]
> 새 [SharePoint 추가 기능 모델](/sharepoint/dev/sp-add-ins/sharepoint-add-ins) 을 사용하여 사용자를 위한 SharePoint 환경을 확장하는 방법을 알아봅니다. 이러한 추가 기능은 SharePoint 솔루션에 비해 차지하는 공간이 매우 적으며 HTML5, JavaScript, CSS3, XML 등 거의 모든 웹 프로그래밍 기술을 사용하여 빌드할 수 있습니다.

|||
|-|-|
|![설명서](../sharepoint/media/vs-icon-documentation.gif "설명서")|**문서**<br /><br /> -   [시작 &#40;Visual Studio에서 SharePoint 개발&#41;](../sharepoint/getting-started-sharepoint-development-in-visual-studio.md)<br />-   [SharePoint 솔루션 개발](../sharepoint/developing-sharepoint-solutions.md)<br />-   [SharePoint 솔루션 지역화](../sharepoint/localizing-sharepoint-solutions.md)<br />-   [빌드 및 SharePoint 솔루션 디버깅](../sharepoint/building-and-debugging-sharepoint-solutions.md)<br />-   [패키지 및 배포 하는 SharePoint 솔루션](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)<br />-   [Visual Studio에서 SharePoint 도구 확장](../sharepoint/extending-the-sharepoint-tools-in-visual-studio.md)|
|![설명서](../sharepoint/media/vs-icon-documentation.gif "설명서")|**주요 작업**<br /><br /> -   [연습: SharePoint 용 사이트 열, 콘텐츠 형식 및 목록 만들기](../sharepoint/walkthrough-create-a-site-column-content-type-and-list-for-sharepoint.md)<br />-   [방법: 이벤트 수신기 만들기](../sharepoint/how-to-create-an-event-receiver.md)<br />-   [방법: BDC 모델 만들기](../sharepoint/how-to-create-a-bdc-model.md)<br />-   [방법: SharePoint 웹 파트 만들기](../sharepoint/how-to-create-a-sharepoint-web-part.md)<br />-   [방법: SharePoint 응용 프로그램 페이지 또는 웹 파트에 대 한 사용자 정의 컨트롤 만들기](../sharepoint/how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part.md)|
|![연습](../sharepoint/media/vs-icon-walkthroughs.gif "연습")|**연습**<br /><br /> -   [SharePoint 개발 연습](../sharepoint/sharepoint-development-walkthroughs.md)|
|![코드 샘플](../sharepoint/media/vs-icon-codesamples.gif "코드 샘플")|**코드 샘플**<br /><br /> -   [SharePoint 개발 샘플](../sharepoint/sharepoint-development-samples.md)<br />-   [SharePoint 개발자 다운로드](/sharepoint/dev/)|
|![교육](../sharepoint/media/vs-icon-training.gif "교육")|**교육**<br /><br /> -   [SharePoint 개발에 대한 자세한 정보](/sharepoint/dev/)|
|![포럼](../sharepoint/media/vs-icon-forums.gif "포럼")|**포럼**<br /><br /> -   [Visual Studio에서 SharePoint 개발](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=vssharepointdevelopment)<br />-   [SharePoint 2010](https://social.msdn.microsoft.com/Forums/sharepoint/home?category=sharepoint2010,sharepoint)|
|![교육](../sharepoint/media/vs-icon-training.gif "교육")|**Blogs**<br /><br /> -   [Visual Studio SharePoint 개발 블로그](https://blogs.msdn.microsoft.com/vssharepointtoolsblog/)|
|![어떻게 할까요? 비디오](../sharepoint/media/vs-icon-howdoivideos.gif "어떻게 할까요? 비디오")|**어떻게 할까요? 비디오**<br /><br /> -   [어떻게 할까요 Visual Studio 2010에서 SharePoint 2010 용 시각적 웹 파트 만들기](https://visualstudio.microsoft.com/)<br />-   [어떻게 할까요 Visual Studio 2010에서 SharePoint 2010 용 콘텐츠 형식 만들기](/previous-versions/visualstudio/visual-studio-2010/dd831853\(v\=vs.100\))<br />-   [어떻게 할까요 Visual Studio 2010에서 SharePoint 2010 용 사이트 정의 만들기](/previous-versions/visualstudio/visual-studio-2010/dd831853\(v\=vs.100\))<br />-   [어떻게 할까요 Visual Studio 2010을 사용 하 여 SharePoint 2010 용 비즈니스 데이터 연결 모델 만들기](/previous-versions/visualstudio/visual-studio-2010/dd831853\(v\=vs.100\))|
|![Channel 9 비디오](../sharepoint/media/vs-icon-channel9videos.gif "Channel 9 비디오")|**Channel 9 비디오 보기**<br /><br /> -   [Visual Studio 2010의 SharePoint 개발 개요](https://channel9.msdn.com/blogs/funkyonex/overview-of-sharepoint-development-in-visual-studio-2010)<br />-   [Visual Studio 2010을 사용한 SharePoint 2010 웹 파트 빌드 모범 사례](https://channel9.msdn.com/blogs/funkyonex/best-practices-on-building-sharepoint-2010-web-parts-with-visual-studio-2010)<br />-   [Visual Studio 2010의 SharePoint 기능 및 패키지 디자이너](https://channel9.msdn.com/blogs/funkyonex/sharepoint-feature-and-package-designers-in-visual-studio-2010)|
|![개발자 센터](../sharepoint/media/vs-icon-msdndevcenter.gif "개발자 센터")|**개발자 센터**<br /><br /> -   [Visual Studio 개발 센터](https://visualstudio.microsoft.com/)<br />-   [SharePoint 개발자 센터](/sharepoint/dev/)<br />-   [SharePoint Server 개발자 센터](/previous-versions/office/fp161348\(v\=office.15\))<br />-   [SharePoint Designer 개발자 센터](/previous-versions/office/fp161348\(v\=office.15\))<br />-   [ASP.NET 개발자 센터](https://msdn.microsoft.com/aa336522.aspx)|
|![사용자 의견 제공](../sharepoint/media/vs-icon-feedback.gif "사용자 의견 제공")|**사용자 의견 제공**<br /><br /> Visual Studio 관련 의견 보내기<br /><br /> -   [Microsoft Connect](http://go.microsoft.com/fwlink/?LinkID=150463)<br /><br /> Visual Studio용 설명서 관련 의견 보내기<br /><br /> -   **Lightweight 보기.** 항목 윗부분에서 **이 항목 평가** 링크를 선택하여 해당 항목 아래쪽으로 이동한 다음 **이 페이지가 유용했습니까?** 라는 질문에 대해 **예** 또는 **아니요** 를 지정할 수 있습니다. **예**를 선택하면 표시되는 확인란 중 하나를 선택하거나 텍스트 상자에 추가 의견을 입력하거나 두 작업을 모두 수행할 수 있습니다. 작업을 완료한 후 **전송** 단추를 선택합니다.<br />-   **ScriptFree 보기.** 항목의 맨 위에 있는 선택 된 **피드백** TechNet 및 Expression 라이브러리 의견 포럼에서 의견을 제공 하는 링크입니다.<br />-   **클래식 보기.** 항목의 위쪽에서 **클릭하여 평가 및 의견 제공** 아이콘을 선택하여 항목에 대한 의견을 설명서 팀에 제공할 수 있습니다.|
