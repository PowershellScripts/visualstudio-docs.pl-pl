---
title: "Wybór i waluty w IDE | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- currency, Visual Studio IDE
- IDE, selection
- selection, Visual Studio IDE
- IDE, currency
ms.assetid: 2f6f18d1-acd8-454d-a856-9a4d81155052
caps.latest.revision: "14"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 307344a9027e629f08350b77adf99d22d0c127a4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="selection-and-currency-in-the-ide"></a>Wybór i waluty w środowisku IDE
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Zintegrowane środowisko programistyczne (IDE) przechowuje informacje dotyczące użytkowników aktualnie wybranych obiektów za pomocą wyboru *kontekstu*. Kontekst zaznaczenia VSPackages mogą brać udział w walucie śledzenia na dwa sposoby:  
  
-   Przez propagowanie waluty informacji na temat VSPackages do środowiska IDE.  
  
-   Monitorując opcje aktywnych użytkowników w środowisku IDE.  
  
## <a name="selection-context"></a>Kontekst zaznaczenia  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE globalnie przechowuje informacje o waluty IDE w własnego obiektu context globalne zaznaczenia. W poniższej tabeli przedstawiono elementy wchodzące w skład kontekst zaznaczenia.  
  
|Element|Opis|  
|-------------|-----------------|  
|Bieżącej hierarchii|Zwykle bieżącego projektu; bieżącej hierarchii NULL oznacza bieżącego rozwiązania jako całość.|  
|Identyfikator bieżącego elementu|Wybrany element w bieżącej hierarchii; w przypadku wielokrotny w oknie projektu może być wielu elementów bieżącej.|  
|Bieżący`SelectionContainer`|Zawiera co najmniej jeden obiekt, dla których okna właściwości należy wyświetlić właściwości.|  
  
 Ponadto środowisko obsługuje dwie globalnej listy:  
  
-   Lista aktywnych identyfikatory poleceń interfejsu użytkownika  
  
-   Lista typów elementów obecnie aktywne.  
  
### <a name="window-types-and-selection"></a>Typy okien i wybór  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE organizuje systemu windows na dwa ogólne typy:  
  
-   Typ hierarchii systemu windows  
  
-   Okna ramowe, takie jak windows narzędzia i zarządzania dokumentami  
  
 IDE śledzi waluty inaczej dla każdego z tych typów okna.  
  
 Najbardziej typowe typu projektu jest Eksploratorze rozwiązań, który kontroluje IDE. Okno typu projektu śledzi hierarchii globalnej i ItemID kontekst zaznaczenia globalne i okna zależy od wybranej przez użytkownika, aby określić bieżącą hierarchią. Dla systemu windows typu projektu, środowisko zawiera usługę globalnej <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection>, za pomocą których VSPackages można monitorować bieżące wartości dla elementów, Otwórz. Właściwość przeglądania w środowisku jest wymuszany przez tę usługę globalnej.  
  
 Okna ramowe z drugiej strony, umożliwia DocObject w oknie ramowym push wartość SelectionContext (Trójka SelectionContainer hierarchii/identyfikatora elementu). . Okna ramowe korzystania z usługi <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection> w tym celu. DocObject może bezzwłocznie przekazywać tylko wartości kontener wyboru pozostawienie lokalnych wartości dla hierarchii i identyfikator elementu bez zmian, ponieważ jest typowa dla dokumentów podrzędnych MDI.  
  
### <a name="events-and-currency"></a>Zdarzenia i waluty  
 Mogą wystąpić dwa typy zdarzeń, które mają wpływ na środowisko pojęcie waluty:  
  
-   Zdarzenia, które są przenoszone na poziomie globalnym i Zmień kontekst zaznaczenia ramki okna. Przykładami tego rodzaju zdarzenia okno potomne MDI otwierany okna narzędzia globalne otwierany lub otwarciu okna narzędzia typu projektu.  
  
-   Zdarzenia, które zmiany elementów śledzone w kontekście wyboru ramki okna. Przykładami zmiana zaznaczenia w obrębie DocObject lub zmiana zaznaczenia w oknie typu projektu.  
  
## <a name="see-also"></a>Zobacz też  
 [Wybór obiektów kontekstu](../../extensibility/internals/selection-context-objects.md)   
 [Opinię do użytkownika](../../extensibility/internals/feedback-to-the-user.md)