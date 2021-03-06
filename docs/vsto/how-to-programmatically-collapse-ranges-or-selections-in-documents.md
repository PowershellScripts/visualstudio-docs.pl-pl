---
title: 'Porady: programowane zwijanie zakresów lub zaznaczenia w dokumentach'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- selections, collapsing
- documents [Office development in Visual Studio], collapsing ranges
- collapsing selections
- ranges, collapsing
- collapsing ranges
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: fee3c821c0b6a39c8dfb499caa00355aa008d413
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49906731"
---
# <a name="how-to-programmatically-collapse-ranges-or-selections-in-documents"></a>Porady: programowane zwijanie zakresów lub zaznaczenia w dokumentach
  Jeśli pracujesz z <xref:Microsoft.Office.Interop.Word.Range> lub <xref:Microsoft.Office.Interop.Word.Selection> obiektu, możesz chcieć zmienić zaznaczenie do punktu wstawiania przed Wstawianie tekstu, aby uniknąć, zastępując istniejący tekst. Zarówno <xref:Microsoft.Office.Interop.Word.Range> i <xref:Microsoft.Office.Interop.Word.Selection> obiekty mają metody Zwiń, co sprawia, że użycie <xref:Microsoft.Office.Interop.Word.WdCollapseDirection> wartości wyliczenia:  
  
- <xref:Microsoft.Office.Interop.Word.WdCollapseDirection.wdCollapseStart> Zwija zaznaczenie do początku zaznaczenia. Jest to opcja domyślna, jeśli nie określisz wartości wyliczenia.  
  
- <xref:Microsoft.Office.Interop.Word.WdCollapseDirection.wdCollapseEnd> Zwija zaznaczenie do końca zaznaczenia.  
  
  [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="to-collapse-a-range-and-insert-new-text"></a>Aby zwinąć zakresu i Wstaw nowy tekst  
  
1. Utwórz <xref:Microsoft.Office.Interop.Word.Range> obiekt, który składa się z pierwszym akapit w dokumencie.  
  
    Poniższy przykład kodu może służyć w dostosowaniu na poziomie dokumentu.  
  
    [!code-vb[Trin_VstcoreWordAutomation#46](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#46)]
    [!code-csharp[Trin_VstcoreWordAutomation#46](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#46)]  
  
    Poniższy przykład kodu może służyć w dodatku VSTO. Ten kod używa aktywnego dokumentu.  
  
    [!code-vb[Trin_VstcoreWordAutomationAddIn#46](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#46)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#46](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#46)]  
  
2. Użyj <xref:Microsoft.Office.Interop.Word.WdCollapseDirection.wdCollapseStart> wartości wyliczenia, aby zwinąć zakresu.  
  
    [!code-vb[Trin_VstcoreWordAutomation#47](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#47)]
    [!code-csharp[Trin_VstcoreWordAutomation#47](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#47)]  
  
3. Wstaw nowy tekst.  
  
    [!code-vb[Trin_VstcoreWordAutomation#48](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#48)]
    [!code-csharp[Trin_VstcoreWordAutomation#48](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#48)]  
  
4. Wybierz <xref:Microsoft.Office.Interop.Word.Range>.  
  
    [!code-vb[Trin_VstcoreWordAutomation#49](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#49)]
    [!code-csharp[Trin_VstcoreWordAutomation#49](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#49)]  
  
   Jeśli używasz <xref:Microsoft.Office.Interop.Word.WdCollapseDirection.wdCollapseEnd> wartości wyliczenia, tekst zostanie wstawiony na początku następujący akapit.  
  
   [!code-vb[Trin_VstcoreWordAutomation#50](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#50)]
   [!code-csharp[Trin_VstcoreWordAutomation#50](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#50)]  
  
   Można by oczekiwać, że wstawianie nowych zdania będzie włóż go przed znaczników akapitu, ale oznacza to inaczej, ponieważ oryginalny zakres zawiera znacznik akapitu. Aby uzyskać więcej informacji, zobacz [porady: programowane wykluczanie znaczników akapitu podczas tworzenia zakresów](../vsto/how-to-programmatically-exclude-paragraph-marks-when-creating-ranges.md).  
  
## <a name="document-level-customization-example"></a>Przykład dostosowania na poziomie dokumentu  
  
### <a name="to-collapse-a-range-in-a-document-level-customization"></a>Aby zwinąć zakresu w dostosowaniu na poziomie dokumentu  
  
1.  Poniższy przykład pokazuje całą metodę dla dostosowywania poziomie dokumentu. Aby użyć tego kodu, należy uruchomić go z `ThisDocument` klasy w projekcie.  
  
     [!code-vb[Trin_VstcoreWordAutomation#45](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#45)]
     [!code-csharp[Trin_VstcoreWordAutomation#45](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#45)]  
  
## <a name="vsto-add-in-example"></a>Przykładu dodatku narzędzi VSTO  
  
### <a name="to-collapse-a-range-in-a-vsto-add-in"></a>Aby zwinąć zakresu w dodatku narzędzi VSTO  
  
1.  Poniższy przykład pokazuje całą metodę dla dodatku VSTO. Aby użyć tego kodu, należy uruchomić go z `ThisAddIn` klasy w projekcie.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#45](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#45)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#45](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#45)]  
  
## <a name="see-also"></a>Zobacz także  
 [Porady: programowane Wstawianie tekstu w dokumentach programu Word](../vsto/how-to-programmatically-insert-text-into-word-documents.md)   
 [Porady: programowane definiowanie i zaznaczanie zakresów w dokumentach](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)   
 [Porady: programowane pobieranie znaków początkowych i końcowych w zakresach](../vsto/how-to-programmatically-retrieve-start-and-end-characters-in-ranges.md)   
 [Porady: programowane wykluczanie znaczników akapitu podczas tworzenia zakresów](../vsto/how-to-programmatically-exclude-paragraph-marks-when-creating-ranges.md)   
 [Porady: programowane rozszerzanie zakresów w dokumentach](../vsto/how-to-programmatically-extend-ranges-in-documents.md)   
 [Porady: programowane Resetowanie zakresów w dokumentach programu Word](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md)  
  