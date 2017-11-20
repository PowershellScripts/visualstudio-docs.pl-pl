---
title: "PowerPoint — rozwiązania | Dokumentacja firmy Microsoft"
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
- Office solutions [Office development in Visual Studio], PowerPoint
- templates [Office development in Visual Studio], PowerPoint
- solutions [Office development in Visual Studio], PowerPoint
- projects [Office development in Visual Studio], PowerPoint
- PowerPoint [Office development in Visual Studio]
- Office projects [Office development in Visual Studio], PowerPoint
ms.assetid: 02ebad64-9fd3-495f-ab27-4f6206b3d6d2
caps.latest.revision: "46"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: de978f92a5c410312cac00034006cd698b1c5cea
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="powerpoint-solutions"></a>PowerPoint — Rozwiązania
  Program Visual Studio udostępnia szablony projektów, które umożliwia tworzenie dodatków narzędzi VSTO dla programu Microsoft Office PowerPoint. Dodatków VSTO służy do automatyzacji programu PowerPoint, rozszerzenie funkcji programu PowerPoint lub dostosowanie interfejsu użytkownika (UI) programu PowerPoint.  
  
 Aby uzyskać więcej informacji na temat dodatków VSTO, zobacz [pobierania VSTO pracy programowania dodatków](../vsto/getting-started-programming-vsto-add-ins.md) i [architektura VSTO Add-ins](../vsto/architecture-of-vsto-add-ins.md). Jeśli jesteś nowym użytkownikiem programowania w języku Microsoft Office, zobacz [wprowadzenie &#40; programowanie Office w Visual Studio &#41;](../vsto/getting-started-office-development-in-visual-studio.md).  
  
 [!INCLUDE[appliesto_pptallapp](../vsto/includes/appliesto-pptallapp-md.md)]  
  
> [!NOTE]  
>  Pytań dotyczących projektowania rozwiązań, które rozszerzają możliwości pakietu Office przez [wielu platform](https://dev.office.com/add-in-availability)? Zapoznaj się z nowym [modelu dodatków pakietu Office](https://dev.office.com/docs/add-ins/overview/office-add-ins). Dodatków pakietu Office mieć niewielkie rozmiary w porównaniu do dodatków VSTO i rozwiązań i można ich tworzyć przy użyciu prawie każdego technologii, takich jak HTML5, CSS3, JavaScript i XML programowanie dla sieci web.  
  
 ![łącze do wideo](../vsto/media/playvideo.gif "łącze do wideo") dla powiązanych pokaz wideo, zobacz [jak: utworzyć dodatku dla programu Microsoft PowerPoint?](http://go.microsoft.com/fwlink/?LinkId=132767).  
  
## <a name="automating-powerpoint-by-using-the-powerpoint-object-model"></a>Automatyzowanie programu PowerPoint za pomocą modelu obiektów programu PowerPoint  
 Model obiektów programu PowerPoint udostępnia wiele typów, które służą do automatyzacji programu PowerPoint. Te typy umożliwiają napisać kod, aby wykonać typowe zadania:  
  
-   Programowo utworzenia i sformatowania prezentacji.  
  
-   Dodawanie lub usuwanie slajdów z prezentacji.  
  
-   Dodawanie lub zmienianie kształtów na slajdzie.  
  
 Aby uzyskać dostęp do modelu obiektów programu PowerPoint z dodatku VSTO, użyj `Application` pole `ThisAddIn` klasy w projekcie. `Application` Pola zwraca <xref:Microsoft.Office.Interop.PowerPoint.Application> obiekt reprezentujący bieżące wystąpienie programu PowerPoint. Aby uzyskać więcej informacji, zobacz [programowania VSTO Add-Ins](../vsto/programming-vsto-add-ins.md).  
  
 Po wywołują modelu obiektów programu PowerPoint, należy użyć typów, które zostały opublikowane w podstawowego zestawu międzyoperacyjnego dla programu PowerPoint. Podstawowy zestaw międzyoperacyjny działa jako mostka między kodu zarządzanego w dodatku VSTO i model obiektów COM w programie PowerPoint. Wszystkie typy w programie PowerPoint podstawowy zestaw międzyoperacyjny są zdefiniowane w <xref:Microsoft.Office.Interop.PowerPoint> przestrzeni nazw. Aby uzyskać więcej informacji na temat podstawowe zestawy międzyoperacyjne zobacz [rozwój rozwiązań Office ― omówienie &#40; VSTO &#41; ](../vsto/office-solutions-development-overview-vsto.md) i [podstawowe zestawy międzyoperacyjne pakietu Office](../vsto/office-primary-interop-assemblies.md).  
  
##  <a name="WordOMDocumentation"></a>Korzystając z dokumentacji modelu obiektów programu PowerPoint  
 Aby uzyskać pełne informacje o modelu obiektów programu PowerPoint mogą odwoływać się do programu PowerPoint odwołania podstawowego zestawu międzyoperacyjnego (PIA) i odwołania do modelu obiektu języka VBA.  
  
### <a name="primary-interop-assembly-reference"></a>Odwołanie do podstawowego zestawu międzyoperacyjnego  
 Dokumentacja odwołania PowerPoint PIA opisano typy w podstawowego zestawu międzyoperacyjnego dla programu PowerPoint. Niniejsza dokumentacja jest dostępna z następującej lokalizacji: [odwołania zestawu Interop PowerPoint 2010 podstawowy](http://go.microsoft.com/fwlink/?LinkId=189588).  
  
 Aby uzyskać więcej informacji dotyczących projektu PIA PowerPoint, takie jak różnice między klasy i interfejsy PIA i implementowania zdarzeń w PIA, zobacz [Przegląd klasy i interfejsy w podstawowe zestawy międzyoperacyjne pakietu Office ](http://go.microsoft.com/fwlink/?LinkId=199885).  
  
### <a name="vba-object-model-reference"></a>Odwołania do modelu obiektu VBA  
 Odwołania do modelu obiektu VBA dokumentów modelu obiektów programu PowerPoint, jak jest narażony na język Visual Basic dla kodu aplikacji (VBA). Aby uzyskać więcej informacji, zobacz [odwołania do modelu obiektu programu PowerPoint 2010](http://go.microsoft.com/fwlink/?LinkId=199770)  
  
 Wszystkie obiekty i elementów członkowskich w odwołania do modelu obiektu VBA odpowiadają typy i składniki w podstawowy zestaw międzyoperacyjny PowerPoint (PIA). Na przykład obiekt prezentacji odwołania do modelu obiektu VBA odpowiada <xref:Microsoft.Office.Interop.PowerPoint.Presentation> typu w PIA programu PowerPoint. Odwołania do modelu obiektu VBA zapewnia przykłady kodu dla większości właściwości, metod i zdarzeń, jednak należy translacji kod VBA w niniejszej dokumentacji Visual Basic lub Visual C#, jeśli chcesz używać ich w projekcie dodatku VSTO dla programu PowerPoint, który utworzono przy użyciu Program Visual Studio.  
  
## <a name="customizing-the-user-interface-of-powerpoint"></a>Dostosowywanie interfejsu użytkownika programu PowerPoint  
 Interfejs użytkownika programu PowerPoint można zmodyfikować w następujący sposób.  
  
|Zadanie|Więcej informacji|  
|----------|--------------------------|  
|Tworzenie niestandardowego okienka zadań.|[Niestandardowe okienka zadań](../vsto/custom-task-panes.md)|  
|Dodaj niestandardowe karty do wstążki.|[Wstążka ― omówienie](../vsto/ribbon-overview.md)|  
|Dodawanie niestandardowych grup wbudowanych kartę na Wstążce.|[Porady: dostosowywanie wbudowanej karty](../vsto/how-to-customize-a-built-in-tab.md)|  
  
 Aby uzyskać więcej informacji dotyczących dostosowywania interfejsu użytkownika programu PowerPoint i inne aplikacje Microsoft Office, zobacz [dostosowywania interfejsu użytkownika pakietu Office](../vsto/office-ui-customization.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Wskazówki: Tworzenie Twojego pierwszego dodatku narzędzi VSTO dla programu PowerPoint](../vsto/walkthrough-creating-your-first-vsto-add-in-for-powerpoint.md)   
 [Wprowadzenie do programowania dodatków narzędzi VSTO](../vsto/getting-started-programming-vsto-add-ins.md)   
 [Rozwój rozwiązań Office ― omówienie &#40; VSTO &#41;](../vsto/office-solutions-development-overview-vsto.md)   
 [Architektura dodatków narzędzi VSTO](../vsto/architecture-of-vsto-add-ins.md)   
 [Porady: tworzenie projektów Office w Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [Programowanie dodatków VSTO](../vsto/programming-vsto-add-ins.md)   
 [Pisanie kodu dla rozwiązań pakietu Office](../vsto/writing-code-in-office-solutions.md)   
 [Podstawowe zestawy międzyoperacyjne pakietu Office](../vsto/office-primary-interop-assemblies.md)   
 [Dostosowywanie interfejsu użytkownika pakietu Office](../vsto/office-ui-customization.md)   
 [PowerPoint 2010 w programowanie Office](http://go.microsoft.com/fwlink/?LinkId=199015)  
  
  