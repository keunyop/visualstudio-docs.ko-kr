---
title: 활동 디자이너를 시퀀스 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Sequence.UI
ms.assetid: 51c8d3cb-4d43-458f-9631-b63755f9ac94
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 47743feae8c256aa0ddb4e3270aca32b108aa5d1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63007481"
---
# <a name="sequence-activity-designer"></a>Sequence 활동 디자이너
<xref:System.Activities.Statements.Sequence> 활동에는 순서대로 실행되는 정렬된 자식 활동 컬렉션이 들어 있습니다.  
  
 활동 집합을 순서대로 실행하는 또 다른 방법은 <xref:System.Activities.Statements.Flowchart> 활동을 사용하는 것입니다. 사용을 고려 합니다 [순서도](../workflow-designer/flowchart-activity-designer.md) 단순 분기 또는 반복 프로그램 흐름이 있는 도식 적으로 보면 모델링 하려는 경우.  
  
## <a name="using-the-sequence-activity-designer"></a>Sequence 활동 디자이너 사용  
 추가할를 <xref:System.Activities.Statements.Sequence> 활동을 끌어서 합니다 **시퀀스** 활동 디자이너의는 **도구 상자** 에 놓습니다는 [!INCLUDE[wfd1](../includes/wfd1-md.md)] 화면. 이 자식 활동을 추가 하려면 <xref:System.Activities.Statements.Sequence> 활동의 다른 활동을 끌어 합니다 **도구 상자** 를 "여기에 작업 놓기" 힌트 텍스트가 있는 상자에 있는 삼각형 놓습니다.  
  
### <a name="sequence-activity-properties-in-the-workflow-designer"></a>워크플로 디자이너의 Sequence 활동 속성  
 다음 표에서는 <xref:System.Activities.Statements.Sequence> 속성을 보여 주고 디자이너에서 이 속성을 사용하는 방법을 설명합니다. 이러한 속성은 속성 표 또는 디자이너 화면에서 편집할 수 있습니다.  
  
|속성 이름|필수|사용법|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|머리글에 <xref:System.Activities.Statements.Sequence> 활동 디자이너의 이름을 지정합니다. 기본값은 Sequence입니다. 속성 표에서 또는 활동 디자이너의 머리글에서 직접 값을 편집할 수 있습니다.<br /><br /> <xref:System.Activities.Activity.DisplayName%2A>은 꼭 필요하지 않더라도 사용하는 것이 좋습니다.|  
  
## <a name="see-also"></a>참고 항목  
 [Flowchart](../workflow-designer/flowchart-activity-designer.md)   
 [제어 흐름](../workflow-designer/control-flow-activity-designers.md)