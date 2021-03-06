---
title: 'Porady: Dodawanie metody Deleter | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], deleting data
- Business Data Connectivity service [SharePoint development in Visual Studio], Deleter
- BDC [SharePoint development in Visual Studio], Deleter
- BDC [SharePoint development in Visual Studio], removing data
- BDC [SharePoint development in Visual Studio], deleting entity instances
- Business Data Connectivity service [SharePoint development in Visual Studio], deleting entity instances
- Business Data Connectivity service [SharePoint development in Visual Studio], deleting data
- Business Data Connectivity service [SharePoint development in Visual Studio], removing data
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 0bc47da90356149e3fe2e1d1b888bf5ac6a877e5
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49842680"
---
# <a name="how-to-add-a-deleter-method"></a>Porady: Dodawanie metody Deleter
  Aby umożliwić użytkownikowi końcowemu usunąć rekord danych z listy zewnętrznej w witrynie programu SharePoint przez dodawanie metody Deleter do modelu. Aby uzyskać więcej informacji, zobacz [projektowanie modelu łączności danych biznesowych](../sharepoint/designing-a-business-data-connectivity-model.md).  
  
### <a name="to-create-a-deleter-method"></a>Aby utworzyć metody Deleter  
  
1. Na **projektanta łączności danych biznesowych**, wybierz jednostkę.  
  
2. Na pasku menu wybierz **widoku** > **Windows inne** > **szczegóły metody BDC**.  
  
    **Szczegóły metody BDC** zostanie otwarte okno. Aby uzyskać więcej informacji na temat tego okna, zobacz [Omówienie narzędzia projektowania modelu usługi łączności danych biznesowych](../sharepoint/bdc-model-design-tools-overview.md).  
  
3. W **Dodaj metodę** wybierz **Utwórz metodę usuwającą**.  
  
    Visual Studio dodaje następujące elementy w modelu. Te elementy są wyświetlane w **szczegóły metody BDC** okna.  
  
   - Metodę o nazwie **Usuń**.  
  
   - Parametr wejściowy metody.  
  
   - Deskryptor typu parametru.  
  
   - Wystąpienia metody dla metody.  
  
     Aby uzyskać więcej informacji, zobacz [projektowanie modelu łączności danych biznesowych](../sharepoint/designing-a-business-data-connectivity-model.md).  
  
4. W **Eksploratora rozwiązań**, otwórz menu skrótów pliku kodu usługi, który został wygenerowany dla jednostki, a następnie wybierz **Wyświetl kod**.  
  
    Pliku kodu usługi jednostki zostanie otwarty w edytorze kodu. Aby uzyskać więcej informacji na temat pliku kodu usługi jednostki, zobacz [Tworzenie modelu łączności danych biznesowych](../sharepoint/creating-a-business-data-connectivity-model.md).  
  
5. Dodaj kod do metody Deleter, aby usunąć rekord. Poniższy przykład usuwa element wiersza z zamówienia sprzedaży, korzystając z przykładowej bazy danych AdventureWorks programu SQL Server.  
  
   > [!NOTE]  
   >  Metody, w tym przykładzie używa dwóch parametrów wejściowych.  
  
   > [!NOTE]  
   >  Zastąp wartość `ServerName` pole z nazwą serwera.  
  
    [!code-csharp[SP_BDC#6](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/salesorderdetailservice.cs#6)]
    [!code-vb[SP_BDC#6](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/salesorderdetailservice.vb#6)]  
  
## <a name="see-also"></a>Zobacz także
 [Projektowanie modelu łączności danych biznesowych](../sharepoint/designing-a-business-data-connectivity-model.md)   
 [Porady: Dodawanie metody wyszukiwania](../sharepoint/how-to-add-a-finder-method.md)   
 [Porady: Dodawanie określonej metody wyszukiwania](../sharepoint/how-to-add-a-specific-finder-method.md)   
 [Porady: Dodawanie metody Creator](../sharepoint/how-to-add-a-creator-method.md)   
 [Porady: Dodawanie metody Updater](../sharepoint/how-to-add-an-updater-method.md)   
 [Omówienie narzędzi projektowania modelu BDC](../sharepoint/bdc-model-design-tools-overview.md)   
 [Porady: Dodawanie parametru do metody](../sharepoint/how-to-add-a-parameter-to-a-method.md)   
 [Porady: Definiowanie wystąpienia metody](../sharepoint/how-to-define-a-method-instance.md)  
  
  
