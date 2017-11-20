---
title: "Porady: Tworzenie skojarzenia między jednostkami | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: AssociationGroupTool
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], create an assocation
- Business Data Connectivity service [SharePoint development in Visual Studio], associations between entities
- BDC [SharePoint development in Visual Studio], associations between entities
- Business Data Connectivity service [SharePoint development in Visual Studio], create an assocation
- Business Data Connectivity service [SharePoint development in Visual Studio], associate external content types
- Business Data Connectivity service [SharePoint development in Visual Studio], relate entities
- BDC [SharePoint development in Visual Studio], relate entities
- BDC [SharePoint development in Visual Studio], associate external content types
ms.assetid: 0c095df8-1f40-4c4d-9fed-e125a8429724
caps.latest.revision: "17"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 92c8643a87a6226e03e8726910a459168e8b4c5d
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-create-an-association-between-entities"></a>Porady: tworzenie skojarzenia między jednostkami
  Można zdefiniować relacji między obiektami modelu łączności danych biznesowych (BDC) przez utworzenie skojarzenia. Program Visual Studio generuje metod, zapewniających konsumentów modelu z informacji na temat każdego skojarzenia. Te metody mogą być używane przez składniki web Part programu SharePoint, listy lub niestandardowych aplikacji, aby wyświetlić relacji danych w interfejsie użytkownika (UI).  
  
 Można tworzyć dwa typy skojarzeń w Projektancie BDC: obcego skojarzenia opartego na kluczach i skojarzenia bez kluczy obcych. Aby uzyskać więcej informacji, zobacz [tworzenia skojarzenia między jednostkami](../sharepoint/creating-an-association-between-entities.md).  
  
### <a name="to-create-an-association-between-entities"></a>Aby utworzyć skojarzenia między jednostkami  
  
1.  Na **BusinessDataConnectivity** karcie **przybornika**, wybierz **skojarzenia** elementu.  
  
2.  W Projektancie BDC wybierz jednostki źródłowej, a następnie wybierz jednostki docelowej.  
  
     **Edytor skojarzenia** pojawi się.  
  
3.  Aby utworzyć skojarzenie na podstawie klucza obcego, zaznacz **to skojarzenie klucza obcego** pole wyboru.  
  
    1.  W **identyfikator źródła** kolumny **mapowanie identyfikatora** tabeli, wybierz identyfikator obok każdego pasującego deskryptor typu wyświetlany w **pola** kolumny.  
  
         Na przykład w **identyfikator źródła** kolumny wybierz `ContactID` obok `ReadList.salesOrderList.SalesOrderList.SalesOrder.ContactID` deskryptor typu i `ReadItem.salesOrder.SalesOrder.ContactID` deskryptor typu.  
  
4.  Jeśli chcesz utworzyć skojarzenie bez kluczy obcych, wyczyść **to skojarzenie klucza obcego** pole wyboru.  
  
5.  Wybierz **OK** przycisku.  
  
6.  W Projektancie BDC wiersza, który reprezentuje skojarzenie pojawi się między jednostki źródłowej i docelowej jednostki.  
  
     Visual Studio dodaje metodę Navigator skojarzenia klasy usługi obiektu docelowego i Klasa usług jednostki źródłowej. Aby uzyskać więcej informacji o metodach nawigacji skojarzenia, zobacz [obsługiwane operacje](http://go.microsoft.com/fwlink/?LinkId=169286).  
  
7.  W metodzie Navigator skojarzenia jednostki źródłowej Dodaj kod, który zwraca kolekcję obiektów docelowego.  
  
8.  W metodzie Navigator skojarzenie obiektu docelowego Dodaj kod, który zwraca jednostki źródłowej pokrewne.  
  
     Przykłady Navigator skojarzenia metod można znaleźć [tworzenia skojarzenia między jednostkami](../sharepoint/creating-an-association-between-entities.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Tworzenie skojarzenia między jednostkami](../sharepoint/creating-an-association-between-entities.md)   
 [Projektowanie modelu łączności danych biznesowych](../sharepoint/designing-a-business-data-connectivity-model.md)   
 [Porady: Dodawanie metody wyszukiwania](../sharepoint/how-to-add-a-finder-method.md)   
 [Porady: Dodawanie metody wyszukiwania](../sharepoint/how-to-add-a-specific-finder-method.md)   
 [Porady: Dodawanie metody Creator](../sharepoint/how-to-add-a-creator-method.md)   
 [Porady: Dodawanie metody Deleter](../sharepoint/how-to-add-a-deleter-method.md)   
 [Porady: Dodawanie metody Updater](../sharepoint/how-to-add-an-updater-method.md)   
 [Omówienie narzędzi projektowania modelu BDC](../sharepoint/bdc-model-design-tools-overview.md)   
 [Porady: Dodawanie parametru do metody](../sharepoint/how-to-add-a-parameter-to-a-method.md)   
 [Porady: Definiowanie wystąpienia metody](../sharepoint/how-to-define-a-method-instance.md)   
 [Porady: Określanie deskryptora typu parametru](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md)   
 [Wskazówki: Tworzenie listy zewnętrznej w SharePoint za pomocą danych biznesowych](../sharepoint/walkthrough-creating-an-external-list-in-sharepoint-by-using-business-data.md)  
  
  