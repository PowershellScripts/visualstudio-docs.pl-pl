---
title: Tworzenie modelu łączności danych biznesowych | Dokumentacja firmy Microsoft
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
- Business Data Connectivity service [SharePoint development in Visual Studio], model
- BDC [SharePoint development in Visual Studio], creating a model
- Business Data Connectivity service [SharePoint development in Visual Studio], creating a model
- SharePoint development in Visual Studio, Business Data Connectivity service
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: b8d76c6f7d28b990d133780c25577cab4e8c3cad
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/22/2018
ms.locfileid: "36326037"
---
# <a name="create-a-business-data-connectivity-model"></a>Tworzenie modelu łączności danych biznesowych
  Można utworzyć model łączności danych biznesowych (BDC) lub dostosować istniejący model BDC przy użyciu programu Visual Studio. Każdy projekt programu SharePoint może zawierać tylko jeden model. Aby uzyskać więcej informacji, zobacz [Integrowanie danych biznesowych programu SharePoint](../sharepoint/integrating-business-data-into-sharepoint.md). 
  
## <a name="create-a-new-model"></a>Utwórz nowy model
 Aby utworzyć nowy model, utwórz projekt **modelu łączności danych biznesowych** lub dodaj element **model łączności danych biznesowych** do **pustego projektu SharePoint**. 
  
> [!NOTE]  
>  Musi mieć [!INCLUDE[moss_14_long](../sharepoint/includes/moss-14-long-md.md)] zainstalowany na tym komputerze.  
  
 Visual Studio dodaje folder do projektu. Ten folder ma nazwę, którą określisz dla **modelu łączności danych biznesowych** elementu **Dodaj nowy element** okno dialogowe. Jeśli tworzysz nową **modelu łączności danych biznesowych** projektu programu Visual Studio nazwy folderu **BdcModel1**.  
  
 Visual Studio dodaje następujące pliki do nowego folderu:  
  
|Plik|Opis|  
|----------|-----------------|  
|Plik definicji modelu|Zawiera kod XML, który definiuje jednostek, metod obiektów systemowych Linia biznesowych (LOB) i innych metadanych, które opisują modelu.<br /><br /> Modyfikowanie metadanych w tym pliku przy użyciu narzędzia Projektant BDC **Eksplorator modelu BDC**, **szczegóły metody usługi łączności danych biznesowych** okno i **właściwości** okna.|  
|Plik kodu usługi jednostki|Zawiera metody stanowiące pobrać, aktualizowanie i usuwanie wystąpienia jednostki domyślnej.|  
  
 Aby zdefiniować właściwości jednostki, Edytuj plik kodu jednostki. Aby uzyskać więcej informacji, zobacz [porady: Dodawanie jednostki do modelu](../sharepoint/how-to-add-an-entity-to-a-model.md).  
  
 Aby pobrać, zaktualizować lub usunąć wystąpienia jednostki, należy dodać kod do pliku kodu usługi jednostki. Aby uzyskać więcej informacji, zobacz [Projektowanie modelu łączności danych biznesowych](../sharepoint/designing-a-business-data-connectivity-model.md). 
  
 Podczas kompilowania projektu program Visual Studio tworzy zestaw. Upewnij się, czy do projektu nie dodano innych elementów, które dodają kod do zestawu projektu (na przykład: elementu **sekwencyjnego przepływu pracy** lub elementu **składnika Web Part**). Nie można uruchomić kodu dla tego elementu podczas wdrażania rozwiązania, ponieważ pakiet rozwiązania nie kopiuje zestawu do globalnej pamięci podręcznej zestawów. Pakiet rozwiązania wdraża zestaw tylko do bazy danych BDC w programie SharePoint. 
  
> [!NOTE]  
>  Podczas debugowania projektu program Visual Studio kopiuje zestaw do obu lokalizacji na lokalnym komputerze. 
  
## <a name="add-an-existing-model"></a>Dodawanie istniejącego modelu
 Możesz zaimportować model, który został utworzony przy użyciu innych narzędzi, takich jak SharePoint Designer. Można także zaimportować istniejący model do projektu w następujących sytuacjach:  
  
-   Aby dostosować model, który jest już wdrożony do farmy serwerów programu SharePoint. 
  
-   Aby utworzyć pakiet i wdrożyć istniejący model w wielu farmach serwerów programu SharePoint. 
  
 W obu przypadkach systemy LOB zdefiniowane w importowanym modelu są niezmienione i będą nadal działać zgodnie z oczekiwaniami. Aby dodać istniejący model do projektu SharePoint, należy użyć okna dialogowego programu Visual Studio **Dodaj istniejący element**. Aby uzyskać więcej informacji, zobacz [Porady: Dodawanie istniejącego pliku modelu BDC do projektu SharePoint](../sharepoint/how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project.md). 
  
System LOB typu zestawu .NET Framework można dodać do importowanego modelu, zaznaczając odpowiednią opcję w obszarze **Dodaj system LOB zestawu .NET **. Umożliwia to pisanie kodu niestandardowego i zdefiniowanie metadanych dla importowanego modelu przy użyciu projektanta.  
  
## <a name="related-topics"></a>Tematy pokrewne
  
|Tytuł|Opis|  
|-----------|-----------------|  
|[Porady: Tworzenie modelu BDC](../sharepoint/how-to-create-a-bdc-model.md)|Pokazuje, jak utworzyć nowy model usługi łączności danych biznesowych.|  
|[Porady: Dodawanie istniejącego modelu BDC do projektu SharePoint](../sharepoint/how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project.md)|Pokazuje, jak zaimportować istniejący model do projektu programu SharePoint.|  
|[Porady: Korzystanie z pliku zasobu do określania zlokalizowanych nazw, właściwości i uprawnień](../sharepoint/how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions.md)|Opisuje sposób udostępnić ciągów, które są łączone w metadanych modelu, jeśli model jest używany przez składnik Web Part lub strony sieci Web.|  
|[Porady: Dołączanie niestandardowego zestawu w funkcji BDC](../sharepoint/how-to-include-a-custom-assembly-in-a-bdc-feature.md)|Pokazuje, jak Dołączanie niestandardowego zestawu w funkcji.|  
  
 
