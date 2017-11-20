---
title: "Ostrzeżenia nazewnictwa | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.codeanalysis.namingrules
helpviewer_keywords:
- managed code analysis warnings, naming warnings
- naming warnings
- warnings, naming
ms.assetid: f97223ce-1d39-4134-81c9-fff2c75d979b
caps.latest.revision: "19"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 21c23e1ebdcf4a4c14fe269376b56a62742e44db
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="naming-warnings"></a>Nazewnictwo — Ostrzeżenia
Ostrzeżenia nazewnictwa Obsługa przestrzeganie konwencje nazewnictwa [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] zaleceń dotyczących projektowania.  
  
## <a name="in-this-section"></a>W tej sekcji  
  
|Reguła|Opis|  
|----------|-----------------|  
|[CA1700: Nie nadawać wartościom enum oznaczenia "Reserved"](../code-quality/ca1700-do-not-name-enum-values-reserved.md)|Ta reguła zakłada, że element członkowski wyliczenia o nazwie, która zawiera „reserved”, nie jest obecnie używany, ale jest symbolem zastępczym do zmiany nazwy lub usunięcia w przyszłej wersji. Zmiana nazwy lub usuwanie członka jest zmianą przerywającą.|  
|[CA1713: Zdarzenia nie powinny mieć, prefiksów before ani after](../code-quality/ca1713-events-should-not-have-before-or-after-prefix.md)|Nazwa zdarzenia rozpoczyna się od „Before” lub „After”. Nazwa powiązanych zdarzeń, które są wywoływane w określonej kolejności, używa czasu teraźniejszego lub przeszłego, aby wskazać względne położenie akcji w sekwencji.|  
|[CA1714: Typy wyliczeniowe flag powinny mieć nazwy w liczbie mnogiej](../code-quality/ca1714-flags-enums-should-have-plural-names.md)|Publiczne wyliczenie ma atrybut System.FlagsAttribute i jego nazwa nie kończy się "s". Typy, które są oznaczone atrybutem Flags mają nazwy, które nie są mnogiej, ponieważ ten atrybut wskazuje, że można określić więcej niż jedną wartość.|  
|[CA1704: Identyfikatory powinny być napisane poprawnie](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)|Nazwa widocznego na zewnątrz identyfikatora zawiera jeden lub więcej wyrazów, które nie są rozpoznane przez bibliotekę sprawdzania pisowni Microsoft.|  
|[CA1708: Identyfikatory powinny różnić się tylko wielkością liter](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)|Identyfikatory przestrzeni nazw, typów, elementów członkowskich i parametry nie mogą się różnić jedynie wielkością liter, ponieważ języki dla środowiska uruchomieniowego języka wspólnego nie muszą rozróżniać wielkości liter.|  
|[CA1715: Identyfikatory powinny mieć poprawny prefiks](../code-quality/ca1715-identifiers-should-have-correct-prefix.md)|Nazwa interfejsu widoczne na zewnątrz nie rozpoczyna się litera "I".  Nazwa parametru typu ogólnego, na zewnątrz typu lub metody nie rozpoczyna się wielką "T".|  
|[CA1720: Identyfikatory nie powinny zawierać nazw typów](../code-quality/ca1720-identifiers-should-not-contain-type-names.md)|Nazwa parametru w widocznym na zewnątrz elemencie członkowskim zawiera nazwę typu danych lub nazwa widocznego na zewnątrz elementu członkowskiego zawiera specyficzną dla języka nazwę typu danych.|  
|[CA1722: Identyfikatory nie powinny mieć nieprawidłowych prefiksów](../code-quality/ca1722-identifiers-should-not-have-incorrect-prefix.md)|Zgodnie z konwencją, tylko niektóre elementy programowania mają nazwy rozpoczynające się od określonego prefiksu.|  
|[CA1711: Identyfikatory nie powinny mieć nieprawidłowych sufiksów](../code-quality/ca1711-identifiers-should-not-have-incorrect-suffix.md)|Według konwencji nazwy typów, które rozszerzają pewne typy podstawowe lub implementują dane interfejsy lub typy pochodzące z tych typów, powinny kończyć się określonym zarezerwowanym sufiksem. Inne nazwy typów nie powinny używać tych zarezerwowanych sufiksów.|  
|[CA1717: Tylko wyliczenia z atrybutem Flags powinny mieć nazwy w liczbie mnogiej](../code-quality/ca1717-only-flagsattribute-enums-should-have-plural-names.md)|Zgodnie z konwencjami nazewnictwa, nazwa w liczbie mnogiej dla wyliczenia wskazuje, że w tym samym czasie można określić więcej niż jedną wartość wyliczenia.|  
|[CA1725: Nazwy parametrów powinny pasować do podstawowej deklaracji](../code-quality/ca1725-parameter-names-should-match-base-declaration.md)|Spójne nazywanie parametrów w zastąpieniu hierarchii zwiększa użyteczność zastąpienia metody. Jeśli nazwa parametru w metodzie pochodnej różni się od nazwy podstawowej deklaracji, może nie być jasne, czy metoda jest zastąpieniem metody podstawowej, czy też nowym przeciążeniem metody.|  
|[CA1719: Nazwy parametrów nie powinny odpowiadać nazwom elementu członkowskiego](../code-quality/ca1719-parameter-names-should-not-match-member-names.md)|Nazwa parametru skontaktować się znaczenie parametr, a nazwę elementu członkowskiego skontaktować się znaczenie elementu członkowskiego. W projekcie rzadko są one takie same. Nazywanie parametru tak samo jak nazwa jego elementu członkowskiego jest nieintuicyjne i utrudnia korzystanie z biblioteki.|  
|[CA1701: Wyrazy złożone ciągu zasobu powinny mieć prawidłową wielkość liter](../code-quality/ca1701-resource-string-compound-words-should-be-cased-correctly.md)|Każdego wyrazu w ciągu zasobu jest podzielony na tokeny, które są oparte na wielkość liter. Każda ciągła kombinacja dwóch tokenów jest sprawdzana przez bibliotekę sprawdzania pisowni firmy Microsoft. Jeżeli zostanie rozpoznana, dane słowo powoduje naruszenie reguły.|  
|[CA1703: Ciągów zasobów powinna być poprawna](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)|Ciąg zasobu zawiera jeden lub więcej wyrazów, które nie są rozpoznane przez bibliotekę sprawdzania pisowni Microsoft.|  
|[CA1724: Nazwy typów nie powinny odpowiadać nazwom](../code-quality/ca1724-type-names-should-not-match-namespaces.md)|Nazwy typów nie powinny odpowiadać nazwy przestrzeni nazw, które są zdefiniowane w [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] biblioteki klas. Naruszenie tej reguły można ograniczyć użyteczność biblioteki.|  
|[CA1707: Identyfikatory nie powinny zawierać podkreśleń](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)|Przez konwencję identyfikatory nazw nie zawierają znaku podkreślenia (_). Ta reguła sprawdza przestrzenie nazw, typy, elementy członkowskie i parametry.|  
|[CA1721: Właściwości nazwy nie powinny odpowiadać metodom get](../code-quality/ca1721-property-names-should-not-match-get-methods.md)|Nazwa publicznego lub chronionego elementu członkowskiego zaczyna się od „Get” i odpowiada nazwie właściwości publicznej lub chronionej. Metody „Get” i właściwości powinny mieć nazwy, które wyraźnie odróżniają ich funkcje.|  
|[CA1716: Identyfikatory nie powinny odpowiadać słowom](../code-quality/ca1716-identifiers-should-not-match-keywords.md)|Przestrzeń nazw lub nazwa typu odpowiada zastrzeżonym słowom kluczowym w języku programowania. Identyfikatory przestrzeni nazw i typów nie powinny być zgodne ze słowami kluczowymi, które są definiowane przez języki dla środowiska uruchomieniowego języka wspólnego.|  
|[CA1726: Używaj preferowanych terminów](../code-quality/ca1726-use-preferred-terms.md)|Nazwa widocznego na zewnątrz identyfikatora zawiera termin, dla którego istnieje alternatywny, preferowany zamiennik. Alternatywnie nazwa zawiera określenie „Flag” lub „Flags”.|  
|[CA1709: Identyfikatory powinny mieć prawidłową wielkość liter](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)|Konwencja, nazwy parametrów używać mieszanej wielkości liter i przestrzeni nazw, typu, a nazwy elementów członkowskich Pascal wielkości liter.|  
|[CA1702: Wyrazy złożone powinien mieć prawidłową wielkość liter](../code-quality/ca1702-compound-words-should-be-cased-correctly.md)|Nazwa identyfikatora zawiera wiele wyrazów i co najmniej jeden z nich wydaje się wyrazem złożonym, w którym wielkość liter nie jest poprawna.|  
|[CA1712: Nie dodawaj prefiksu wartości enum nazwą typu](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)|Nazwy elementów członkowskich wyliczenie nie są poprzedzane prefiksem nazwy typu, ponieważ informacje o typie oczekiwana jest dostarczane przez narzędzia deweloperskie.|  
|[CA1710: Identyfikatory powinny mieć poprawny przyrostek](../code-quality/ca1710-identifiers-should-have-correct-suffix.md)|Konwencja nazwy typów, które rozszerzać niektórych typów podstawowych lub zawierają implementację niektórych interfejsów lub typy pochodzące z tych typów mieć sufiks, który jest skojarzony z typu podstawowego lub interfejs.|