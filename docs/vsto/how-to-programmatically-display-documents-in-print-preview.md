---
title: '방법: 프로그래밍 방식으로 인쇄 미리 보기로 문서 표시'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word [Office development in Visual Studio], displaying documents in print preview
- documents [Office development in Visual Studio], displaying in print preview
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d8296d28e884c746e09b427914af02213bbbaa7e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62813038"
---
# <a name="how-to-programmatically-display-documents-in-print-preview"></a>방법: 프로그래밍 방식으로 인쇄 미리 보기로 문서 표시
  솔루션에서 보고서를 생성하는 경우 인쇄 미리 보기 모드로 사용자에게 보고서를 표시하려고 할 수 있습니다.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="procedures-for-document-level-customizations"></a>문서 수준 사용자 지정 하는 절차

### <a name="to-display-a-document-in-print-preview-by-calling-the-printpreview-method"></a>PrintPreview 메서드를 호출하여 인쇄 미리 보기로 문서를 표시하려면

1. <xref:Microsoft.Office.Tools.Word.Document.PrintPreview%2A> 클래스의 <xref:Microsoft.Office.Tools.Word.Document> 메서드를 호출합니다. 이 코드 예제를 사용하려면 프로젝트의 `ThisDocument` 클래스에서 실행합니다.

     [!code-vb[Trin_VstcoreWordAutomation#13](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#13)]
     [!code-csharp[Trin_VstcoreWordAutomation#13](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#13)]

### <a name="to-display-a-document-in-print-preview-by-setting-the-printpreview-property"></a>PrintPreview 속성을 설정하여 인쇄 미리 보기로 문서를 표시하려면

1. 설정 합니다 <xref:Microsoft.Office.Interop.Word._Application.PrintPreview%2A> 의 속성을 <xref:Microsoft.Office.Interop.Word.Application> 개체를 **true**합니다.

     [!code-vb[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#14)]
     [!code-csharp[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#14)]

## <a name="procedures-for-vsto-add-ins"></a>VSTO 추가 기능에 대한 프로시저

### <a name="to-display-a-document-in-print-preview-by-calling-the-printpreview-method"></a>PrintPreview 메서드를 호출하여 인쇄 미리 보기로 문서를 표시하려면

1. 미리 보려는 <xref:Microsoft.Office.Interop.Word._Document.PrintPreview%2A> 의 <xref:Microsoft.Office.Interop.Word.Document> 메서드를 호출합니다. 이 코드 예제를 사용하려면 프로젝트의 `ThisAddIn` 클래스에서 실행합니다.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#13](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#13)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#13](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#13)]

### <a name="to-display-a-document-in-print-preview-by-setting-the-printpreview-property"></a>PrintPreview 속성을 설정하여 인쇄 미리 보기로 문서를 표시하려면

1. 설정 합니다 <xref:Microsoft.Office.Interop.Word._Application.PrintPreview%2A> 의 속성을 <xref:Microsoft.Office.Interop.Word.Application> 개체를 **true**합니다.

     [!code-vb[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#14)]
     [!code-csharp[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#14)]

## <a name="see-also"></a>참고자료
- [방법: 프로그래밍 방식으로 문서 인쇄](../vsto/how-to-programmatically-print-documents.md)
- [방법: 프로그래밍 방식으로 기존 문서 열기](../vsto/how-to-programmatically-open-existing-documents.md)
- [방법: 프로그래밍 방식으로 새 문서 만들기](../vsto/how-to-programmatically-create-new-documents.md)
