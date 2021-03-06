---
title: RequiresFramework35SP1Assembly 작업 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- RequiresFramework35SP1Assembly task [MSBuild]
- MSBuild, RequiresFramework35SP1Assembly task
ms.assetid: 755c018a-8a8b-4c94-8aee-3f171fc419e5
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ada207a619021922b999d0e821ecf27ba48dbb38
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MTE95
ms.contentlocale: ko-KR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59650644"
---
# <a name="requiresframework35sp1assembly-task"></a>RequiresFramework35SP1Assembly 작업
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

애플리케이션에 .NET Framework 3.5 SP1이 필요한지 여부를 확인합니다.  
  
## <a name="parameters"></a>매개 변수  
 다음 표에서는 `RequiresFramework35SP1Assembly` 작업의 매개 변수에 대해 설명합니다.  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`Assemblies`|선택적 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 매개 변수입니다.<br /><br /> 애플리케이션에서 참조되는 어셈블리를 지정합니다.|  
|`CreateDesktopShortcut`|선택적 `Boolean` 매개 변수입니다.<br /><br /> `true`인 경우 설치하는 동안 데스크톱에서 바로 가기 아이콘을 만듭니다.|  
|`DeploymentManifestEntryPoint`|선택적 <xref:Microsoft.Build.Framework.ITaskItem> 매개 변수입니다.<br /><br /> 애플리케이션에 대한 매니페스트 파일 이름을 지정합니다.|  
|`EntryPoint`|선택적 <xref:Microsoft.Build.Framework.ITaskItem> 매개 변수입니다.<br /><br /> 애플리케이션이 실행될 때 실행되어야 하는 어셈블리를 지정합니다.|  
|`ErrorReportUrl`|선택적 `String` 매개 변수입니다.<br /><br /> ClickOnce 설치 중에 발생되는 대화 상자에 표시되는 웹 사이트를 지정합니다.|  
|`Files`|선택적 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 매개 변수입니다.<br /><br /> 애플리케이션을 게시할 때 배포되는 파일 목록을 지정합니다.|  
|`ReferencedAssemblies`|선택적 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 매개 변수입니다.<br /><br /> 프로젝트에서 참조되는 어셈블리를 지정합니다.|  
|`RequiresMinimumFramework35SP1`|선택적 `Boolean` 출력 매개 변수입니다.<br /><br /> `true`인 경우 애플리케이션에 .NET Framework 3.5 SP1이 필요합니다.|  
|`SigningManifests`|선택적 `Boolean` 출력 매개 변수입니다.<br /><br /> `true`인 경우 ClickOnce 매니페스트가 서명됩니다.|  
|`SuiteName`|선택적 `String` 매개 변수입니다.<br /><br /> **시작** 메뉴에서 애플리케이션을 설치할 폴더 이름을 지정합니다.|  
|`TargetFrameworkVersion`|선택적 `String` 매개 변수입니다.<br /><br /> 이 애플리케이션의 대상 .NET Framework 버전을 지정합니다.|  
  
## <a name="remarks"></a>주의  
 이 작업은 표에 나열된 매개 변수 외에, <xref:Microsoft.Build.Utilities.Task> 클래스에서 직접 상속하는 <xref:Microsoft.Build.Tasks.TaskExtension> 클래스의 매개 변수도 상속합니다. 이러한 추가 매개 변수 및 해당 설명이 포함된 목록은 [TaskExtension Base Class](../msbuild/taskextension-base-class.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [작업](../msbuild/msbuild-tasks.md)   
 [작업 참조](../msbuild/msbuild-task-reference.md)
