---
title: 무엇이 잘못된 매개 변수 값을 전달하는지 어떻게 알 수 있습니까? | Microsoft 문서
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.parameters
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- debugging [C++], parameters
- parameters [debugger]
- passing parameters, troubleshooting wrong values
- functions [debugger], detecting wrong parameter values
- parameter values, troubleshooting
ms.assetid: 1f1ae455-0e25-4e9d-b33f-53908f5bd6ce
caps.latest.revision: 22
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fa3f96cd6ee5ff3c4f78a3e9a9bc89b2037066fc
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60053834"
---
# <a name="how-can-i-find-out-who-is-passing-a-wrong-parameter-value"></a>무엇이 잘못된 매개 변수 값을 전달하는지 어떻게 알 수 있습니까?
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

문제 설명  
 함수 하나에 잘못된 매개 변수 값이 전달되고 있습니다. 모든 위치에서 이 함수가 호출됩니다. 무엇이 잘못된 값을 전달하고 있는지 어떻게 알 수 있습니까?  
  
## <a name="solution"></a>솔루션  
  
#### <a name="to-resolve-this-problem"></a>이 문제를 해결하려면  
  
1. 함수 시작 부분에 위치 중단점을 설정합니다.  
  
2. 마우스 오른쪽 단추로 중단점을 클릭하고 **조건**을 선택합니다.  
  
3. **중단점 조건** 대화 상자에서 **조건** 확인란을 클릭합니다. 참조 [중단점 고급](../debugger/using-breakpoints.md#BKMK_Specify_a_breakpoint_condition_using_a_code_expression)합니다.  
  
4. 텍스트 상자에 `Var==3` 같은 식을 입력합니다. 여기서 `Var`은 잘못된 값을 포함하는 매개 변수의 이름이고 `3`은 이 매개 변수에 전달된 잘못된 값입니다.  
  
5. **참인 경우** 라디오 단추를 선택하고 **확인** 단추를 클릭합니다.  
  
6. 이제 프로그램을 다시 실행합니다. `Var` 매개 변수의 값이 `3`인 경우 중단점은 함수의 시작 부분에서 프로그램을 중단하게 합니다.  
  
7. 호출 스택 창을 사용하여 호출하는 함수를 찾고 함수의 소스 코드를 탐색합니다. 자세한 내용은 [방법: 호출 스택 창 사용](../debugger/how-to-use-the-call-stack-window.md)을 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [네이티브 코드 디버깅 FAQ](../debugger/debugging-native-code-faqs.md)   
 [중단점](http://msdn.microsoft.com/fe4eedc1-71aa-4928-962f-0912c334d583)   
 [네이티브 코드 디버그](../debugger/debugging-native-code.md)
