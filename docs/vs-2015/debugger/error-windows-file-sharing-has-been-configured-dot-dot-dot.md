---
title: '오류: Windows 파일 공유가 구성 되었습니다... | Microsoft Docs'
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
- vs.debug.error.remote_credentials_prohibited
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: c45a1b74-61ec-4c64-9e2c-13051a4f50a5
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9fc4d3fb02b1c7c9d5003f82fbe42be73c93d6eb
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47550623"
---
# <a name="error-windows-file-sharing-has-been-configured"></a>오류: ...Windows 파일 공유가 구성되었습니다.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [오류: Windows 파일 공유가 구성 되었습니다... ](https://docs.microsoft.com/visualstudio/debugger/error-windows-file-sharing-has-been-configured-dot-dot-dot).  
  
원격 컴퓨터에 다른 사용자 이름을 사용하여 연결하도록 Windows 파일 공유가 구성되었습니다. 이러한 구성은 원격 디버깅과 호환되지 않습니다.  
  
 현재 파일 공유 구성은 다른 사용자 이름을 사용하여 원격 컴퓨터에 연결하도록 설정되어 있습니다. 이러한 상황에서는 원격으로 디버깅할 수 없습니다.  
  
 이 오류를 해결하려면 다른 계정 이름을 사용하여 컴퓨터에 로그온하거나 디버깅할 때 사용하는 계정 이름을 사용하도록 파일 공유를 변경하십시오.  
  
 이 사용자 이름을 사용하여 원격 컴퓨터에 연결하려면 먼저 원격 컴퓨터와의 연결을 끊어야 합니다.  
  
### <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  다른 계정 이름을 사용하여 로컬 컴퓨터 즉, 디버깅하고 있는 컴퓨터에 로그온합니다.  
  
     또는  
  
     . 원격 컴퓨터와의 연결을 끊고 사용자의 계정 이름을 사용하여 다른 컴퓨터에 연결하도록 파일 공유를 다시 구성합니다.  
  
    1.  에 **시작** 메뉴에서 **Accessories**를 클릭 하 고 **명령 프롬프트**합니다.  
  
    2.  Windows 명령 프롬프트에 다음과 같이 입력합니다.  
  
         `net use /delete computer_name`  
  
    3.  Windows 도움말에 문서화된 방법을 사용하여 파일 공유 설정을 변경합니다.


