---
title: "Porady: Dołączanie niestandardowego zestawu w funkcji BDC | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: VS.SharePointTools.BDC.Add_Assemblies_Dialog
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], add reference
- Business Data Connectivity service [SharePoint development in Visual Studio], custom assembly
- BDC [SharePoint development in Visual Studio], custom assembly
- BDC [SharePoint development in Visual Studio], add reference
ms.assetid: 2ddf44b9-5f51-4bca-b8bb-94c4bbd1c5f3
caps.latest.revision: "17"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: c5916da8b7aa5018824ffe8040e7184fe6d1bf31
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-include-a-custom-assembly-in-a-bdc-feature"></a>Porady: dołączanie niestandardowego zestawu w funkcji BDC
  Projekt można odwołuje się do zestawów z innych projektów w tym samym rozwiązaniu. Jednak należy dodać te zestawy do pliku funkcji projektu za pomocą **Przypisz odwołania do zestawów do LobSystems** okno dialogowe.  
  
### <a name="to-include-a-custom-assembly-in-a-business-data-connectivity-bdc-feature"></a>Aby Dołączanie niestandardowego zestawu w funkcji łączności danych biznesowych (BDC)  
  
1.  W **Eksploratora rozwiązań**, wybierz folder, który zawiera model usługi łączności danych biznesowych.  
  
2.  Na **widoku** menu, kliknij przycisk **okna właściwości**.  
  
3.  W **właściwości** okna, wybierz **zestawy** właściwości, a następnie przycisk wielokropka (![elipsy ASP.NET Mobile Designer](../sharepoint/media/mwellipsis.gif "ASP.NET Mobile Projektant elipsy")).  
  
     **Przypisz odwołania do zestawów do LobSystems** zostanie wyświetlone okno dialogowe.  
  
4.  W **wybierz zestaw** wybierz zestaw niestandardowy.  
  
    > [!NOTE]  
    >  Zestawy są wyświetlane tylko w **Przypisz odwołania do zestawów do LobSystems** okno dialogowe, jeśli dodano odwołanie do projektu, który zawiera zestaw. Aby uzyskać więcej informacji, zobacz [porady: Dodawanie lub usuwanie odwołań za pomocą okna dialogowego Dodaj odwołanie](http://msdn.microsoft.com/en-us/3bd75d61-f00c-47c0-86a2-dd1f20e231c9).  
  
5.  W **właściwości odwołania** grupy, Otwórz listę, które pojawiają się **zakresu LOB** właściwości, wybierz System LOB z metod, które używać niestandardowego zestawu, a następnie wybierz pozycję **OK**  przycisku.  
  
    > [!NOTE]  
    >  Aby debugować kod w zestawie niestandardowe, należy dodać zestaw do pakietu rozwiązania. Aby uzyskać więcej informacji, zobacz [porady: Dodawanie i usuwanie zestawów dodatkowych](../sharepoint/how-to-add-and-remove-additional-assemblies.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: Korzystanie z pliku zasobu do określania zlokalizowanych nazw, właściwości i uprawnień](../sharepoint/how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions.md)   
 [Porady: Dodawanie istniejącego modelu BDC do projektu SharePoint](../sharepoint/how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project.md)   
 [Tworzenie modelu łączności danych biznesowych](../sharepoint/creating-a-business-data-connectivity-model.md)   
 [Porady: Tworzenie modelu BDC](../sharepoint/how-to-create-a-bdc-model.md)   
 [Integrowanie danych biznesowych programu SharePoint](../sharepoint/integrating-business-data-into-sharepoint.md)  
  
  