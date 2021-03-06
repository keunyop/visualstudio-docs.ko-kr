---
title: '방법: Deleter 메서드 추가 | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], deleting data
- Business Data Connectivity service [SharePoint development in Visual Studio], Deleter
- BDC [SharePoint development in Visual Studio], Deleter
- BDC [SharePoint development in Visual Studio], removing data
- BDC [SharePoint development in Visual Studio], deleting entity instances
- Business Data Connectivity service [SharePoint development in Visual Studio], deleting entity instances
- Business Data Connectivity service [SharePoint development in Visual Studio], deleting data
- Business Data Connectivity service [SharePoint development in Visual Studio], removing data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c9d005ef8bade9f83027c216d875d24aad602449
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63418344"
---
# <a name="how-to-add-a-deleter-method"></a>방법: Deleter 메서드 추가
  최종 사용자가 SharePoint 사이트에서 외부 목록에서 모델을 Deleter 메서드를 추가 하 여 데이터 레코드를 삭제할 수 있습니다. 자세한 내용은 [비즈니스 데이터 연결 모델 디자인](../sharepoint/designing-a-business-data-connectivity-model.md)합니다.

### <a name="to-create-a-deleter-method"></a>Deleter 메서드를 만들려면

1. 에 **BDC 디자이너**, 엔터티를 선택 합니다.

2. 메뉴 모음에서 선택 **뷰** > **기타 Windows** > **BDC 메서드 세부 정보**합니다.

    합니다 **BDC 메서드 세부 정보** 창이 열립니다. 이 창에 대 한 자세한 내용은 참조 하세요. [BDC 모델 디자인 도구 개요](../sharepoint/bdc-model-design-tools-overview.md)합니다.

3. 에 **메서드를 추가** 목록에서 선택 **Deleter 메서드 만들기**합니다.

    Visual Studio 모델에는 다음 요소를 추가합니다. 이러한 요소에 표시 된 **BDC 메서드 세부 정보** 창입니다.

   - 메서드가 **삭제**합니다.

   - 메서드에 대 한 입력된 매개 변수입니다.

   - 매개 변수의 형식 설명자입니다.

   - 메서드에 대 한 메서드 인스턴스입니다.

     자세한 내용은 [비즈니스 데이터 연결 모델 디자인](../sharepoint/designing-a-business-data-connectivity-model.md)합니다.

4. **솔루션 탐색기**, 엔터티에 대해 생성 된 서비스 코드 파일의 바로 가기 메뉴를 열고 선택한 후 **코드 보기**합니다.

    엔터티 서비스 코드 파일이 코드 편집기에서 열립니다. 엔터티 서비스 코드 파일에 대 한 자세한 내용은 참조 하세요. [비즈니스 데이터 연결 모델 만들기](../sharepoint/creating-a-business-data-connectivity-model.md)합니다.

5. 코드는 레코드를 삭제 하는 Deleter 메서드를 추가 합니다. 다음 예제에서는 SQL Server에 대 한 AdventureWorks 예제 데이터베이스를 사용 하 여 판매 주문에서 줄 항목을 삭제 합니다.

   > [!NOTE]
   > 이 예제에서 메서드는 두 개의 입력된 매개 변수를 사용합니다.

   > [!NOTE]
   > 값을 `ServerName` 필드 서버의 이름입니다.

    [!code-csharp[SP_BDC#6](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/salesorderdetailservice.cs#6)]
    [!code-vb[SP_BDC#6](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/salesorderdetailservice.vb#6)]

## <a name="see-also"></a>참고자료
- [비즈니스 데이터 연결 모델 디자인](../sharepoint/designing-a-business-data-connectivity-model.md)
- [방법: Finder 메서드 추가](../sharepoint/how-to-add-a-finder-method.md)
- [방법: 특정 Finder 메서드 추가](../sharepoint/how-to-add-a-specific-finder-method.md)
- [방법: Creator 메서드 추가](../sharepoint/how-to-add-a-creator-method.md)
- [방법: Updater 메서드 추가](../sharepoint/how-to-add-an-updater-method.md)
- [BDC 모델 디자인 도구 개요](../sharepoint/bdc-model-design-tools-overview.md)
- [방법: 메서드에 매개 변수를 추가 합니다.](../sharepoint/how-to-add-a-parameter-to-a-method.md)
- [방법: 메서드 인스턴스 정의](../sharepoint/how-to-define-a-method-instance.md)
