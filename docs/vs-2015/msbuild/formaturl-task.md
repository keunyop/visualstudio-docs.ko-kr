---
title: FormatUrl 작업 | Microsoft Docs
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
- MSBuild, FormatUrl task
- FormatUrl task [MSBuild]
ms.assetid: 81114b67-520f-43b5-8891-224f68a78516
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: bb870bcc3c4297d5d1b403176f931f75e418d423
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MTE95
ms.contentlocale: ko-KR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59651477"
---
# <a name="formaturl-task"></a>FormatUrl 작업
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

URL을 올바른 URL 형식으로 변환합니다.  
  
## <a name="parameters"></a>매개 변수  
 다음 표에서는 `FormatUrl` 작업의 매개 변수에 대해 설명합니다.  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`InputUrl`|선택적 `String` 매개 변수입니다.<br /><br /> 서식을 지정하려면 URL을 지정합니다.|  
|`OutputUrl`|선택적 `String` 출력 매개 변수입니다.<br /><br /> 서식이 지정된 URL을 지정합니다.|  
  
## <a name="remarks"></a>주의  
 이 작업은 표에 나열된 매개 변수 외에도 <xref:Microsoft.Build.Utilities.Task> 클래스에서 직접 상속하는 <xref:Microsoft.Build.Tasks.TaskExtension> 클래스의 매개 변수도 상속합니다. 이러한 추가 매개 변수 및 해당 설명이 포함된 목록은 [TaskExtension Base Class](../msbuild/taskextension-base-class.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [작업](../msbuild/msbuild-tasks.md)   
 [작업 참조](../msbuild/msbuild-task-reference.md)
