---
title: Tworzenie funkcji SharePoint | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, features
- features [SharePoint development in Visual Studio]
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 56bc4dbd50bedc15fcf6c69cbc334fe09c6094cc
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/22/2018
ms.locfileid: "36325602"
---
# <a name="create-sharepoint-features"></a>Tworzenie funkcji SharePoint
  Funkcja programu SharePoint można użyć do grupowania powiązanych SharePoint — elementy projektu wdrożenia łatwiejsze. Można utworzyć funkcji, ustaw zakresy i oznaczyć za pomocą programu SharePoint Designer funkcji innych funkcji jako zależności. Projektant generuje również manifestu, który jest plik XML, który opisuje każdej funkcji.  
  
## <a name="add-features-to-the-sharepoint-solution"></a>Dodawanie funkcji do rozwiązań SharePoint
 Funkcja można dodać do rozwiązania SharePoint przy użyciu Eksploratora rozwiązań lub Eksploratora pakietów. Można użyć jednej z następujących metod można dodać funkcji.  
  
-   W **Eksploratora rozwiązań**, otwórz menu skrótów **funkcji**, a następnie wybierz pozycję **dodawania funkcji**.  
  
-   W **Eksploratora pakietów**, otwórz menu skrótów dla pakietu, a następnie wybierz **dodać funkcję**.  
  
## <a name="using-the-feature-designer"></a>Przy użyciu narzędzia Projektant funkcji
 Rozwiązania programu SharePoint może zawierać jedną lub więcej funkcji programu SharePoint, które są pogrupowane w węźle funkcji w Eksploratorze rozwiązań. Każdej funkcji ma własną **projektanta funkcji** której można dostosować właściwości funkcji. Aby uzyskać więcej informacji, zobacz [porady: dostosowywanie funkcji SharePoint](../sharepoint/how-to-customize-a-sharepoint-feature.md). Aby odróżnić funkcje od siebie nawzajem, można skonfigurować właściwości funkcji, takich jak tytuł, opis, wersji i zakresu.  
  
### <a name="feature-designer-options"></a>Opcje projektanta funkcji
 Po utworzeniu funkcja może używać Projektanta funkcji, aby dostosować go.  
  
 W poniższej tabeli opisano właściwości funkcji, które są wyświetlane w Projektancie funkcji.  
  
|Właściwość|Opis|  
|--------------|-----------------|  
|Tytuł|Opcjonalna. Tytuł domyślny funkcji ma ustawioną wartość *Nazwa rozwiązania* *FeatureName*.|  
|Opis|Opcjonalna. Opis funkcji programu SharePoint.|  
|Zakres|Wymagana. Jeśli funkcja jest tworzona przy użyciu **Eksploratora rozwiązań**, zakres jest domyślnie ustawiany na sieci Web.<br /><br /> -Farmy: Aktywacja funkcji dla całej farmy serwerów.<br /><br /> -Site: Aktywacja funkcji dla wszystkich witryn sieci web w zbiorze witryn.<br /><br /> -Web: Aktywacja funkcji dla określonej witryny sieci web.<br /><br /> -WebApplication: Aktywacja funkcji dla wszystkich witryn sieci web w aplikacji sieci web.|  
|Elementy w rozwiązaniu|Wszystkie elementy programu SharePoint, które mogą zostać dodane do funkcji.|  
|Elementy w funkcji|Elementy projektu programu SharePoint, które zostały dodane do funkcji.|  
  
## <a name="add-and-remove-sharepoint-project-items"></a>Dodawanie i usuwanie elementów projektu SharePoint
 Możesz wybrać elementy projektu programu SharePoint, które chcesz dodać funkcję programu SharePoint do wdrożenia. Użyj **projektanta funkcji** do dodawania i usuwania elementów do funkcji oraz wyświetlić manifestu funkcji. Aby uzyskać więcej informacji, zobacz [porady: Dodawanie i usuwanie elementów do funkcji SharePoint](../sharepoint/how-to-add-and-remove-items-to-sharepoint-features.md).  
  
## <a name="add-feature-dependencies"></a>Dodaj zależności funkcji
 Manifest funkcji można skonfigurować tak, aby serwer programu SharePoint aktywuje niektórych funkcji aktywowania funkcji programu. Na przykład jeśli funkcji programu SharePoint jest zależny od innych funkcji dla funkcji lub danych, serwer programu SharePoint można najpierw spróbuj aktywować żadnych funkcji, które zależy od użytkownika funkcji. Aby uzyskać więcej informacji, zobacz [porady: Dodawanie i usuwanie zależności funkcji](../sharepoint/how-to-add-and-remove-feature-dependencies.md).  
  
## <a name="see-also"></a>Zobacz także
 [Porady: dostosowywanie funkcji SharePoint](../sharepoint/how-to-customize-a-sharepoint-feature.md)   
 [Porady: Dodawanie i usuwanie elementów do funkcji SharePoint](../sharepoint/how-to-add-and-remove-items-to-sharepoint-features.md)   
 [Porady: Dodawanie i usuwanie zależności funkcji](../sharepoint/how-to-add-and-remove-feature-dependencies.md)  
  
  
