---
title: 'Porady: programowane Włączanie ochrony skoroszytów'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, passwords
- documents [Office development in Visual Studio], document protection
- workbooks, unprotecting
- document protection, removing from workbooks
- document protection, adding to workbooks
- workbooks, protecting
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 8999bb1e30958897f9b7732ab393650320ec77b1
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/06/2018
ms.locfileid: "35676197"
---
# <a name="how-to-programmatically-protect-workbooks"></a>Porady: programowane Włączanie ochrony skoroszytów
  Może chronić programu Microsoft Office Excel, dzięki czemu użytkownicy nie mogą dodać lub usuwanie arkuszy i również programowe usuwające ochronę skoroszytu. Opcjonalnie można określić hasło, wskazują, czy mają strukturę chronione (dzięki czemu użytkownicy nie można przenieść arkusze) i wskazuje, czy windows skoroszytu chronionego.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
 Ochrona skoroszytu nie uniemożliwia użytkownikom edytowanie komórki. Aby chronić dane, należy włączyć ochronę arkuszy. Aby uzyskać więcej informacji, zobacz [porady: programowane Włączanie ochrony arkuszy](../vsto/how-to-programmatically-protect-worksheets.md).  
  
 Poniższe przykłady kodu użyć zmiennej zawierać hasło, które są uzyskiwane przez użytkownika.  
  
## <a name="protect-a-workbook-that-is-part-of-a-document-level-customization"></a>Chroń skoroszyt, który jest częścią dostosowywania poziomie dokumentu  
  
### <a name="to-protect-a-workbook"></a>Aby chronić skoroszyt  
  
1.  Wywołaj <xref:Microsoft.Office.Tools.Excel.Workbook.Protect%2A> metoda skoroszytu i zawierać hasło. Aby użyć w poniższym przykładzie kodu, należy uruchomić go `ThisWorkbook` klasy, nie w klasie arkusza.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#10](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/ThisWorkbook.cs#10)]
     [!code-vb[Trin_VstcoreExcelAutomation#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/ThisWorkbook.vb#10)]  
  
### <a name="to-unprotect-a-workbook"></a>Aby wyłączyć ochronę skoroszytu  
  
1.  Wywołaj <xref:Microsoft.Office.Tools.Excel.Workbook.Unprotect%2A> metody, przekazując hasła, jeśli jest to wymagane. Aby użyć w poniższym przykładzie kodu, należy uruchomić go `ThisWorkbook` klasy, nie w klasie arkusza.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#11](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/ThisWorkbook.cs#11)]
     [!code-vb[Trin_VstcoreExcelAutomation#11](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/ThisWorkbook.vb#11)]  
  
## <a name="protect-a-workbook-by-using-an-application-level-add-in"></a>Chroń skoroszyt przy użyciu dodatku poziomu aplikacji  
  
### <a name="to-protect-a-workbook"></a>Aby chronić skoroszyt  
  
1.  Wywołaj <xref:Microsoft.Office.Interop.Excel._Workbook.Protect%2A> metoda skoroszytu i zawierać hasło. Ten przykład kodu używa aktywnego skoroszytu. Aby użyć tego przykładu, należy uruchomić kod z `ThisAddIn` klasy w projekcie.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#6](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#6)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#6](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#6)]  
  
### <a name="to-unprotect-a-workbook"></a>Aby wyłączyć ochronę skoroszytu  
  
1.  Wywołaj <xref:Microsoft.Office.Interop.Excel._Workbook.Unprotect%2A> metoda aktywnym skoroszycie, przekazując hasła, jeśli jest to wymagane. Aby użyć tego przykładu, należy uruchomić kod z `ThisAddIn` klasy w projekcie.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#7](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#7)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#7](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#7)]  
  
## <a name="see-also"></a>Zobacz także  
 [Praca ze skoroszytami](../vsto/working-with-workbooks.md)   
 [Porady: programowane Włączanie ochrony arkuszy](../vsto/how-to-programmatically-protect-worksheets.md)   
 [Porady: programowane ukrywanie arkuszy](../vsto/how-to-programmatically-hide-worksheets.md)   
 [Parametry opcjonalne w rozwiązaniach pakietu Office](../vsto/optional-parameters-in-office-solutions.md)  
  
  