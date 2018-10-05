---
title: '방법: 네이티브 런타임 검사 사용 | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- c.runtime.errorchecks
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- /RTC compiler option [C++], /O compiler option
- run-time checks, native
- stack, pointer corruption
- stack pointers, corruption
- /O compiler option, /RTC option
- run-time errors, error checks
- O compiler option, /RTC option
- debugger, runtime errors
- variables [debugger], loss of data
- runtime_checks pragma
- variables [debugger], catching dependencies on uninitialized local variables
- run-time errors, debugging
- debugger, native run-time checks
- optimized build option
- RTC compiler option, /O compiler option
- native run-time checks
- run-time checks
- debugging arrays
- stack pointers
- arrays [Visual Studio], debugging
ms.assetid: dc7b2f1e-5ff6-42e0-89b3-dc9dead83ee1
caps.latest.revision: 24
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e90af82b5f3d7cd88d3b8488b0ebd9a4359b566f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47543702"
---
# <a name="how-to-use-native-run-time-checks"></a>방법: 네이티브 런타임 검사 기능 사용
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [방법: 사용 하 여 네이티브 런타임 검사](https://docs.microsoft.com/visualstudio/debugger/how-to-use-native-run-time-checks)합니다.  
  
Visual c + +에서는 네이티브 따르면 [runtime_checks](http://msdn.microsoft.com/library/ae50b43f-f88d-47ad-a2db-3389e9e7df5b) 와 같은 일반적인 런타임 오류를 catch 합니다.  
  
-   스택 포인터 손상  
  
-   지역 배열의 오버런  
  
-   스택 손상  
  
-   초기화되지 않은 지역 변수에 대한 종속성  
  
-   Short형 변수에 할당한 경우 발생한 데이터 손실  
  
 **/RTC** 를 최적화된 빌드(**/O**)와 함께 사용하면 컴파일러 오류가 발생합니다. 최적화된 빌드에는 `runtime_checks` pragma를 사용해도 적용되지 않습니다.  
  
 런타임 검사가 활성화된 상태에서 프로그램을 디버깅하면 런타임 오류가 발생한 경우 기본적으로 프로그램을 중지하고 디버거를 중단합니다. 모든 런타임 검사의 기본 동작은 변경할 수 있습니다. 자세한 내용은 [디버거를 사용한 예외 관리](../debugger/managing-exceptions-with-the-debugger.md)합니다.  
  
 다음 절차에서는 디버그 빌드에서 네이티브 런타임 검사 기능을 활성화하는 방법과 네이티브 런타임 검사 동작을 수정하는 방법에 대해 설명합니다.  
  
 이 섹션의 다른 항목에서는 다음 내용에 대해 설명합니다.  
  
-   [C 런타임 라이브러리와 함께 런타임 검사 사용자 지정](../debugger/native-run-time-checks-customization.md)  
  
-   [C 런타임 라이브러리 없이 런타임 검사 사용](../debugger/using-run-time-checks-without-the-c-run-time-library.md)  
  
### <a name="to-enable-native-run-time-checks-in-a-debug-build"></a>디버그 빌드에 네이티브 런타임 검사 기능을 사용하려면  
  
-   **/RTC** 옵션을 사용하고 C 런타임 라이브러리의 디버그 버전(예: /MDd)으로 연결합니다.  
  
### <a name="to-modify-native-run-time-check-behavior"></a>네이티브 런타임 검사 동작을 수정하려면  
  
-   `runtime_checks` pragma를 사용합니다.  
  
## <a name="see-also"></a>참고 항목  
 [Visual Studio의 디버깅](../debugger/debugging-in-visual-studio.md)   
 [runtime_checks](http://msdn.microsoft.com/library/ae50b43f-f88d-47ad-a2db-3389e9e7df5b)   
 [런타임 오류 검사](http://msdn.microsoft.com/library/c965dd01-57ad-4a3c-b1d6-5aa04f920501)




