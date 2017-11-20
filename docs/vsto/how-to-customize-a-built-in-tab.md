---
title: 'Porady: dostosowywanie wbudowanej karty | Dokumentacja firmy Microsoft'
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
- Ribbon [Office development in Visual Studio], tabs
- built-in tabs [Office development in Visual Studio]
ms.assetid: 197a7aaa-a51d-496c-b904-b9421849fad9
caps.latest.revision: "28"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 1161af5501ebd0df8137293b137600697af91516
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-customize-a-built-in-tab"></a>Porady: dostosowywanie wbudowanej karty
  Możesz dodać grup i kontroli do wbudowanej karty. Tabulator wbudowana jest karta, która jest już na Wstążce aplikacji pakietu Microsoft Office. Na przykład **danych** karta jest wbudowanej karty w programie Excel. Podczas tworzenia niestandardowych grup pojawia się na karcie ostatnich, ale można przenieść tej grupy dowolne miejsce na karcie.  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
> [!NOTE]  
>  Można dodać grupy do wbudowanej karty, ale nie można usunąć wbudowanych grup z wbudowanej karty.  
  
### <a name="to-add-groups-to-a-built-in-tab"></a>Aby dodać grupy do wbudowanej karty  
  
1.  Kliknij prawym przyciskiem myszy plik kodu wstążki w **Eksploratora rozwiązań**, a następnie kliknij przycisk **Widok projektanta**.  
  
    > [!NOTE]  
    >  Jeśli nie ma pliku kodu wstążki **Eksploratora rozwiązań**, należy dodać **element wstążki** do projektu. Zobacz [porady: wprowadzenie do dostosowywania wstążki](../vsto/how-to-get-started-customizing-the-ribbon.md).  
  
2.  Kliknij prawym przyciskiem myszy dowolną kartę w Projektancie wstążki, a następnie kliknij przycisk **właściwości**.  
  
3.  W **właściwości** okna, rozwiń węzeł **ControlId** właściwości, a następnie ustawić **ControlIdType** właściwości **Office**.  
  
4.  Ustaw **OfficeId** właściwości *identyfikator formantu* karty wbudowane, który chcesz dostosować.  
  
     Identyfikator formantu jest to nazwa, który unikatowo identyfikuje kart, grup i kontrolek, które są wbudowane w aplikacji Microsoft Office.  
  
     Lista kontroli identyfikatorów, zobacz [pliki Pomocy pakietu Office 2010: identyfikatory formantu interfejsu użytkownika Office Fluent](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
5.  Z **formantów wstążki pakietu Office** karcie **przybornika**, przeciągnij grupy na karcie.  
  
    > [!NOTE]  
    >  Wbudowane grupy nie są wyświetlane w projektancie. Dlatego jedynym sposobem, aby określić, czy użytkownik korzysta z wbudowanej karty jest zbadanie **ControlId** właściwości karty.  
  
### <a name="to-position-groups-on-a-built-in-tab"></a>Aby umieścić grupy wbudowanej karty  
  
1.  Wybierz grupę niestandardowych w Projektancie wstążki.  
  
2.  W **właściwości** okna, rozwiń węzeł **pozycji** właściwości.  
  
3.  Ustaw **PositionType** odpowiedniej wartości dla właściwości:  
  
    -   **BeforeOfficeId** umieszcza grupy przed określonej grupy wbudowane.  
  
    -   **AfterOfficeId** umieszcza po określonej grupy wbudowane grupy.  
  
4.  Ustaw **OfficeId** właściwość identyfikatora formantu wbudowane grupy.  
  
     Lista kontroli identyfikatorów, zobacz [pliki Pomocy pakietu Office 2010: identyfikatory formantu interfejsu użytkownika Office Fluent](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
## <a name="see-also"></a>Zobacz też  
 [Wstążka ― omówienie](../vsto/ribbon-overview.md)   
 [Projektant wstążki](../vsto/ribbon-designer.md)   
 [XML wstążki](../vsto/ribbon-xml.md)   
 [Wskazówki: Tworzenie kart niestandardowych za pomocą projektanta wstążki](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)   
 [Wskazówki: Tworzenie kart niestandardowych za pomocą XML wstążki](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)   
 [Porady: wprowadzenie do dostosowywania wstążki](../vsto/how-to-get-started-customizing-the-ribbon.md)   
 [Porady: zmiana położenia zakładki na Wstążce](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md)   
 [Porady: dodawanie formantów do widoku Zakulisowego](../vsto/how-to-add-controls-to-the-backstage-view.md)   
 [Porady: Pokaż błędy interfejsu użytkownika dodatku](../vsto/how-to-show-add-in-user-interface-errors.md)  
  
  