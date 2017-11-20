---
title: "Globalny dostęp do obiektów w projektach pakietu Office | Dokumentacja firmy Microsoft"
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
- ThisDocument_Shutdown
- ThisDocument_Startup
- Globals class, object global access
- worksheets [Office development in Visual Studio], global access
- documents [Office development in Visual Studio], global access
- event handlers [Office development in Visual Studio]
- ThisWorkbook_Startup
- application-level addins [Office development in Visual Studio]
- addins [Office development in Visual Studio], events
- workbooks [Office development in Visual Studio], global access
- ThisWorkbook_Shutdown
- document-level customizations [Office development in Visual Studio]
- Startup event
- Shutdown event
- projects [Office development in Visual Studio], global access
- Office documents [Office development in Visual Studio, global access
- ThisAddin_Startup
- events [Office development in Visual Studio]
- ThisAddIn_Shutdown
ms.assetid: f6a7f0ef-75d0-4a9b-9aec-be95ffa26adf
caps.latest.revision: "55"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: c8119ccf0c6715d1c18957fcf8cac92d9872a27e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="global-access-to-objects-in-office-projects"></a>Globalny dostęp do obiektów w projektach pakietu Office
  Podczas tworzenia projektu pakietu Office Visual Studio automatycznie generuje klasę o nazwie `Globals` w projekcie. Można użyć `Globals` klasę, aby uzyskiwać dostęp do wielu elementów innego projektu w czasie wykonywania z dowolnego kodu w projekcie.  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
## <a name="how-to-use-the-globals-class"></a>Sposób użycia klasy globalne  
 `Globals`to statyczny klasa, która przechowuje odwołania do niektórych elementów w projekcie. Za pomocą `Globals` klasy, są dostępne następujące elementy kodu w projekcie w czasie wykonywania:  
  
-   `ThisWorkbook` i `Sheet`  *n*  klas w projekcie skoroszytu lub szablon programu Excel. Dostęp do tych obiektów przy użyciu `Globals.ThisWorkbook` i `Sheet`  *n*  właściwości.  
  
-   `ThisDocument` Klasy w projekcie dokument lub szablon programu Word. Dostęp do obiektu przy użyciu `Globals.ThisDocument` właściwości.  
  
-   `ThisAddIn` Klasy w projekcie dodatku VSTO. Dostęp do obiektu przy użyciu `Globals.ThisAddIn` właściwości.  
  
-   Wszystkie taśmy w projekcie, który można dostosować przy użyciu projektanta wstążki. Dostęp do wstążek przy użyciu `Globals.Ribbons` właściwości. Aby uzyskać więcej informacji, zobacz [podczas uzyskiwania dostępu do wstążki w czasie wykonywania](../vsto/accessing-the-ribbon-at-run-time.md).  
  
-   Wszystkie regiony formularzy programu Outlook w projekcie dodatku narzędzi VSTO programu Outlook. Dostęp do regionów formularzy przy użyciu `Globals.FormRegions` właściwości. Aby uzyskać więcej informacji, zobacz [podczas uzyskiwania dostępu do regionów formularzy w czasie wykonywania](../vsto/accessing-a-form-region-at-run-time.md).  
  
-   Obiekt fabryki, który pozwala na tworzenie formantów Wstążki i udostępniać elementów w czasie wykonywania w projektach przeznaczonych [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] lub [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]. Dostęp do obiektu przy użyciu `Globals.Factory` właściwości. Ten obiekt jest wystąpieniem klasy, która implementuje jednej następujących interfejsów:  
  
    -   <xref:Microsoft.Office.Tools.Factory>  
  
    -   <xref:Microsoft.Office.Tools.Excel.Factory>  
  
    -   <xref:Microsoft.Office.Tools.Outlook.Factory>  
  
    -   <xref:Microsoft.Office.Tools.Word.Factory>  
  
 Na przykład można użyć `Globals.Sheet1` właściwości Wstawianie tekstu do <xref:Microsoft.Office.Tools.Excel.NamedRange> kontrolować na `Sheet1` gdy użytkownik kliknie przycisk w okienku Akcje w projektach na poziomie dokumentu dla programu Excel.  
  
 [!code-vb[Trin_VstcoreProgramming#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/Sheet1.vb#1)]
 [!code-csharp[Trin_VstcoreProgramming#1](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingExcelCS/Sheet1.cs#1)]  
  
## <a name="initializing-the-globals-class"></a>Podczas inicjowania klasy globalne  
 Kod, który próbuje użyć `Globals` klasy przed zainicjowaniem całkowicie dokumentu lub dodatku VSTO może zgłosić wyjątek czasu wykonywania. Na przykład za pomocą `Globals` po deklarowanie zmiennej poziomie klasy mogą się niepowodzeniem, ponieważ `Globals` klasy może nie być zainicjowana z odwołaniami do wszystkich elementów hosta przed utworzeniem wystąpienia jest zadeklarowane obiektu.  
  
> [!NOTE]  
>  `Globals` Klasy nigdy nie został zainicjowany w czasie projektowania, ale formant wystąpienia są tworzone przez projektanta. Oznacza to, że w przypadku utworzenia kontrolki użytkownika, który używa właściwości `Globals` klasy z wewnątrz klasy formantu użytkownika należy czy właściwość zwraca **null** przed próbą użycia zwrócony obiekt.  
  
## <a name="see-also"></a>Zobacz też  
 [Uzyskiwanie dostępu do wstążki w czasie wykonywania](../vsto/accessing-the-ribbon-at-run-time.md)   
 [Uzyskiwanie dostępu do regionów formularzy w czasie wykonywania](../vsto/accessing-a-form-region-at-run-time.md)   
 [Obiekty hosta i informacje o formantach hosta](../vsto/host-items-and-host-controls-overview.md)   
 [Element hosta dokumentu](../vsto/document-host-item.md)   
 [Element hosta skoroszytu](../vsto/workbook-host-item.md)   
 [Element hosta arkusza](../vsto/worksheet-host-item.md)   
 [Pisanie kodu dla rozwiązań pakietu Office](../vsto/writing-code-in-office-solutions.md)  
  
  