---
title: '방법: WPF 트리 시각화 도우미를 사용 하 여 | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- WPF, debugging
- debugging, WPF
ms.assetid: 2a1bf1cd-90f9-4d06-9fb4-1bfc925afef3
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9e99bdaac9feb343c594e808433d686e5d607b45
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "47592827"
---
# <a name="how-to-use-the-wpf-tree-visualizer"></a>방법: WPF 트리 시각화 도우미 사용
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [방법: WPF 트리 시각화 도우미를 사용 하 여](https://docs.microsoft.com/visualstudio/debugger/how-to-use-the-wpf-tree-visualizer)입니다.  
  
WPF 트리 시각화 도우미를 사용하여 WPF 개체의 표시 트리를 탐색하고 트리에 포함된 개체의 WPF 종속성 속성을 볼 수 있습니다. 시각적 트리에 대 한 자세한 내용은 참조 하세요. [WPF의 트리](http://msdn.microsoft.com/library/e83f25e5-d66b-4fc7-92d2-50130c9a6649)합니다. 종속성 속성에 대 한 자세한 내용은 참조 하세요. [종속성 속성 개요](http://msdn.microsoft.com/library/d119d00c-3afb-48d6-87a0-c4da4f83dee5)합니다.  
  
 WPF 트리 시각화 도우미를 열면 두 개의 창이 표시 됩니다: 합니다 **시각적 트리** 왼쪽 하며 **의 속성** _이름_**:**  _형식_ 오른쪽 창입니다. 모든 개체를 선택 합니다 **시각적 트리** 창 및 **속성을** _이름_**:**_형식_ 창은 해당 개체에 대 한 속성을 표시 하도록 자동으로 업데이트 합니다.  
  
### <a name="to-open-the-wpf-tree-visualizer"></a>WPF 트리 시각화 도우미를 열려면  
  
1.  DataTip에서 **Watch** 창 **자동** 창 또는 **지역** WPF 개체 이름 옆에 있는 창에서 돋보기 아이콘 옆의 화살표를 클릭 합니다.  
  
     시각화 도우미의 목록이 나타납니다.  
  
2.  클릭 **WPF 트리 시각화 도우미**합니다.  
  
### <a name="to-search-the-visual-tree"></a>표시 트리를 검색하려면  
  
-   에 **시각적 트리** 창에서 검색 하려는 문자열을 입력 합니다 **검색** 상자입니다.  
  
     WPF 트리 시각화 도우미가 입력한 문자열과 일치하는 표시 트리의 첫 번째 개체를 즉시 찾습니다. 문자를 추가로 입력하여 좀 더 정확하게 일치하는 항목을 찾을 수 있습니다.  
  
    -   시각적 트리 내에서 다음 일치 항목으로 이동 하려면 클릭 **다음**합니다.  
  
    -   이전 일치 항목으로 돌아가려면 클릭 **Prev**합니다.  
  
    -   검색 조건을 지우려면 클릭 **의 선택을 취소**합니다.  
  
### <a name="to-search-the-properties-list"></a>속성 목록을 검색하려면  
  
-   에 **의 속성** _이름_**:**_형식_ 창에서 검색 하려는 문자열을 입력 합니다 **필터링**상자입니다.  
  
     WPF 트리 시각화 도우미가 입력한 문자열과 일치하는 속성을 즉시 찾습니다. 이제 목록에는 입력한 문자열과 일치하는 속성만 표시됩니다. 문자를 추가로 입력하여 좀 더 정확하게 일치하는 항목을 찾을 수 있습니다.  
  
    -   검색 조건을 지우려면 클릭 **의 선택을 취소**합니다.  
  
### <a name="to-close-the-visualizer"></a>시각화 도우미를 닫으려면  
  
-   클릭 합니다 **닫기** 대화 상자의 오른쪽 위 모서리에 있는 아이콘입니다.  
  
## <a name="see-also"></a>참고 항목  
 [방법: 시각화 도우미 사용](../misc/how-to-use-a-visualizer.md)   
 [사용자 지정 시각화 도우미 만들기](../debugger/create-custom-visualizers-of-data.md)   
 [WPF의 트리](http://msdn.microsoft.com/library/e83f25e5-d66b-4fc7-92d2-50130c9a6649)   
 [종속성 속성 개요](http://msdn.microsoft.com/library/d119d00c-3afb-48d6-87a0-c4da4f83dee5)


