---
title: 'Porady: programowane usuwanie arkuszy ze skoroszytu | Dokumentacja firmy Microsoft'
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
- workbooks, deleting worksheets
- worksheets, deleting
ms.assetid: c5ae99f0-806d-4320-a29c-75ad444fb996
caps.latest.revision: "48"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: efa5c68555fbd9e309335d8c985c4f14f1b07b18
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-programmatically-delete-worksheets-from-workbooks"></a>Porady: Programowane usuwanie arkuszy ze skoroszytu
  Możesz usunąć wszelkie arkusza w skoroszycie. Aby usunąć arkusza, użyj element hosta arkusza lub dostęp do arkusza przy użyciu kolekcji arkuszy skoroszytu.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="using-the-worksheet-host-item"></a>Przy użyciu element hosta arkusza  
 Jeśli arkusz został dodany w czasie projektowania w dostosowaniu poziomie dokumentu, użyj <xref:Microsoft.Office.Tools.Excel.Worksheet.Delete%2A> metodę, aby usunąć określony arkusza. Następujący kod usuwa arkusz ze skoroszytu, umieszczając odwołanie do element hosta arkusza bezpośrednio.  
  
> [!IMPORTANT]  
>  Ten kod zadziała tylko w przypadku projektów utworzonych za pomocą dowolnej z następujących szablonów projektu:  
>   
>  -   Skoroszyt programu Excel 2013  
> -   Szablon programu Excel 2013  
> -   Skoroszyt programu Excel 2010  
> -   Szablon programu Excel 2010  
>   
>  Jeśli chcesz wykonać tego zadania w żadnym innym typem projektu, należy dodać odwołanie do **Microsoft.Office.Interop.Excel** zestawu, a następnie użyć klasy z tego zestawu Otwórz skoroszyt i usuwanie arkusza. Aby uzyskać więcej informacji, zobacz [porady: docelowy Office aplikacji za pośrednictwem podstawowe zestawy międzyoperacyjne](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md) i [odwołanie do programu Excel 2010 podstawowy Interop zestawu](http://go.microsoft.com/fwlink/?LinkId=189585).  
  
#### <a name="to-delete-a-worksheet-by-using-a-worksheet-host-item"></a>Aby usunąć arkuszu za pomocą element hosta arkusza  
  
1.  Wywołanie <xref:Microsoft.Office.Tools.Excel.Worksheet.Delete%2A> metody `Sheet1`.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#17](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#17)]
     [!code-vb[Trin_VstcoreExcelAutomation#17](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#17)]  
  
## <a name="using-the-sheets-collection-of-the-excel-workbook"></a>Przy użyciu kolekcji arkuszy skoroszytu programu Excel  
 Dostęp do arkuszy za pomocą programu Microsoft Office Excel <xref:Microsoft.Office.Interop.Excel.Sheets> kolekcji w następujących przypadkach:  
  
-   Chcesz usunąć arkusza w dodatku VSTO.  
  
-   Arkusz, który chcesz usunąć został utworzony w czasie wykonywania w dostosowaniu poziomie dokumentu.  
  
 Poniższy kod usuwa arkusz ze skoroszytu, umieszczając odwołanie do arkusza za pośrednictwem numer indeksu **arkusze** kolekcji. Ten kod zakłada nowego arkusza zostało utworzone programowo.  
  
> [!IMPORTANT]  
>  Jeśli chcesz wykonać tego zadania w żadnym innym typem projektu, należy dodać odwołanie do **Microsoft.Office.Interop.Excel** zestawu, a następnie użyć klasy z tego zestawu Otwórz skoroszyt i usuwanie arkusza. Aby uzyskać więcej informacji, zobacz [porady: docelowy Office aplikacji za pośrednictwem podstawowe zestawy międzyoperacyjne](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md) i [odwołanie do programu Excel 2010 podstawowy Interop zestawu](http://go.microsoft.com/fwlink/?LinkId=189585).  
  
#### <a name="to-delete-a-worksheet-by-using-the-sheets-collection-of-the-excel-workbook"></a>Aby usunąć arkuszu za pomocą kolekcji arkuszy skoroszytu programu Excel  
  
1.  Wywołanie <xref:Microsoft.Office.Interop.Excel._Worksheet.Delete%2A> metody <xref:Microsoft.Office.Interop.Excel.Sheets> kolekcji.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#18](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#18)]
     [!code-vb[Trin_VstcoreExcelAutomation#18](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#18)]  
  
## <a name="see-also"></a>Zobacz też  
 [Praca z arkuszami](../vsto/working-with-worksheets.md)   
 [Porady: programowane ukrywanie arkuszy](../vsto/how-to-programmatically-hide-worksheets.md)   
 [Porady: programowane przenoszenie arkuszy w obrębie skoroszytu](../vsto/how-to-programmatically-move-worksheets-within-workbooks.md)   
 [Porady: programowane Zaznaczanie arkuszy](../vsto/how-to-programmatically-select-worksheets.md)   
 [Porady: programowane Dodawanie nowych arkuszy ze skoroszytami](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md)   
 [Element hosta arkusza](../vsto/worksheet-host-item.md)   
 [Globalny dostęp do obiektów w projektach pakietu Office](../vsto/global-access-to-objects-in-office-projects.md)   
 [Ograniczenia programowe elementów hosta i formantów hosta](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)  
  
  