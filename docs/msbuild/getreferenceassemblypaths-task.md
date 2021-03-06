---
title: GetReferenceAssemblyPaths 작업 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 178ef49c-5dee-405b-a14b-a37f41dc0609
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e752e345de9211a2b6c8d8fe076be863a04c70ca
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977137"
---
# <a name="getreferenceassemblypaths-task"></a>GetReferenceAssemblyPaths 작업
다양한 프레임워크의 참조 어셈블리 경로를 반환합니다.

## <a name="parameters"></a>매개 변수
 다음 표에서는 `GetReferenceAssemblyPaths` 작업의 매개 변수에 대해 설명합니다.

|매개 변수|설명|
|---------------|-----------------|
|`ReferenceAssemblyPaths`|선택적 `String[]` 출력 매개 변수입니다.<br /><br /> `TargetFrameworkMoniker` 매개 변수를 기반으로 경로를 반환합니다. `TargetFrameworkMoniker`가 null이거나 비어 있으면 이 경로는 `String.Empty`가 됩니다.|
|`FullFrameworkReferenceAssemblyPaths`|선택적 `String[]` 출력 매개 변수입니다.<br /><br /> 모니커의 프로필 부분을 고려하지 않고 `TargetFrameworkMoniker` 매개 변수를 기반으로 경로를 반환합니다. `TargetFrameworkMoniker`가 null이거나 비어 있으면 이 경로는 `String.Empty`가 됩니다.|
|`TargetFrameworkMoniker`|선택적 `String` 매개 변수입니다.<br /><br /> 참조 어셈블리 경로와 연결된 대상 프레임워크 모니커를 지정합니다.|
|`RootPath`|선택적 `String` 매개 변수입니다.<br /><br /> 참조 어셈블리 경로를 생성하는 데 사용할 루트 경로를 지정합니다.|
|`BypassFrameworkInstallChecks`|선택적 <xref:System.Boolean> 매개 변수입니다.<br /><br /> `true`인 경우 대상 프레임워크에 따라 특정 런타임 프레임워크가 설치되었는지 확인하기 위해 기본적으로 `GetReferenceAssemblyPaths`가 수행하는 기본 검사를 무시합니다.|
|`TargetFrameworkMonikerDisplayName`|선택적 `String` 출력 매개 변수입니다.<br /><br /> 대상 프레임워크 모니커의 표시 이름을 지정합니다.|

## <a name="remarks"></a>주의
 이 작업은 표에 나열된 매개 변수 외에, <xref:Microsoft.Build.Utilities.Task> 클래스에서 직접 상속하는 <xref:Microsoft.Build.Tasks.TaskExtension> 클래스의 매개 변수도 상속합니다. 이러한 추가 매개 변수 및 해당 설명이 포함된 목록은 [TaskExtension 기본 클래스](../msbuild/taskextension-base-class.md)를 참조하세요.

## <a name="see-also"></a>참고 항목
- [작업](../msbuild/msbuild-tasks.md)
- [작업 참조](../msbuild/msbuild-task-reference.md)