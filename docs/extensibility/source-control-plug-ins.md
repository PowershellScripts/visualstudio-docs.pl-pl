---
title: "Dodatki plug-in do kontroli źródła | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: source control plug-ins, reference
ms.assetid: 964980ca-21c5-4706-8535-6ea23e1c9cc9
caps.latest.revision: "17"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ea5169b3d74a77bbb079dab5b310a3b7ebbbeff0
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="source-control-plug-ins"></a>Plug-in kontroli źródła
Sekcja odwołania zestawu SDK dodatku typu Plug-in kontroli źródła zawiera specyfikacja interfejsu pełną, który umożliwia systemów kontroli źródła do można zintegrować z [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Określa składnię i semantyki różne typy danych i funkcje, które wtyczka do kontroli źródła należy zaimplementować interfejsu z [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] zintegrowane środowisko programistyczne (IDE).  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Funkcje API wtyczkę kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)  
 Zawiera listę funkcji, które muszą zostać zaimplementowane przez wtyczkę kontroli źródła do wykonania API dodatku typu Plug-in kontroli źródła.  
  
 [Funkcje wywołania zwrotnego zaimplementowana IDE](../extensibility/callback-functions-implemented-by-the-ide.md)  
 Opisuje funkcje używane do przekazywania informacji do środowiska IDE, gdy niektóre polecenia są wykonywane przez wtyczkę kontroli źródła.  
  
 [Moduły wyliczające](../extensibility/enumerators.md)  
 Wyświetla listę typów danych modułu wyliczającego w interfejsie API dodatku typu Plug-in kontroli źródła znajomość wtyczkę kontroli źródła.  
  
 [Flagi możliwości](../extensibility/capability-flags.md)  
 W tym artykule opisano `SCC_CAP_xxx` flagi, wskazujące możliwości dostawcy.  
  
 [Używane przez określonego polecenia flag bitowych](../extensibility/bitflags-used-by-specific-commands.md)  
 Wyświetla listę flag, które są przydatne w kontekście określonego polecenia.  
  
 [Kody błędów](../extensibility/error-codes.md)  
 Wyświetla listę wartości typowych błędów zwracanych przez funkcje jako `SCCTRN`.  
  
 [Ciągi używane jako klucze do znajdowania wtyczka do kontroli źródła](../extensibility/strings-used-as-keys-for-finding-a-source-control-plug-in.md)  
 W tym artykule opisano klucze do uzyskiwania dostępu do rejestru, aby znaleźć wtyczka do kontroli źródła.  
  
 [MSSCCPRJ. Plik SCC](../extensibility/mssccprj-scc-file.md)  
 W tym artykule opisano plik po stronie klienta, zawierającego informacje o nieprzezroczysta dla IDE, ale używany przez wtyczkę kontroli źródła do zlokalizowania rozwiązania lub projektu w kontroli wersji.  
  
 [Najlepsze rozwiązania dotyczące wdrażania dodatku Plug-in kontroli źródła](../extensibility/best-practices-for-implementing-a-source-control-plug-in.md)  
 Zawiera kolekcję ważne przypomnienia techniczne pamiętać podczas wdrażania interfejsu API dodatku typu Plug-in kontroli źródła.  
  
 [Ograniczenia długości ciągu](../extensibility/restrictions-on-string-lengths.md)  
 Opis ograniczeń w interfejsie API dodatku typu Plug-in kontroli źródła na długości ciągów używanych w różnych funkcji.  
  
 [Słownik](../extensibility/source-control-plug-in-glossary.md)  
 Udostępnia przydatne postanowień oraz ich definicje do odczytywania dokumentacji zestawu SDK dodatku typu Plug-in kontroli źródła.  
  
 [Porady: wyłączanie ostrzeżenia dotyczące zgodności dla plug-in kontroli źródła](../extensibility/how-to-turn-off-compatibility-warnings-for-source-control-plug-ins.md)  
 Opisuje sposób wyłączania ostrzeżenia.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Przykładowa wtyczka kontroli źródła](http://msdn.microsoft.com/en-us/61de7d2b-71db-451e-8e3e-d41b11c7a4ca)  
 Podano przykładowe funkcje wtyczkę kontroli źródła.  
  
 [Przewodnik po testowym dla plug-in kontroli źródła](../extensibility/internals/test-guide-for-source-control-plug-ins.md)  
 Zawiera opis procedur testowych związane z wtyczka do kontroli źródła.  
  
 [Tworzenie wtyczki kontroli źródła](../extensibility/internals/creating-a-source-control-plug-in.md)  
 W tym artykule omówiono sposób tworzenia wtyczka do kontroli źródła dostarczającego funkcja kontroli źródła, gdy jest używany [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] interfejsu użytkownika kontroli źródła (UI).  
  
 [Odwołanie do zestawu SDK programu Visual Studio](../extensibility/visual-studio-sdk-reference.md)  
 Wyświetla listę tematów odwołania.