---
title: '오류: 원격 컴퓨터의 Microsoft Visual Studio 원격 디버깅 모니터가 이 컴퓨터에 연결할 수 있는 권한이 없습니다.'
titleSuffix: ''
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.access_denied_oncallback
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, Windows version error
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ac6e632927878988f8a3ff86d63fea080a45bd6d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62850441"
---
# <a name="error-the-microsoft-visual-studio-remote-debugging-monitor-on-the-remote-computer-does-not-have-permission-to-connect-to-this-computer"></a>오류: 원격 컴퓨터의 Microsoft Visual Studio 원격 디버깅 모니터가 이 컴퓨터에 연결할 수 있는 권한이 없습니다.

이 오류는 로컬 컴퓨터에 계정이 없는 사용자가 Visual Studio 원격 디버깅 모니터(msvsmon)를 실행하려고 할 때 발생합니다.

## <a name="to-fix-this-problem"></a>이 문제를 해결하려면

- 원격 컴퓨터에서 msvsmon을 실행하는 사용자 계정과 이름 및 암호가 같은 사용자 계정을 Visual Studio 디버거 호스트 컴퓨터에 추가합니다.

   \- 또는 -

- 로컬 컴퓨터에 대한 호출 권한이 있는 사용자로 msvsmon을 실행합니다. 즉, 이 사용자는 msvsmon 컴퓨터의 관리자이자 도메인 사용자여야 합니다. msvsmon을 실행하기 위한 사용자 계정은 다음 두 가지 방법 중 하나로 지정할 수 있습니다.

  - msvsmon 아이콘을 마우스 오른쪽 단추로 클릭하고 바로 가기 메뉴에서 **다음 계정으로 실행**을 선택합니다.

    \- 또는 -

  - 명령 프롬프트에서 `runas.exe`를 실행합니다.

## <a name="see-also"></a>참고자료

- [원격 디버깅 오류 및 문제 해결](../debugger/remote-debugging-errors-and-troubleshooting.md)
- [Remote Debugging](../debugger/remote-debugging.md)