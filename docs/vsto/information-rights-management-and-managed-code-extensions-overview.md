---
title: 정보 권한 관리 및 관리 코드 확장명 개요
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Information Rights Management [Office development in Visual Studio]
- workbooks [Office development in Visual Studio], restricted permissions
- IRM [Office development in Visual Studio]
- documents [Office development in Visual Studio], restricted permissions
- rights management [Office development in Visual Studio]
- Office documents [Office development in Visual Studio, restricted permissions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 109f6b85653a842f7c6fc9ce2d2c09b74113bbc7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62583922"
---
# <a name="information-rights-management-and-managed-code-extensions-overview"></a>정보 권한 관리 및 관리 코드 확장명 개요
  Microsoft Office Word 및 Microsoft Office Excel IRM 정보 권한 관리 (), 권한이 없는 사용자가 보거나 중요 한 정보를 변경 되지 않도록 도움이 될 수 있는 기능을 제공 합니다. 정보 권한 관리의 작동 원리에 대 한 자세한 내용은 특정 Office 응용 프로그램에서 도움말을 참조 합니다.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

## <a name="run-code-behind-documents-with-restricted-permissions"></a>제한 된 권한으로 문서의 숨겨진 코드를 실행 합니다.
 솔루션이 들어 문서나 통합 문서는 기본적으로 IRM을 사용 하는 경우 Word 및 Excel을 실행 하는 코드를 허용 하지 않습니다. 문서의 작성자는 권한을 가질 경우 솔루션에서 작동할 수 있도록 기본값을 변경할 수 있습니다. 자세한 내용은 [방법: 제한 된 권한으로 문서 뒤에서 실행 하는 코드를 허용](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md)합니다.

 IRM 사용 하지 못하도록 <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.ServerDocument> 검색 또는 문서에서 캐시 된 데이터를 조작 합니다.

## <a name="end-users-to-restrict-permissions-to-documents-that-use-managed-code-extensions"></a>최종 사용자가 관리 코드 확장을 사용 하는 문서에는 권한을 제한 하려면
 IRM을 사용 솔루션의 문서 또는 통합 문서에 대 한 모든 권한이 있는 사용자는 누구나 권한을 제한할 수 있습니다. 예를 들어, 회계 부서에서 최종 사용자는 데이터베이스의 데이터로 워크시트를 자동으로 채워지는 솔루션에서는 해당 사용자가 자신의 부서의 사용자 에게만 액세스를 변경 하 고 다른 사용자에 대 한 읽기 액세스를 허용 하도록 좋습니다. 사용자는 제한 된 권한을 추가 하면 기본적으로 워크시트의 코드를 실행할 수 없으면 및 워크시트 데이터를 사용 하 여 채워지지 않습니다.

 문제를 해결 하려면 문서 또는 통합 문서에 대 한 모든 권한을 가진 사람이 개체 모델에 대 한 프로그래밍 방식의 액세스를 허용 하도록 기본 사용 권한 설정을 변경 해야 합니다. 자세한 내용은 [방법: 제한 된 권한으로 문서 뒤에서 실행 하는 코드를 허용](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md)합니다.

## <a name="see-also"></a>참고자료
- [문서 수준 솔루션의 문서 보호](../vsto/document-protection-in-document-level-solutions.md)
- [Office 문서의 암호 보호](../vsto/password-protection-on-office-documents.md)
- [Office 솔루션 보안](../vsto/securing-office-solutions.md)
- [Office 솔루션 배포](../vsto/deploying-an-office-solution.md)
- [Office 솔루션을 만들고 디자인](../vsto/designing-and-creating-office-solutions.md)
