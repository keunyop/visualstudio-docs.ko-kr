---
title: '&lt;postActionData&gt; 요소 (Visual Studio에서 Office 개발)'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- <postActionData> element
- application manifests [Office development in Visual Studio], <postActionData> element
- postActionData element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: cda7829fc615c64be75f295a0cbc26b2ebbc7eea
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62561488"
---
# <a name="ltpostactiondatagt-element-office-development-in-visual-studio"></a>&lt;postActionData&gt; 요소 (Visual Studio에서 Office 개발)
  `postActionData` 네임스페이스의 `vstav3` 요소는 Office 솔루션이 설치된 후 실행되는 배포 후 작업과 관련된 데이터를 지정합니다.

## <a name="syntax"></a>구문

```xml
<postActionData>
</postActionData>
```

## <a name="elements-and-attributes"></a>요소 및 특성
 `postActionData` 요소는 선택적이며 `vstav3` 네임스페이스에 있습니다. 하나의 애플리케이션 매니페스트에서는 각 배포 후 작업에 대해 하나의 `postActionData` 요소만 정의할 수 있습니다.

 `postActions` 요소에는 특성이 없습니다.

 `postActions` 에는 자식 요소가 없습니다.

## <a name="post-deployment-action-example"></a>배포 후 작업 예제

### <a name="description"></a>설명
 다음 코드 예제에서는 `postAction` 을 사용하여 배포된 Office 솔루션에 대한 애플리케이션 매니페스트의 [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]요소를 보여 줍니다. 이 코드 예제는에서 제공 하는 더 큰 예제의 일부입니다 [Office 솔루션에 대 한 응용 프로그램 매니페스트](../vsto/application-manifests-for-office-solutions.md)합니다.

### <a name="code"></a>코드

```xml
<vstav3:postActionData>
  data in any format
</vstav3:postActionData>
```

## <a name="see-also"></a>참고 항목

- [Office 솔루션에 대 한 응용 프로그램 매니페스트](../vsto/application-manifests-for-office-solutions.md)
- [Office 솔루션의 배포 매니페스트](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce 애플리케이션 매니페스트](../deployment/clickonce-application-manifest.md)
