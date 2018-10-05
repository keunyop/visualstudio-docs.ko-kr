---
title: '테스트 영역 6: 삭제 | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- source control [Visual Studio SDK], deleting items
- source control plug-ins, deleting items
ms.assetid: 6f2e872c-5ba2-4303-9f50-a90cef9a6225
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a05b84b3c75cec22f008b5f690c8b4ee0f8c6df3
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47554057"
---
# <a name="test-area-6-delete"></a>테스트 영역 6: 삭제
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [테스트 영역 6: 삭제](https://docs.microsoft.com/visualstudio/extensibility/internals/test-area-6-delete)합니다.  
  
이 소스 제어 플러그 인 테스트 영역 삭제 작업을 설명합니다.  
  
 소스 제어에서 삭제 작업에 응답할 **솔루션 탐색기**합니다.  
  
 다음은 삭제할 수 있는 항목의 목록.  
  
-   파일  
  
-   폴더  
  
-   프로젝트  
  
 프로젝트 형식에 따라 수 있을 **제거할** (디스크의 파일을 리프) 프로젝트 또는 **삭제** 프로젝트 (디스크의 파일을 제거 합니다.). 프로젝트 또는 항목에서 두 동작 모두 제거 **솔루션 탐색기**합니다.  
  
## <a name="expected-behavior"></a>예상된 된 동작  
 Delete 테스트 영역에서 테스트 사례에 대해 예상 되는 동작은 다음과 같습니다.  
  
-   삭제 된 항목을 더 이상 내에서 볼 **솔루션 탐색기**합니다.  
  
-   삭제 된 프로젝트 또는 항목의 부모를 체크 아웃 필요에 따라 (가능한 경우 프롬프트.)  
  
-   을 체크 아웃 삭제 하거나 추가 항목 후에 나타나지 않습니다 합니다 **보류 중인 체크 인** 창입니다.  
  
-   항목이 여전히 소스 제어 저장소에서 삭제 한 후에 있고 수동으로 제거 해야 합니다.  
  
|작업|테스트 단계|확인 하려면 예상된 결과|  
|------------|----------------|--------------------------------|  
|클라이언트 프로젝트를 삭제 합니다.|1.  클라이언트 프로젝트를 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다.<br />3.  전체 프로젝트를 솔루션에서 제거|일반적인 예상된 동작입니다.|  
|빈 파일을 삭제 합니다.|1.  클라이언트 프로젝트를 만듭니다.<br />2.  0 바이트 파일을 프로젝트에 추가 합니다.<br />3.  소스 제어에 솔루션을 추가 합니다.<br />4.  파일을 선택, 삭제 합니다.|일반적인 예상된 동작입니다.|  
|파일 하나를 사용 하 여 폴더를 삭제 합니다.|1.  단일 프로젝트 솔루션을 만듭니다.<br />2.  폴더를 추가 합니다.<br />3.  폴더에 파일을 하나 추가 합니다.<br />4.  소스 제어에 솔루션을 추가 합니다.<br />5.  프롬프트를 방지 하려면 프로젝트를 확인 합니다.<br />6.  폴더를 삭제 합니다.|일반적인 예상된 동작입니다.|  
|파일 시스템 웹 프로젝트를 삭제 합니다.|1.  파일 시스템 웹 프로젝트 (사용 하 여 UNC 경로 지정 하려면 찾아보기 단추를) 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다.<br />3.  솔루션에서 전체 프로젝트를 제거 합니다.<br />4.  로컬 웹 프로젝트에 대해 1 ~ 3 단계를 반복 합니다. (코드를 통해 서로 다른 경로 실행 하지만 동일한 외부 인터페이스 및 동작).|일반적인 예상된 동작입니다.|  
|파일 시스템 웹 프로젝트에서 파일을 삭제 합니다.|1.  파일 시스템 웹 프로젝트를 만듭니다.<br />2.  소스 제어에 솔루션을 추가 합니다.<br />3.  프로젝트에서 파일을 삭제 합니다.<br />4.  로컬 웹 프로젝트에 대해 1 ~ 3 단계를 반복 합니다. (코드를 통해 서로 다른 경로 실행 하지만 동일한 외부 인터페이스 및 동작).|일반적인 예상된 동작입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [소스 제어 플러그 인에 대한 테스트 가이드](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)
