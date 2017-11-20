---
title: "Porady: programowane rozszerzanie zakresów w dokumentach | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, extending
- documents [Office development in Visual Studio], extending ranges
ms.assetid: 055af7a4-13d5-4236-b5fb-a112721482c5
caps.latest.revision: "41"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a9ad40c7a4a9e10e6198e2c021ba646f84e50ff9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-programmatically-extend-ranges-in-documents"></a>Porady: Programowane rozszerzanie zakresów w dokumentach
  Po zdefiniowaniu <xref:Microsoft.Office.Interop.Word.Range> obiekt w dokumencie programu Microsoft Office Word, zmienić jego początkowego i końcowego za pomocą <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> i <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> metody. <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> i <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> metody przyjmują te same argumenty dwóch *jednostki* i *liczba*. *Liczba* argument jest liczbę jednostek można przenieść oraz *jednostki* argument może być jedną z następujących <xref:Microsoft.Office.Interop.Word.WdUnits> wartości:  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdCharacter>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdWord>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdSentence>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdParagraph>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdSection>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdStory>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdCell>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdColumn>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdRow>  
  
-   <xref:Microsoft.Office.Interop.Word.WdUnits.wdTable>  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
 W poniższym przykładzie zdefiniowano zakres 7 znaków. Przenosi następnie pozycja początkowa zakresu siedmiu znaków, po oryginalnej pozycja początkowa. Ponieważ pozycja końcowa zakresu został również siedem znaków od pozycji początkowej, wynikiem jest zakres, który zawiera znaki, zero. Kod następnie przejdzie do kolejnych pozycji zakończenia siedem znaków po bieżącym pozycja końcowa.  
  
### <a name="to-extend-a-range"></a>Aby rozszerzyć zakres  
  
1.  Zdefiniuj zakres znaków. Aby uzyskać więcej informacji, zobacz [porady: programowane definiowanie i wybierz zakresów w dokumentach](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md).  
  
     Poniższy przykład kodu może służyć w dostosowaniu poziomie dokumentu.  
  
     [!code-vb[Trin_VstcoreWordAutomation#39](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#39)]
     [!code-csharp[Trin_VstcoreWordAutomation#39](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#39)]  
  
     Poniższy przykład kodu można używać w dodatku VSTO. W tym przykładzie użyto aktywny dokument.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#39](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#39)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#39](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#39)]  
  
2.  Użyj <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> metody <xref:Microsoft.Office.Interop.Word.Range> przesunięcia pozycja początkowa zakresu.  
  
     [!code-vb[Trin_VstcoreWordAutomation#40](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#40)]
     [!code-csharp[Trin_VstcoreWordAutomation#40](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#40)]  
  
3.  Użyj <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> metody <xref:Microsoft.Office.Interop.Word.Range> przesunięcia pozycja końcowa zakresu.  
  
     [!code-vb[Trin_VstcoreWordAutomation#41](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#41)]
     [!code-csharp[Trin_VstcoreWordAutomation#41](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#41)]  
  
## <a name="document-level-customization-code"></a>Kod dostosowania na poziomie dokumentu  
  
#### <a name="to-extend-a-range-in-a-document-level-customization"></a>Aby rozszerzyć zakres dostosowywania poziomie dokumentu  
  
1.  Poniższy przykład przedstawia kompletny kod dla dostosowania poziomie dokumentu. Aby użyć tego kodu, uruchom go z `ThisDocument` klasy w projekcie.  
  
     [!code-vb[Trin_VstcoreWordAutomation#38](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#38)]
     [!code-csharp[Trin_VstcoreWordAutomation#38](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#38)]  
  
## <a name="vsto-add-in-code"></a>Kodu dodatku narzędzi VSTO  
  
#### <a name="to-extend-a-range-in-an-application-level-vsto-add-in"></a>Aby rozszerzyć zakres w dodatku VSTO poziomie aplikacji  
  
1.  Poniższy przykład przedstawia kompletny kod dla dodatku VSTO. Aby użyć tego kodu, uruchom go z `ThisAddIn` klasy w projekcie.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#38](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#38)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#38](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#38)]  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: programowane Resetowanie zakresów w programie Word dokumentów](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md)   
 [Porady: programowane zwijanie zakresów lub zaznaczenia w dokumentach](../vsto/how-to-programmatically-collapse-ranges-or-selections-in-documents.md)   
 [Porady: programowane definiowanie i zaznaczanie zakresów w dokumentach](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)   
 [Porady: programowane pobieranie początkowych i końcowych w zakresach](../vsto/how-to-programmatically-retrieve-start-and-end-characters-in-ranges.md)   
 [Porady: programowane wykluczanie znaczników akapitu podczas tworzenia zakresów](../vsto/how-to-programmatically-exclude-paragraph-marks-when-creating-ranges.md)  
  