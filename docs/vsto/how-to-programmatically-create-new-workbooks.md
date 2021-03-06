---
title: '방법: 프로그래밍 방식으로 새 통합 문서 만들기'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Excel [Office development in Visual Studio], creating workbooks
- workbooks, creating
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 4404541327aa5e42290847784f9faf3b35b51054
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63412454"
---
# <a name="how-to-programmatically-create-new-workbooks"></a>방법: 프로그래밍 방식으로 새 통합 문서 만들기
  프로그래밍 방식으로 통합 문서를 만드는 경우 <xref:Microsoft.Office.Tools.Excel.Workbook> 호스트 항목이 아니라 네이티브 <xref:Microsoft.Office.Interop.Excel.Workbook> 개체입니다.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 VSTO 추가 기능 프로젝트에서 <xref:Microsoft.Office.Interop.Excel.Workbook> 개체에 대한 <xref:Microsoft.Office.Tools.Excel.Workbook> 호스트 항목을 생성할 수 있습니다. 자세한 내용은 [확장 Word 문서 및 Excel 통합 런타임에 VSTO 추가 기능에서](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)합니다.

## <a name="to-create-a-new-workbook"></a>새 통합 문서를 만들려면

1. <xref:Microsoft.Office.Interop.Excel.Workbooks.Add%2A> 컬렉션의 <xref:Microsoft.Office.Interop.Excel.Workbooks> 메서드를 사용합니다.

     [!code-csharp[Trin_VstcoreExcelAutomation#1](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#1)]
     [!code-vb[Trin_VstcoreExcelAutomation#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#1)]

    > [!NOTE]
    > 기본 서식 파일 이외의 서식 파일을 기반으로 하여 통합 문서를 만들 수 있습니다. 사용하려는 서식 파일을 <xref:Microsoft.Office.Interop.Excel.Workbooks.Add%2A> 메서드에 매개 변수로 전달합니다.

## <a name="see-also"></a>참고자료
- [Word 문서 및 런타임에 VSTO 추가 기능에서 Excel 통합 문서 확장](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [런타임에 Office 문서에 컨트롤 추가](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [통합 문서를 사용 하 여 작동 합니다.](../vsto/working-with-workbooks.md)
- [방법: 프로그래밍 방식으로 통합 문서 열기](../vsto/how-to-programmatically-open-workbooks.md)
- [방법: 프로그래밍 방식으로 통합 문서 저장](../vsto/how-to-programmatically-save-workbooks.md)
- [방법: 프로그래밍 방식으로 통합 문서 닫기](../vsto/how-to-programmatically-close-workbooks.md)
- [호스트 항목 및 호스트 컨트롤의 프로그래밍 방식으로 제한 사항](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office 솔루션의 선택적 매개 변수](../vsto/optional-parameters-in-office-solutions.md)
- [호스트 항목 및 호스트 컨트롤 개요](../vsto/host-items-and-host-controls-overview.md)
