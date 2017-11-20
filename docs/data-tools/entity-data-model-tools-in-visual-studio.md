---
title: "Entity Framework narzędzia w programie Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 1b06b573-84aa-4458-b3f5-e238df47bf45
caps.latest.revision: "21"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: eb4ca4445af3970828f4212c69c11d9d173d5650
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="entity-framework-tools-in-visual-studio"></a>Entity Framework narzędzia w programie Visual Studio
Entity Framework jest technologia mapowania relacyjnego obiektu, która umożliwia deweloperom platformy .NET pracować z relacyjnej bazie danych przy użyciu obiektów specyficznego dla domeny. Eliminuje potrzebę większość kodu dostępu do danych, deweloperzy zazwyczaj potrzebne do zapisu. Entity Framework jest zalecane mapowania obiektów relacyjnych (ORM) modelowania technologii nowych aplikacji .NET.  
  
Entity Framework narzędzia są przeznaczone do tworzenia aplikacji Entity Framework (EF). Pełną dokumentację programu Entity Framework jest tutaj: [EF rdzeni i EF 6](https://docs.microsoft.com/ef/).  
  
Narzędziami Entity Framework, można utworzyć *modelu koncepcyjnego* z istniejącej bazy danych graficznie wizualizacji i edytować model koncepcyjny. Lub graficznie najpierw utworzyć model koncepcyjny, a następnie wygenerować bazę danych, która obsługuje modelu. W obu przypadkach można automatycznie aktualizować modelu, gdy podstawowa zmiany bazy danych i automatycznie generować kod warstwy obiektu aplikacji. Dostosowania są generowania bazy danych i warstwy obiektu generowania kodu.  
  
Narzędzia Entity Framework są instalowane jako część **magazynu danych i przetwarzania** obciążenia w Instalatorze programu Visual Studio. Można także zainstalować jako składnik indvidual w obszarze **zestawów SDK, bibliotek i platform** kategorii.  
 
Są to określone narzędzia, które tworzą narzędzia Entity Framework w programie Visual Studio:  
  
-   Można użyć [!INCLUDE[vstecado](../data-tools/includes/vstecado_md.md)]  **[!INCLUDE[adonet_edm](../data-tools/includes/adonet_edm_md.md)] projektanta** (**Entity Designer**) aby wizualnie tworzyć i modyfikować jednostek, skojarzenia mapowania i relacji dziedziczenia. **Entity Designer** generuje również [!INCLUDE[TLA#tla_cshrp](../data-tools/includes/tlasharptla_cshrp_md.md)] lub [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] kodu warstwy obiektu.  
  
-   Można użyć  **[!INCLUDE[adonet_edm](../data-tools/includes/adonet_edm_md.md)] kreatora** do generowania modelu koncepcyjnego z istniejącej bazy danych i Dodaj informacje dotyczące połączenia bazy danych do aplikacji.  
  
-   Można użyć **Kreatora tworzenia bazy danych** najpierw utworzyć model koncepcyjny, a następnie utworzyć bazę danych, która obsługuje model.  
  
-   Można użyć **Kreatora aktualizacji modelu** można zaktualizować Twojego model koncepcyjny modelu magazynu i mapowania podczas zmiany zostały wprowadzone do podstawowej bazy danych.  
  
    > [!NOTE]
    >  Począwszy od programu Visual Studio 2010 narzędzia Entity Framework nie obsługują [!INCLUDE[ss2k](../data-tools/includes/ss2k_md.md)].  
  
Narzędzia Generowanie lub zmodyfikowania pliku edmx. Ten plik edmx zawiera informacje opisujące modelu koncepcyjnego i modelu magazynu, mapowań między nimi. Aby uzyskać więcej informacji, zobacz [EDMX](https://msdn.microsoft.com/data/jj650889.aspx).  
  
[Entity Framework zaawansowanych narzędzi](https://marketplace.visualstudio.com/items?itemName=EntityFrameworkTeam.EntityFrameworkPowerToolsBeta4) tworzenia aplikacji, które używają modelu danych jednostki. Narzędzia power można wygenerować model koncepcyjny, sprawdzania poprawności istniejącego modelu, tworzenia plików kodu źródłowego, zawierające klasy obiektu oparte na modelu koncepcyjnego i tworzenia plików kodu źródłowego, które zawierają widoki, które generuje modelu. Aby uzyskać szczegółowe informacje, zobacz [widoków mapowania Pre-Generated](https://msdn.microsoft.com/data/dn469601.aspx).  
  
## <a name="related-topics"></a>Tematy pokrewne  
  
|Tytuł|Opis|  
|-----------|-----------------|  
|[ADO.NET Entity Framework](/dotnet/framework/data/adonet/ef/index)|Informacje dotyczące używania [!INCLUDE[adonet_edm](../data-tools/includes/adonet_edm_md.md)] narzędzia, które [!INCLUDE[adonet_ef](../data-tools/includes/adonet_ef_md.md)] umożliwia tworzenie aplikacji.|  
|[Modelu danych jednostki](/dotnet/framework/data/adonet/entity-data-model)|Zawiera łącza i informacje dotyczące pracy z danymi, który jest używany przez aplikacje oparte na [!INCLUDE[adonet_ef](../data-tools/includes/adonet_ef_md.md)].|  
|[Entity Framework (EF) dokumentacji)](https://msdn.microsoft.com/library/ee712907(v=vs.113).aspx)|Zawiera indeks wideo, samouczki i zaawansowane dokumentacji, aby pomóc najlepiej Entity Framework.|  
|[ASP.NET 5 aplikacji do nowej bazy danych](https://docs.efproject.net/en/latest/platforms/aspnetcore/new-db.html)|Opisuje sposób tworzenia nowej aplikacji ASP.NET 5 za pomocą programu Entity Framework 7.|  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio tools danych dla platformy .NET](../data-tools/visual-studio-data-tools-for-dotnet.md)