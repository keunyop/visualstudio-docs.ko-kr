---
title: CombinePath 작업 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, CombinePath task
- CombinePath task [MSBuild]
ms.assetid: c20edbf4-3d4f-4f66-b1d5-753a0d858ed8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6b73ddd4715d3abd29f87d7ef38a269d821733ba
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62569729"
---
# <a name="combinepath-task"></a>CombinePath 작업
지정된 경로를 단일 경로로 결합합니다.

## <a name="task-parameters"></a>작업 매개 변수
 다음 표에서는 [CombinePath 작업](../msbuild/combinepath-task.md)의 매개 변수에 대해 설명합니다.

|매개 변수|설명|
|---------------|-----------------|
|`BasePath`|필수 `String` 매개 변수입니다.<br /><br /> 다른 경로와 결합할 기본 경로입니다. 상대 경로, 절대 경로 또는 빈 값일 수 있습니다.|
|`Paths`|필수 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 매개 변수입니다.<br /><br /> BasePath와 결합되어 결합된 경로를 구성할 개별 경로의 목록입니다. 경로는 상대 경로이거나 절대 경로일 수 있습니다.|
|`CombinedPaths`|선택적 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 출력 매개 변수입니다.<br /><br /> 이 작업에서 만든 조합된 경로입니다.|

## <a name="remarks"></a>주의
 이 작업은 위에 나와 있는 매개 변수 외에 <xref:Microsoft.Build.Utilities.Task> 클래스에서 직접 상속하는 <xref:Microsoft.Build.Tasks.TaskExtension> 클래스의 매개 변수도 상속합니다. 이러한 추가 매개 변수 및 해당 설명이 포함된 목록은 [TaskExtension 기본 클래스](../msbuild/taskextension-base-class.md)를 참조하세요.

## <a name="see-also"></a>참고 항목
- [작업](../msbuild/msbuild-tasks.md)
- [작업 참조](../msbuild/msbuild-task-reference.md)