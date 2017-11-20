---
title: "Dodawanie nowych źródeł danych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.datasource.datasourcefieldspicker
helpviewer_keywords:
- data [Visual Studio], data sources
- data sources
ms.assetid: ed28c625-bb89-4037-bfde-cfa435d182a2
caps.latest.revision: "56"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: 0c83367d383ab72194e5f83609b0f93d8602fdcd
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="add-new-data-sources"></a>Dodawanie nowych źródeł danych
W kontekście narzędzi danych .NET w programie Visual Studio termin *źródła danych* odwołuje się do obiektów .NET połączenia z magazynem danych i udostępniania danych do aplikacji .NET. Projektanci programu Visual Studio może używać źródła danych do generowania kodu umożliwiającego, który wiąże dane do formularzy podczas przeciągania i upuszczania obiektów bazy danych z danych wyjściowych **źródeł danych** okna. Tego rodzaju źródła danych może być:  
  
-   Klasa w modelu Entity Framework, która jest skojarzona z jakiejś bazy danych.  
  
-   Zestaw danych, który jest skojarzony z jakiejś bazy danych.  
  
-   Klasa, która reprezentuje usługi sieciowej, takich jak dane usługi Windows Communication Foundation (WCF) lub usługi REST.  
  
-   Klasa, która reprezentuje usługi programu SharePoint.  
  
-   Klasa lub kolekcji w rozwiązaniu.  
  
> [!NOTE]
>  Jeśli nie używasz funkcji wiązania danych, zestawy danych, Entity Framework LINQ do SQL, WCF lub SharePoint, pojęcie "źródło danych" nie ma zastosowania. Po prostu połączenia bezpośrednio z bazą danych przy użyciu obiektów SQLCommand i komunikować się bezpośrednio z bazą danych.  
  
 Możesz tworzyć i edytować źródła danych za pomocą **Kreator konfiguracji źródła danych** w aplikacji formularzy systemu Windows lub Windows Presentation Foundation. Entity Framework, należy najpierw utworzyć klas jednostek, a następnie uruchomić kreatora, wybierając **projektu** > **Dodaj nowe źródło danych** (opisany bardziej szczegółowo w dalszej części tego artykułu).  
  
 ![Kreator konfiguracji źródła danych](../data-tools/media/data-source-configuration-wizard.png "Kreator konfiguracji źródła danych")  
  
 Po utworzeniu źródła danych, zostanie wyświetlony w **źródeł danych** okna narzędzia (Shift + Alt + D lub **widoku** > **inne okna**  >  **Źródła danych**). Możesz przeciągnąć źródła danych z **źródeł danych** okna na powierzchni projektowej formularza lub kontrolki. Powoduje to schematyczny kod służący do wygenerowania — kod, który zawiera dane, które pochodzą z magazynu danych do użytkownika. Na poniższej ilustracji przedstawiono zestawu danych, który został porzucony na formularzu systemu Windows. Jeśli wybrano F5 w aplikacji, dane z bazy danych pojawią się w formantach formularza.  
  
 ![Źródło danych operacji przeciągania](../data-tools/media/raddata-data-source-drag-operation.png "operacji przeciągania raddata źródła danych")  
  
## <a name="data-source-for-a-database-or-a-database-file"></a>Źródło danych dla bazy danych lub pliku bazy danych  
  
### <a name="dataset"></a>Zestaw danych  
 Aby utworzyć zestawu danych jako źródła danych, uruchom **Kreator konfiguracji źródła danych** (**projektu** > **Dodaj nowe źródło danych**) i wybierz polecenie  **Baza danych** typ źródła danych. Postępuj zgodnie z monitami, aby określić połączenia nowej lub istniejącej bazy danych lub pliku bazy danych.  
  
### <a name="entity-classes"></a>Klas jednostek  
 Aby utworzyć model narzędzia Entity Framework jako źródło danych, najpierw uruchom **kreatora modelu danych jednostki** do tworzenia klas jednostek (**projektu** > **Dodaj nowy element**  >  **Modelu danych jednostki ADO.NET**).  
  
 ![Nowy element projektu modelu programu Entity Framework](../data-tools/media/raddata-new-entity-framework-model-project-item.png "raddata nowego programu Entity Framework modelu projektu elementu")  
  
 Wybierz metodę, za pomocą którego chcesz wygenerować model.  
  
 ![Kreator modelu danych jednostki](../data-tools/media/raddata-entity-data-model-wizard.png "raddata kreatora modelu danych jednostki")  
  
 Dodaj modelu jako źródła danych. Klasy, które zostały wygenerowane są wyświetlane w **Kreator konfiguracji źródła danych** po wybraniu **obiektów** kategorii.  
  
 ![Kreator konfiguracji źródła danych z klas jednostek](../data-tools/media/raddata-data-source-configuration-wizard-with-entity-classes.png "raddata Kreator konfiguracji źródła danych z klasami jednostki")  
  
## <a name="data-source-for-a-service"></a>Źródło danych dla usługi  
 Aby utworzyć źródło danych z usługi, uruchom **Kreator konfiguracji źródła danych** i wybierz polecenie **usługi** typ źródła danych. Jest to naprawdę właśnie skrót do **Dodaj odwołanie do usługi** okno dialogowe, które można również przejść, klikając prawym przyciskiem myszy projekt w **Eksploratora rozwiązań** i wybierając **dodać odwołania do usługi** .  
  
 Po utworzeniu źródła danych z usługą Visual Studio dodaje odwołania do usługi do projektu. Visual Studio tworzy także obiekty serwera proxy, które odnoszą się do obiektów, które zwraca usługi. Na przykład usługa, która zwraca dataset jest reprezentowany w projekcie dataset; Usługa, która zwraca wartość określonego typu jest wyświetlana w projekcie jako typ zwracany.  
  
 Można utworzyć źródło danych spośród następujących typów usług:  
  
-   Usługi danych WCF. Aby uzyskać więcej informacji, zobacz [omówienie](/dotnet/framework/data/wcf/wcf-data-services-overview).  
  
-   Usługi WCF. Aby uzyskać więcej informacji, zobacz [usług Windows Communication Foundation oraz usługi danych WCF w programie Visual Studio](../data-tools/windows-communication-foundation-services-and-wcf-data-services-in-visual-studio.md).  
  
-   Usługi sieci Web.  
  
    > [!NOTE]
    >  Elementy, które są widoczne w **źródeł danych** okna są zależne od danych, które zwraca usługi. Niektóre usługi mogą nie zawiera informacji wystarczających **Kreator konfiguracji źródła danych** do tworzenia obiektów powiązania. Na przykład, jeśli usługa zwraca nietypizowanego zestawu danych, elementy nie będą wyświetlane w **źródeł danych** okna po zakończeniu pracy kreatora. Jest tak dlatego nietypizowane zbiory danych i schemat nie zostanie określona, i w związku z tym kreatorze nie ma wystarczających informacji do utworzenia źródła danych.  
  
## <a name="data-source-for-an-object"></a>Źródło danych obiektu  
 Można utworzyć źródło danych z dowolnych obiektów, który ujawnia co najmniej jednej właściwości publiczne, uruchamiając **Kreator konfiguracji źródła danych** , a następnie wybierając **obiektu** typ źródła danych. Wszystkie publiczne właściwości obiektu są wyświetlane w **źródeł danych** okna.   Jeśli używasz programu Entity Framework i mieć wygenerowany model, jest to, gdzie znaleźć klas jednostek, które będą źródła danych dla aplikacji.  
  
 Na **wybierz obiekty danych** strony, rozwiń węzły w widoku drzewa do lokalizowania obiektów, które chcesz powiązać. Widok drzewa zawiera węzły dla projektu i zestawów i inne projekty, do których odwołuje się projekt.  
  
 Jeśli chcesz powiązać obiektu w zestawie lub projektu, który nie jest wyświetlany w widoku drzewa kliknij **Dodaj odwołanie do** i użyj **Dodaj odwołanie — okno dialogowe** można dodać odwołania do zestawu lub projektu. Po dodaniu odwołania zestawu lub projekt jest dodawana do widoku drzewa.  
  
> [!NOTE]
>  Może być konieczne skompilowanie projektu, który zawiera obiekty, zanim obiekty zostaną wyświetlone w widoku drzewa.  
  
> [!NOTE]
>  Do obsługi powiązania danych przeciągnij i upuść obiekty, które implementują <xref:System.ComponentModel.ITypedList> lub <xref:System.ComponentModel.IListSource> interfejs musi mieć konstruktora domyślnego. W przeciwnym razie Visual Studio nie może utworzyć wystąpienia obiektu źródła danych, a następnie zostanie wyświetlony błąd, gdy użytkownik przeciąga element powierzchnię projektu.  
  
## <a name="data-source-for-a-sharepoint-list"></a>Źródło danych dla listy programu SharePoint  
 Możesz utworzyć źródło danych z listy programu SharePoint, uruchamiając **Kreator konfiguracji źródła danych** i wybierając **SharePoint** typ źródła danych. SharePoint udostępnia dane za pomocą [!INCLUDE[ssAstoria](../data-tools/includes/ssastoria_md.md)], dlatego tworzenie źródła danych programu SharePoint jest taki sam, jak podczas tworzenia źródła danych z usługi. Wybieranie **SharePoint** elementu **Kreator konfiguracji źródła danych** otwiera **Dodaj odwołanie do usługi** okno dialogowe, w którym można połączyć się z usługą danych programu SharePoint poprzez wskazanie serwera programu SharePoint.  To wymaga zestawu SDK programu SharePoint.  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio tools danych dla platformy .NET](../data-tools/visual-studio-data-tools-for-dotnet.md)