---
title: '오류: 원격 컴퓨터를 원격 연결 대화 상자에 나타나지 않으면 | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: dd194bc26574e8004894a72ce29d753cabf66a21
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62850809"
---
# <a name="error-remote-machine-does-not-appear-in-a-remote-connections-dialog"></a>오류: 원격 컴퓨터는 원격 연결 대화 상자에 표시되지 않습니다.
원격 컴퓨터가 원격 연결 대화 상자에 표시되지 않는 경우 다음과 같은 일반적인 원인을 확인합니다.

 관리 되는 호환성 모드를 사용 하는 경우에 Visual Studio 2010 설명서를 확인 하세요. [원격 디버깅-문제 해결 Visual Studio 2010](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/2ys11ead(v=vs.100))합니다.

### <a name="common-causes-for-this-error"></a>이 오류의 일반적인 원인

- 원격 컴퓨터가 다른 서브넷에 있는 컴퓨터에서 실행되고 있습니다. 이 문제를 해결하려면 수동으로 한정자 대화 상자에 컴퓨터 이름 또는 IP 주소를 입력합니다.

- 원격 컴퓨터에서 원격 디버거가 실행되고 있지 않습니다. 이 문제를 해결하려면 원격 디버거를 시작합니다.

- 방화벽이 Visual Studio와 원격 컴퓨터 간의 통신을 차단하고 있습니다. 이 문제를 해결하려면 Visual Studio와 원격 디버거(msvsmon) 간의 통신을 허용하도록 방화벽을 구성합니다.

- 바이러스 백신 소프트웨어가 Visual Studio와 원격 컴퓨터 간의 통신을 차단하고 있습니다. 이 문제를 해결하려면 Visual Studio와 원격 디버거(msvsmon) 간의 통신을 허용하도록 바이러스 백신 소프트웨어를 구성합니다.

## <a name="see-also"></a>참고 항목
- [Remote Debugging](../debugger/remote-debugging.md)