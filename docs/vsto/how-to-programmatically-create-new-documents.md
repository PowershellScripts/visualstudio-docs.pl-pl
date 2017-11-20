---
title: "Porady: programowane tworzenie nowych dokumentów | Dokumentacja firmy Microsoft"
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
- templates [Office development in Visual Studio], custom document
- Word [Office development in Visual Studio], creating documents
- documents [Office development in Visual Studio], creating
ms.assetid: c24bb8a3-1303-438e-9b33-ba8b00b29c3b
caps.latest.revision: "49"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b1935b7657e7aad612b855ecd4e9c1c8e222c952
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-programmatically-create-new-documents"></a>Porady: Programowane tworzenie nowych dokumentów
  Po utworzeniu dokumentu programowo, nowy dokument jest natywny <xref:Microsoft.Office.Interop.Word.Document> obiektu. Ten obiekt nie ma dodatkowych zdarzeń i możliwości wiązania danych <xref:Microsoft.Office.Tools.Word.Document> element hosta. Aby uzyskać więcej informacji, zobacz [programowe ograniczenia elementów hosta i formantów hosta](../vsto/programmatic-limitations-of-host-items-and-host-controls.md).  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
 Podczas opracowywania projektu poziomie dokumentu nie można dodać programistycznie <xref:Microsoft.Office.Tools.Word.Document> hosta elementy do projektu. W projekcie dodatku narzędzi VSTO można przekonwertować żadnego <xref:Microsoft.Office.Interop.Word.Document> do obiektu <xref:Microsoft.Office.Tools.Word.Document> element hosta w czasie wykonywania. Aby uzyskać więcej informacji, zobacz [Rozszerzanie dokumentów programu Word i skoroszytów programu Excel w dodatkach VSTO w czasie wykonywania](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).  
  
### <a name="to-create-a-new-document-based-on-the-normal-template"></a>Aby utworzyć nowy dokument na podstawie szablonu normalnej  
  
-   Użyj <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> metody <xref:Microsoft.Office.Interop.Word.Documents> kolekcję, aby utworzyć nowy dokument oparty na szablonie normalnego. Aby użyć w tym przykładzie kodu, uruchom go z `ThisDocument` lub `ThisAddIn` klasy w projekcie.  
  
     [!code-vb[Trin_VstcoreWordAutomation#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#1)]
     [!code-csharp[Trin_VstcoreWordAutomation#1](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#1)]  
  
## <a name="using-custom-templates"></a>Za pomocą szablonów niestandardowych  
 <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> Metoda ma opcjonalny *szablonu* argumentu, aby utworzyć nowy dokument na podstawie szablonu innego niż szablon Normal. Należy podać nazwę pliku i w pełni kwalifikowana szablonu.  
  
#### <a name="to-create-a-new-document-based-on-a-custom-template"></a>Aby utworzyć nowy dokument na podstawie szablonu niestandardowego  
  
-   Wywołanie <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> metody <xref:Microsoft.Office.Interop.Word.Documents> kolekcji i określ ścieżkę do szablonu. Aby użyć w tym przykładzie kodu, uruchom go z `ThisDocument` lub `ThisAddIn` klasy w projekcie.  
  
     [!code-vb[Trin_VstcoreWordAutomation#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#2)]
     [!code-csharp[Trin_VstcoreWordAutomation#2](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#2)]  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: programowane otwieranie istniejących dokumentów](../vsto/how-to-programmatically-open-existing-documents.md)   
 [Obiekty hosta i informacje o formantach hosta](../vsto/host-items-and-host-controls-overview.md)   
 [Ograniczenia programowe elementów hosta i formantów hosta](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)   
 [Parametry opcjonalne w rozwiązaniach pakietu Office](../vsto/optional-parameters-in-office-solutions.md)  
  
  