---
title: "Omówienie narzędzi projektowania modelu BDC | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- VS.SharePointTools.BDC.Method_Details
- VS.SharePointTools.BDC.Explorer
- VS.SharePointTools.BDC.Diagram
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], visual tools
- Business Data Connectivity service [SharePoint development in Visual Studio], visual tools
- Business Data Connectivity service [SharePoint development in Visual Studio], BDC Explorer
- BDC [SharePoint development in Visual Studio], method details
- Business Data Connectivity service [SharePoint development in Visual Studio], designer
- Business Data Connectivity service [SharePoint development in Visual Studio], method details
- BDC [SharePoint development in Visual Studio], BDC Explorer
- BDC [SharePoint development in Visual Studio], designer
ms.assetid: dbd7b746-9e93-4ed4-a546-4a6f17a4725f
caps.latest.revision: "16"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: eaf6871f7ad9316ba2dbdaa8fa29b4810b1d6a3d
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="bdc-model-design-tools-overview"></a>Omówienie narzędzi projektowania modelu BDC
  Można zaprojektować modelu łączności danych biznesowych (BDC) przy użyciu narzędzia Projektant BDC **szczegóły metody usługi łączności danych biznesowych** okno i **Eksplorator modelu BDC**.  
  
 **Eksplorator modelu BDC** umożliwia przeglądanie modelu, wyszukiwanie modelu i zdefiniuj deskryptory typu.  
  
## <a name="bdc-designer"></a>Projektant BDC  
 Projektant BDC umożliwia definiowanie jednostek w modelu oraz wizualnie ułożyć ich relacje ze sobą. Za pomocą projektanta BDC do wykonywania następujących zadań:  
  
-   Dodaj jednostki do modelu.  
  
-   Usuwanie jednostek z modelu.  
  
-   Definiowanie relacji między obiektami.  
  
 Aby otworzyć projektanta usługi łączności danych biznesowych, kliknij dwukrotnie plik modelu w projekcie, lub Otwórz menu skrótów dla pliku modelu, a następnie wybierz pozycję **Otwórz**. Dodawanie jednostki do modelu, przeciągając lub kopiowanie **jednostki** z **przybornika** do projektanta. Aby utworzyć skojarzenie między dwiema jednostkami, wybierz **skojarzenia** kontroli w **przybornika**, wybierz pierwszy jednostki, a następnie wybierz jednostki drugiego.  
  
## <a name="bdc-method-details-window"></a>Okno Szczegóły BDC — metoda  
 Użyj **szczegóły metody usługi łączności danych biznesowych** okno, aby określić parametry wystąpień i filtrować deskryptory metody.  
  
 Mogą szybko generować metod wyszukiwania, określonej metody wyszukiwania, tworzenia, aktualizacji i Deleter **szczegóły metody usługi łączności danych biznesowych** okna. Podczas generowania tych metod, Visual Studio dodaje metadane, takie jak parametry, wystąpienia i deskryptorów typu metody. Można zmodyfikować te metadane do zaspokojenia konkretnego scenariusza.  
  
 Aby otworzyć **szczegóły metody usługi łączności danych biznesowych** okna, na pasku menu wybierz **widoku**, **inne okna**, **szczegóły metody usługi łączności danych biznesowych**.  
  
 Aby wyświetlić metod w **szczegóły metody usługi łączności danych biznesowych** okna, wybierz jednostki w Projektancie usługi łączności danych biznesowych. Metody wybranego obiektu są wyświetlane w **szczegóły metody usługi łączności danych biznesowych** okna. Jeśli nie wybierzesz jednostki w Projektancie BDC **szczegóły metody usługi łączności danych biznesowych** wyświetlane żadne informacje.  
  
 Rozwiń lub Zwiń węzłów w **szczegóły metody usługi łączności danych biznesowych** okno, aby określić parametry, wystąpień i filtrować deskryptorów. Użyj **Eksplorator modelu BDC** do definiowania deskryptory typu.  
  
## <a name="bdc-explorer"></a>Eksplorator modelu BDC  
 **Eksplorator modelu BDC** Wyświetla elementy wchodzące w skład modelu. Aby otworzyć **Eksplorator modelu BDC**, na pasku menu wybierz **widoku**, **inne okna**, **Eksplorator modelu BDC**. Aby przeglądać model, rozwiń węzły w **Eksplorator modelu BDC**. Każdy węzeł reprezentuje element w pliku XML z pliku modelu.  
  
 Wybierz polecenie węzłów w **Eksplorator modelu BDC**, wyświetlania właściwości każdego węzła wybranego w **właściwości** okna. Wiele z tych właściwości odpowiadają atrybutom w pliku modelu. Umożliwia wyszukiwanie modelu przy użyciu pola wyszukiwania w górnej części **Eksplorator modelu BDC**.  
  
> [!NOTE]  
>  **Eksplorator modelu BDC** nie Wyświetla identyfikatory, właściwości niestandardowe, zlokalizowanych ciągów, skojarzenie grupy, działania, deskryptory filtrów, akcji listy kontroli i domyślne wartości parametrów.  
  
### <a name="defining-type-descriptors"></a>Definiowanie deskryptory typów.  
 Użyj **Eksplorator modelu BDC** do definiowania deskryptory typu. Eksplorator modelu BDC umożliwia definiowanie deskryptor typu jeden raz i ponowne użycie tego deskryptora typu w modelu. W tym celu kopiowania deskryptora typu i wkleić go do innych parametrów lub deskryptor typu.  
  
> [!NOTE]  
>  Zmiany w oryginalnym deskryptor typu nie wpływają na kopii tego deskryptor typu.  
  
 Aby uzyskać więcej informacji, zobacz [porady: Określanie deskryptora typu parametru](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: Tworzenie modelu BDC](../sharepoint/how-to-create-a-bdc-model.md)   
 [Porady: Dodawanie jednostki do modelu](../sharepoint/how-to-add-an-entity-to-a-model.md)   
 [Porady: Dodawanie metody wyszukiwania](../sharepoint/how-to-add-a-finder-method.md)   
 [Porady: Dodawanie metody wyszukiwania](../sharepoint/how-to-add-a-specific-finder-method.md)   
 [Porady: Dodawanie metody Creator](../sharepoint/how-to-add-a-creator-method.md)   
 [Porady: Dodawanie metody Deleter](../sharepoint/how-to-add-a-deleter-method.md)   
 [Porady: Dodawanie metody Updater](../sharepoint/how-to-add-an-updater-method.md)   
 [Tworzenie skojarzenia między jednostkami](../sharepoint/creating-an-association-between-entities.md)   
 [Wskazówki: Tworzenie listy zewnętrznej w SharePoint za pomocą danych biznesowych](../sharepoint/walkthrough-creating-an-external-list-in-sharepoint-by-using-business-data.md)   
 [Integrowanie danych biznesowych programu SharePoint](../sharepoint/integrating-business-data-into-sharepoint.md)   
 [Tworzenie modelu łączności danych biznesowych](../sharepoint/creating-a-business-data-connectivity-model.md)   
 [Projektowanie modelu łączności danych biznesowych](../sharepoint/designing-a-business-data-connectivity-model.md)  
  
  