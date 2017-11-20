---
title: Analizowanie i modelowanie architektury | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-techdebt
ms.tgt_pltfrm: 
ms.topic: get-started-article
helpviewer_keywords:
- Visual Studio Ultimate, exploring code
- Visual Studio Ultimate, visualizing code
- diagrams - modeling
- Visual Studio ALM, modeling
- application, design
- architecture
- code visualization
- application design
- applications, architecture
- code exploration
- Visual Studio ALM, exploring code
- modeling
- application architecture
- application, modeling
- applications, modeling
- architecture [Visual Studio ALM], modeling
- application modeling
- Visual Studio Ultimate, modeling
- architecture [Visual Studio Ultimate], modeling
- application, architecture
- Visual Studio ALM, visualizing code
- applications, designing
ms.assetid: c9f04cfa-72bd-419d-a952-616eed01472e
caps.latest.revision: "127"
author: alexhomer1
ms.author: ahomer
manager: douge
ms.openlocfilehash: 57d04543cf604ced1b94632c2f2c3bc566267f85
ms.sourcegitcommit: ec1c7e7e3349d2f3a4dc027e7cfca840c029367d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/07/2017
---
# <a name="analyze-and-model-your-architecture"></a>Analizowanie i modelowanie architektury
Upewnij się, że aplikacja spełnia wymagania architektury za pomocą architektury programu Visual Studio i modelowanie narzędzia do projektowania i modelu aplikacji. 

* Łatwiej zrozumieć istniejący kod programu przy użyciu programu Visual Studio do wizualizacji struktury kodu, zachowania i relacje. 

* Poinformuj zespołu konieczność przestrzegania zależnościami architektury.  
  
* Tworzenie modeli na różnych poziomach szczegółów w całym cyklu życia aplikacji w ramach procesu tworzenia.

Zobacz [scenariusz: zmiana projektu z wykorzystaniem wizualizacji i modelowania](../modeling/scenario-change-your-design-using-visualization-and-modeling.md).  
  
## <a name="to"></a>Do  
  
|||  
|-|-|  
|**Tworzenie wizualizacji kodu**:<br /><br /> — Zobacz organizacji i relacje kodu przez utworzenie mapy kodu. Wizualizowanie zależności między zestawy, przestrzenie nazw, klasy, metody i tak dalej.<br />— Zobacz strukturze klas i członków dla konkretnego projektu przez tworzenie diagramów klas z kodu.<br />-Znalezienie konfliktów między kodu i jego projekt, tworząc diagramy zależności Weryfikacja kodu.|-   [Tworzenie wizualizacji kodu](../modeling/visualize-code.md)<br />-   [Praca z klasami i innymi typami (Projektant klas)](../ide/working-with-classes-and-other-types-class-designer.md)<br />-   [Wideo: Zrozumienie projektu z kodu przy użyciu map kodu programu Visual Studio 2015](https://channel9.msdn.com/Events/Visual-Studio/Connect-event-2015/502)<br />-   [Wideo: Sprawdzanie poprawności zależności architektury w czasie rzeczywistym](https://sec.ch9.ms/sessions/69613110-c334-4f25-bb36-08e5a93456b5/170ValidateArchitectureDependenciesWithVisualStudio.mp4)|  
|**Zdefiniuj architektura**:<br /><br /> -Definiujące i wymuszające ograniczenia dotyczące zależności między składnikami kodu przez tworzenie diagramów zależności.|-   [Wideo: Sprawdzanie poprawności zależnościami architektury z programem Visual Studio (Channel 9)](https://channel9.msdn.com/Events/Connect/2016/170)|  
|**Weryfikacja systemu z wymaganiami i przeznaczony projekt:**<br /><br /> -Sprawdzanie poprawności kodu zależności z diagramy zależności, które opisują architekturę zamierzone i zapobiec zmiany, które może powodować konflikt z projektu.|-   [Wideo: Sprawdzanie poprawności zależnościami architektury z programem Visual Studio (Channel 9)](https://channel9.msdn.com/Events/Connect/2016/170)|  
|**Udostępnianie modeli, diagramy oraz mapy kodu przy użyciu kontroli wersji Team Foundation**:<br /><br /> -Umieścić mapy kodu, projektów i diagramów deoendency w ramach kontroli wersji Team Foundation, aby można je udostępnić.| |  
|**Dostosowywanie modeli i diagramów**:<br /><br /> -Utwórz języków specyficznego dla domeny.|-   [Modelowanie zestawu SDK dla programu Visual Studio — języki specyficzne dla domeny](../modeling/modeling-sdk-for-visual-studio-domain-specific-languages.md)|  
|**Generowanie tekstu przy użyciu szablonów T4**:<br /><br /> -Użyj bloki tekstu i logiki kontroli wewnątrz szablonów na wygenerowanie plików tekstowych.<br /> -T4 kompilacji szablonu przy użyciu programu MSBuild uwzględnione w programie Visual Studio|-   [Generowanie kodu i szablony tekstowe T4](../modeling/code-generation-and-t4-text-templates.md)|

Aby dowiedzieć się, które wersje programu Visual Studio obsługują każdej funkcji, zobacz [obsługę wersji architektura i modelowanie narzędzi](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport)  
  
## <a name="types-of-models-and-their-uses"></a>Typy modeli i ich zastosowań  
  
|**Typ modelu i typowe zastosowania**|  
|-------------------------------------|  
|**Mapy kodu**<br /><br /> Kod mapy pomocy, zobacz organizacji i relacji w kodzie.<br /><br /> Typowe zastosowania:<br /><br /> -Sprawdź kod programu, można lepiej zrozumieć jego struktury i jego zależności, jak zaktualizować go i oszacowanie kosztów proponowane zmiany.<br /><br /> Zobacz:<br /><br /> -   [Zależności mapy w ramach rozwiązań](../modeling/map-dependencies-across-your-solutions.md)<br />-   [Używanie map kodu do debugowania aplikacji](../modeling/use-code-maps-to-debug-your-applications.md)<br />-   [Wyszukiwanie potencjalnych problemów za pomocą analizatorów mapy kodu](../modeling/find-potential-problems-using-code-map-analyzers.md)|  
|**Diagram zależności**<br /><br /> Diagramy zależności umożliwiają zdefiniowanie struktury aplikacji jako zestaw warstw lub bloki z jawne zależności. Można uruchomić sprawdzania poprawności do wykrywania konfliktów między zależności w kodzie i opisano na diagramie zależności zależności.<br /><br /> Typowe zastosowania:<br /><br /> -Ustabilizowania struktury aplikacji za pomocą wiele zmian przez jego użytkowania.<br />-Odnajdź konfliktów zależności niezamierzone przed zaewidencjonowaniem zmian w kodzie.<br /><br /> Zobacz:<br /><br /> -   [Tworzenie diagramów zależności w kodzie](../modeling/create-layer-diagrams-from-your-code.md)<br />-   [Diagramy zależności: odwołanie](../modeling/layer-diagrams-reference.md)<br />-   [Weryfikacja kodu przy użyciu diagramów zależności](../modeling/validate-code-with-layer-diagrams.md)|  
|**Języka specyficznego dla domeny (DSL)**<br /><br /> DSL jest notacji, który projekt z określonym przeznaczeniem. W programie Visual Studio jest zwykle graficznego.<br /><br /> Typowe zastosowania:<br /><br /> -Generowanie lub skonfiguruj części aplikacji. Praca jest wymagany do opracowywania notacji i narzędzia. Może to spowodować powstanie lepszym rozwiązaniem niż dostosowania UML do domeny.<br />— Dla dużych projektów lub, w którym inwestycji w opracowywaniu DSL i jej narzędzi jest zwracany przez użyciem jej w więcej niż jednym projekcie linii produktów.<br /><br /> Zobacz:<br /><br /> -   [Modelowanie zestawu SDK dla programu Visual Studio — języki specyficzne dla domeny](../modeling/modeling-sdk-for-visual-studio-domain-specific-languages.md)|  
  
## <a name="where-can-i-get-more-information"></a>Gdzie można uzyskać więcej informacji?  
  
[Visual Studio wizualizacji & modelowania Forum narzędzia](http://go.microsoft.com/fwlink/?LinkId=184720)  
  
## <a name="see-also"></a>Zobacz też  
 [Nowości](../modeling/what-s-new-for-design-in-visual-studio.md)   
 [DevOps i zarządzanie cyklem życia aplikacji](http://msdn.microsoft.com/Library/74a1f71d-7f23-4c71-8fd7-89ede614fab6)