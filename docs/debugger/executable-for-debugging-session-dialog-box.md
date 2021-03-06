---
title: 디버깅 세션 대화 상자에 대 한 실행 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.exefordebug
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- executable files, specifying when debugging
- DLLs, debugging
- debugger, Executable for Debugging Session dialog box
- Executable for Debugging Session dialog box
ms.assetid: c0ddbe32-b99f-4425-acf1-f48842804f56
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 41b93ae19afd54b6e22458d1ba12029d5bb93cf3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62849952"
---
# <a name="executable-for-debugging-session-dialog-box"></a>디버깅 세션에 사용할 실행 파일 대화 상자

이 대화 상자는 실행 파일이 지정되지 않은 DLL을 디버깅하려고 할 때 나타납니다. Visual Studio는 DLL을 직접 시작할 수 없습니다. 대신, Visual Studio는 지정된 된 실행 파일을 시작합니다. 실행 파일을 통해 호출 될 때 DLL을 디버깅할 수 있습니다.

 **실행 파일 이름을** 디버깅 하는 DLL을 호출 하는 실행 파일의 경로 이름을 입력 합니다.

 **프로젝트 수 있는 URL (ATL 서버 전용)에 액세스할** ATL 서버 DLL을 디버깅 하는 경우 URL을 입력 프로젝트를 찾을 수 있습니다.

 입력 한 이러한 설정은 프로젝트 속성 페이지에에서 저장 되므로 이후 디버깅 세션에서 다시 입력할 필요가 없습니다. 설정을 변경해야 하는 경우에는 속성 페이지를 열고 값을 변경할 수 있습니다. 디버깅 세션의 실행 파일 지정에 대한 자세한 내용은 [DLL 디버깅](../debugger/how-to-debug-from-a-dll-project.md)을 참조하세요.

## <a name="see-also"></a>참고 항목

- [Visual Studio의 디버깅](../debugger/index.md)
- [디버거 소개](../debugger/debugger-feature-tour.md)