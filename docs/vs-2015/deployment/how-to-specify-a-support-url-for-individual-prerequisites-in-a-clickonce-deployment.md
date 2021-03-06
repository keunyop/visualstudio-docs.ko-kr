---
title: '방법: ClickOnce 배포 시에서 개별 필수 구성 요소에 대 한 지원 URL 지정 | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, prerequisites
- ClickOnce deployment, URLs
ms.assetid: 590742c3-a286-4160-aa75-7a441bb2207b
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f272f1b7a8fc970ab616ba1c02e815cbb6ecb568
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60059138"
---
# <a name="how-to-specify-a-support-url-for-individual-prerequisites-in-a-clickonce-deployment"></a>방법: ClickOnce 배포 시에서 개별 필수 구성 요소에 대 한 지원 URL 지정
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

A [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 배포 필수 구성 요소에 대 한 클라이언트 컴퓨터에서 사용할 수 있어야 하는 다양 한 테스트 수를 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 응용 프로그램을 실행 합니다. 여기에 필요한 최소 버전의는 [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)], 운영 체제와 전역 어셈블리 캐시 (GAC)에 미리 설치 해야 하는 모든 어셈블리의 버전입니다. [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)]그러나 없습니다 스스로 설치 필수 구성이 요소 중 하나; 필수 구성 요소가 없는 경우 단순히 설치를 중지 하 고 설치에 실패 한 이유를 설명 하는 대화 상자를 표시 합니다.  
  
 필수 구성 요소를 설치 하는 방법은 두 가지가 있습니다. 부트스트래퍼 응용 프로그램을 사용 하 여 설치할 수 있습니다. 또는 필수 구성 요소를 찾을 수 없으면 대화 상자에서 사용자에 게 표시 되는 개별 필수 구성 요소에 대 한 지원 URL을 지정할 수 있습니다. 해당 URL에서 참조 하는 페이지는 필요한 필수 구성 요소를 설치 하기 위한 지침에 대 한 링크를 포함할 수 있습니다. 응용 프로그램에는 개별 필수 구성 요소에 대 한 지원 URL을 지정 하지 않는 경우 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 정의 되어 있는 경우 전체 응용 프로그램에 대 한 배포 매니페스트에 지정한 지원 URL이 표시 됩니다.  
  
 하는 동안 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], Mage.exe 및 MageUI.exe 모든 데 사용할 수 있습니다 생성 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 배포를 지원 하지 않습니다 이러한 도구의 직접 개별 필수 구성 요소에 대 한 지원 URL을 지정 합니다. 이 문서에서는 배포를 수정 하는 방법 설명 응용 프로그램 매니페스트 및이 포함 하도록 배포 매니페스트 Url을 지원 합니다.  
  
### <a name="specifying-a-support-url-for-an-individual-prerequisite"></a>개별 필수 구성 요소에 대 한 지원 URL을 지정합니다.  
  
1. 에 대 한 응용 프로그램 매니페스트 (.manifest 파일)를 열고 프로그램 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 텍스트 편집기에서 응용 프로그램입니다.  
  
2. 운영 체제 필수 구성 요소를 추가 합니다 `supportUrl` 특성을 `dependentOS` 요소:  
  
    ```  
     <dependency>  
        <dependentOS supportUrl="http://www.adatum.com/MyApplication/wrongOSFound.htm">  
          <osVersionInfo>  
            <os majorVersion="5" minorVersion="1" buildNumber="2600" servicePackMajor="0" servicePackMinor="0" />  
          </osVersionInfo>  
        </dependentOS>  
      </dependency>  
    ```  
  
3. 공용 언어 런타임에서의 특정 버전에 대 한 필수 구성 요소를 추가 합니다 `supportUrl` 특성을 `dependentAssembly` 공용 언어 런타임 종속성을 지정 하는 항목:  
  
    ```  
      <dependency>  
        <dependentAssembly dependencyType="preRequisite" allowDelayedBinding="true" supportUrl=" http://www.adatum.com/MyApplication/wrongClrVersionFound.htm">  
          <assemblyIdentity name="Microsoft.Windows.CommonLanguageRuntime" version="4.0.30319.0" />  
        </dependentAssembly>  
      </dependency>  
    ```  
  
4. 전역 어셈블리 캐시에 미리 설치 해야 하는 어셈블리에 대 한 필수 구성 요소를 설정 합니다 `supportUrl` 에 대 한는 `dependentAssembly` 필요한 어셈블리를 지정 하는 요소:  
  
    ```  
      <dependency>  
        <dependentAssembly dependencyType="preRequisite" allowDelayedBinding="true" supportUrl=" http://www.adatum.com/MyApplication/missingSampleGACAssembly.htm">  
          <assemblyIdentity name="SampleGACAssembly" version="5.0.0.0" publicKeyToken="04529dfb5da245c5" processorArchitecture="msil" language="neutral" />  
        </dependentAssembly>  
      </dependency>  
    ```  
  
5. 선택 사항입니다. .NET Framework 4를 대상으로 하는 응용 프로그램에 대 한 배포 매니페스트 (.application 파일)를 열에 대 한 프로그램 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 텍스트 편집기에서 응용 프로그램입니다.  
  
6. .NET Framework 4에 필수 구성 요소를 추가 합니다 `supportUrl` 특성을 `compatibleFrameworks` 요소:  
  
    ```  
    <compatibleFrameworks  xmlns="urn:schemas-microsoft-com:clickonce.v2" supportUrl="http://adatum.com/MyApplication/CompatibleFrameworks.htm">  
      <framework targetVersion="4.0" profile="Client" supportedRuntime="4.0.30319" />  
      <framework targetVersion="4.0" profile="Full" supportedRuntime="4.0.30319" />  
    </compatibleFrameworks>  
    ```  
  
7. 응용 프로그램 매니페스트를 수동으로 변경한 후 디지털 인증서를 사용 하 여 응용 프로그램 매니페스트에 다시 서명 후 업데이트 하 고도 배포 매니페스트에 다시 서명 합니다. Mage.exe를 사용 해야 합니다 또는 MageUI.exe SDK 도구를 사용 하 여 이러한 파일을 다시 생성으로이 작업을 위해 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 수동 변경 내용을 지웁니다. Mage.exe를 사용 하 여 매니페스트에 다시 서명할 수에 대 한 자세한 내용은 참조 하세요. [방법: 응용 프로그램 및 배포 매니페스트에 다시 서명](../deployment/how-to-re-sign-application-and-deployment-manifests.md)합니다.  
  
## <a name="net-framework-security"></a>.NET Framework 보안  
 지원 URL은 응용 프로그램은 부분 신뢰에서 실행 하도록 표시 되어 있으면 대화 상자에서 표시 되지 않습니다.  
  
## <a name="see-also"></a>참고 항목  
 [Mage.exe(매니페스트 생성 및 편집 도구)](http://msdn.microsoft.com/library/77dfe576-2962-407e-af13-82255df725a1)   
 [연습: ClickOnce 응용 프로그램 수동 배포](../deployment/walkthrough-manually-deploying-a-clickonce-application.md)   
 [\<compatibleFrameworks > 요소](../deployment/compatibleframeworks-element-clickonce-deployment.md)   
 [ClickOnce 및 Authenticode](../deployment/clickonce-and-authenticode.md)   
 [응용 프로그램 배포 필수 조건](../deployment/application-deployment-prerequisites.md)
