---
title: "Ostrzeżenia o zabezpieczeniach | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.codeanalysis.securityrules
helpviewer_keywords:
- security [Visual Studio ALM], Enterprise Templates
- security warnings
- managed code analysis warnings, security warnings
- warnings, security
ms.assetid: 60d4e8ea-230a-494f-aa6a-b91db77540e4
caps.latest.revision: "28"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 54b7a3a62c5940419b946b85424fa745298bb89b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="security-warnings"></a>Ostrzeżenia o zabezpieczeniach
Ostrzeżenia o zabezpieczeniach obsługują bezpieczniejsze biblioteki i aplikacje. Ostrzeżenia te pomagają zapobiec usterkom w zabezpieczeniach w programie. Przyczynę wyłączenia któregokolwiek z tych ostrzeżeń należy wyraźnie oznaczyć w kodzie i poinformować o tym osobę odpowiedzialną za bezpieczeństwo w projekcie.  
  
## <a name="in-this-section"></a>W tej sekcji  
  
|Reguła|Opis|  
|----------|-----------------|  
|[Ca2100: należy Przeglądnąć zapytania SQL w poszukiwaniu luk w zabezpieczeniach](../code-quality/ca2100-review-sql-queries-for-security-vulnerabilities.md)|Metoda ustawia właściwość System.Data.IDbCommand.CommandText przez użycie ciągu, który jest zbudowany z argumentem ciągu do metody. Zasada ta zakłada, że argument ciągu zawiera dane wejściowe użytkownika. Ciąg polecenia SQL zbudowany z danych wejściowych użytkownika jest narażony na ataki przez wstrzyknięcie kodu SQL.|  
|[CA2102: Przechwytuj wyjątki bez atrybutu CLSCompliant w ogólnych procedurach obsługi](../code-quality/ca2102-catch-non-clscompliant-exceptions-in-general-handlers.md)|Element członkowski w zestawie, który nie jest oznaczony za pomocą atrybutu RuntimeCompatibilityAttribute lub jest oznaczony jako RuntimeCompatibility(WrapNonExceptionThrows = false), zawiera blok catch obsługujący wyjątek System.Exception i nie zawiera bezpośrednio następującego ogólnego bloku catch.|  
|[CA2103: Przejrzyj zabezpieczenia imperatywne](../code-quality/ca2103-review-imperative-security.md)|Metoda używa imperatywnych zabezpieczeń i może konstruować uprawnienia za pomocą informacji o stanie lub wartości zwrotnych, które można zmienić, podczas gdy żądanie jest aktywne. Należy używać zabezpieczeń deklaracyjnych wszędzie, gdzie to możliwe.|  
|[CA2104: Nie deklaruj typów referencyjnych tylko do odczytu](../code-quality/ca2104-do-not-declare-read-only-mutable-reference-types.md)|Typ widoczny z zewnątrz zawiera widoczne na zewnątrz pole tylko do odczytu, które jest typu referencji zmiennej. Typ zmienny to typ, którego dane wystąpienia mogą być modyfikowane.|  
|[CA2105: Pola tablicy nie powinien być odczytywany tylko](../code-quality/ca2105-array-fields-should-not-be-read-only.md)|Po zastosowaniu modyfikator (tylko do odczytu w języku Visual Basic) tylko do odczytu do pola, które zawiera tablicę, pole nie można zmienić do innej tablicy odwołania. Można jednak zmienić elementy tablicy przechowywane w polu tylko do odczytu.|  
|[CA2106: Secure potwierdzeń](../code-quality/ca2106-secure-asserts.md)|Metoda potwierdza uprawnienia i żadne sprawdzenia zabezpieczeń nie są wykonywane na obiekcie wywołującym. Potwierdzanie uprawnienia zabezpieczeń bez sprawdzania zabezpieczeń może pozostawić zdatną do wykorzystania słabość zabezpieczeń w kodzie.|  
|[CA2107: Przejrzyj Odmów i permit only](../code-quality/ca2107-review-deny-and-permit-only-usage.md)|Metoda PermitOnly i akcje zabezpieczeń CodeAccessPermission.Deny powinny być używane tylko przez tych, którzy mają zaawansowaną wiedzę o zabezpieczeniach .NET Framework. Kod, który używa tych akcji zabezpieczeń, należy poddać przeglądowi zabezpieczeń.|  
|[Ca2108: należy Przeglądnąć zabezpieczenia deklaratywne dla typów wartości](../code-quality/ca2108-review-declarative-security-on-value-types.md)|Publiczny lub chroniony typ wartości jest zabezpieczony przez dostęp do danych lub zapotrzebowanie na łącza.|  
|[CA2109: Przejrzyj widoczne programy obsługi zdarzeń](../code-quality/ca2109-review-visible-event-handlers.md)|Wykryto publiczną lub chronioną metodę obsługi zdarzeń. Metody obsługi zdarzeń nie powinny być udostępnione, chyba że jest to absolutnie konieczne.|  
|[CA2111: Wskaźniki nie powinny być widoczne](../code-quality/ca2111-pointers-should-not-be-visible.md)|Wskaźnik nie jest prywatny, wewnętrzny ani tylko do odczytu. Złośliwy kod może zmienić wartość wskaźnika, potencjalnie umożliwiając dostęp do dowolnego miejsca w pamięci lub powodując błędy aplikacji bądź systemu.|  
|[CA2112: Typy zabezpieczone nie powinny ujawniać pól](../code-quality/ca2112-secured-types-should-not-expose-fields.md)|Typ publiczny lub chroniony zawiera pola publiczne i jest zabezpieczony przez zapotrzebowania na łącza. Jeśli kod ma dostęp do wystąpienia typu zabezpieczonego przez żądanie łącza, kod nie musi spełniać zapotrzebowania na łącza, aby uzyskać dostęp do pól typu.|  
|[CA2114: Metody zabezpieczeń powinny być nadzbiorem typu](../code-quality/ca2114-method-security-should-be-a-superset-of-type.md)|Metoda nie powinna mieć zabezpieczeń deklaratywnych zarówno na poziomie metody, jak i na poziomie typu dla tej samej akcji.|  
|[CA2115: Wywołaj GC. KeepAlive, gdy używasz zasobów natywnych](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)|Ta reguła wykrywa błędy, które mogą wystąpić, ponieważ kończy się działanie niezarządzanego zasobu, a wciąż jest on używany w kodzie niezarządzanym.|  
|[CA2116: Metody APTCA powinny wywoływać tylko metody APTCA](../code-quality/ca2116-aptca-methods-should-only-call-aptca-methods.md)|Gdy atrybut APTCA (AllowPartiallyTrustedCallers) jest obecny w zestawie całkowicie zaufanym i wykonuje kod w innym zestawie, który nie zezwala na dostęp częściowo zaufanych wywołań, mogą zostać wykorzystane luki w zabezpieczeniach.|  
|[CA2117: Typy APTCA powinny rozszerzać tylko typy bazowe APTCA](../code-quality/ca2117-aptca-types-should-only-extend-aptca-base-types.md)|Gdy atrybut APTCA (AllowPartiallyTrustedCallers) jest obecny w całkowicie zaufanym zestawie i typ w zestawie dziedziczy z typu, który nie zezwala na dostęp częściowo zaufanych wywołań, mogą zostać wykorzystane luki w zabezpieczeniach.|  
|[CA2118: Przegląd wykorzystania SuppressUnmanagedCodeSecurityAttribute](../code-quality/ca2118-review-suppressunmanagedcodesecurityattribute-usage.md)|SuppressUnmanagedCodeSecurityAttribute zmienia domyślne zachowanie systemu zabezpieczeń dla elementów członkowskich wykonujących kod niezarządzany, który używa wywołań międzyoperacyjnych COM lub platformy. Atrybut ten jest używany głównie w celu zwiększenia wydajności; jednak wzrost wydajności powoduje znaczące zagrożenia dla bezpieczeństwa.|  
|[CA2119: Zapieczętuj metody, które spełniają interfejsy prywatne](../code-quality/ca2119-seal-methods-that-satisfy-private-interfaces.md)|Dziedziczone typu publicznego udostępnia implementację przesłonięcia metody Interfejs wewnętrzny (Friend w języku Visual Basic). Aby naprawić naruszenie tej zasady, należy zapobiegać zastąpieniu metody poza zestawem.|  
|[CA2120: Zabezpieczaj konstruktory serializacji](../code-quality/ca2120-secure-serialization-constructors.md)|Typ ten ma konstruktor, który przyjmuje obiekt System.Runtime.Serialization.SerializationInfo i obiekt System.Runtime.Serialization.StreamingContext (podpis konstruktora serializacji). Ten konstruktor nie jest zabezpieczony przez sprawdzanie zabezpieczeń, ale jeden lub kilka regularnych konstruktorów typu jest zabezpieczonych.|  
|[CA2121: Konstruktory statyczne powinny być prywatne](../code-quality/ca2121-static-constructors-should-be-private.md)|System wywołuje statyczny konstruktor przed utworzeniem pierwszego wystąpienia typu lub przed odwołaniem do któregokolwiek ze statycznych elementów członkowskich. Jeśli konstruktor statyczny nie jest prywatny, może być wywołany przez kod inny niż system. W zależności od operacji, które są wykonywane w konstruktorze, może to spowodować nieoczekiwane zachowanie.|  
|[CA2122: Nie ujawniaj pośrednio metod żądaniami linkdemand](../code-quality/ca2122-do-not-indirectly-expose-methods-with-link-demands.md)|Element członkowski publiczny lub chroniony ma zapotrzebowanie na łącza i jest wywoływany przez element członkowski, który nie sprawdza zabezpieczeń. Zapotrzebowanie na łącza sprawdza uprawnienia tylko bezpośredniego wywołującego.|  
|[CA2123: Zastąpienia powinny być identyczne z bazowym](../code-quality/ca2123-override-link-demands-should-be-identical-to-base.md)|Ta reguła dopasowuje metodę do jej metody podstawowej, która jest interfejsem lub metodą wirtualną innego typu, a następnie porównuje zapotrzebowania na łącza na każdym z nich. Jeśli zasada ta jest naruszona, złośliwy wywołujący może pominąć zapotrzebowanie na łącza przez wywołanie niezabezpieczonej metody.|  
|[CA2124: Opakuj podatne na koniec klauzule w zewnętrznym spróbuj](../code-quality/ca2124-wrap-vulnerable-finally-clauses-in-outer-try.md)|Metoda publiczna lub chroniona zawiera blok try/finally. Wygląda na to, że blok finally resetuje stan zabezpieczeń i sam nie jest ujęty w bloku finally.|  
|[CA2126: Typ żądań konsolidacji wymaga żądań dziedziczenia](../code-quality/ca2126-type-link-demands-require-inheritance-demands.md)|Niezamknięty typ publiczny jest chroniony za pomocą zapotrzebowania na łącza i ma metodę, którą można zastąpić. Ani typ, ani metoda nie są chronione za pomocą żądania dziedziczenia.|  
|[CA2136: Elementy członkowskie nie powinny mieć skonfliktowanych adnotacji przezroczystości](../code-quality/ca2136-members-should-not-have-conflicting-transparency-annotations.md)|Krytyczny kod nie może wystąpić w zestawie, który jest w 100% przezroczysty. Ta reguła analizuje zestawy w 100% przezroczyste dla adnotacji SecurityCritical na poziomie typu, pola i metody.|  
|[CA2147: Jawne metody nie mogą używać zabezpieczeń potwierdzeń](../code-quality/ca2147-transparent-methods-may-not-use-security-asserts.md)|Reguła ta analizuje wszystkie metody i typy w zestawie, który jest w 100% przezroczysty lub mieszany przezroczysto-krytyczny i zaznacza deklaratywne lub imperatywne użycie potwierdzenia.|  
|[CA2140: Jawny kod nie może odwoływać elementów krytycznych dla zabezpieczeń](../code-quality/ca2140-transparent-code-must-not-reference-security-critical-items.md)|Metody, które są oznaczone przez atrybut SecurityTransparentAttribute, wywołują niepubliczne elementy członkowskie, które są oznaczone jako SecurityCritical. Ta reguła analizuje wszystkie metody i typy w zestawie mieszanym przezroczysto-krytycznym i oznacza wszelkie wywołania z przezroczystego kodu do niepublicznego krytycznego kodu, który nie jest oznaczony jako SecurityTreatAsSafe.|  
  
|[CA2130: Krytyczne stałe zabezpieczeń powinny być przezroczyste](../code-quality/ca2130-security-critical-constants-should-be-transparent.md)|Wymuszanie przezroczystości nie jest wymuszane dla wartości stałych, ponieważ kompilatory wbudowują stałe wartości, tak aby nie było wymagane żadne wyszukiwanie w czasie wykonywania. Stałe pola powinny być przezroczyste dla zabezpieczeń, tak aby recenzenci kodu nie zakładali, że przezroczysty kod nie może uzyskać dostępu do stałej.|  
|-----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|[CA2131: Typy krytyczne dla zabezpieczeń nie może uczestniczyć w równoważnikach typów](../code-quality/ca2131-security-critical-types-may-not-participate-in-type-equivalence.md)|Typ uczestniczy w równoważeniu typu i albo sam typ, albo jego element członkowski lub pole jest oznaczone atrybutem SecurityCriticalAttribute. Ta reguła jest uruchamiana na wszystkich typach krytycznych lub typach zawierających metody krytyczne lub pola, które uczestniczą w równoważeniu typu. Gdy CLR wykryje taki typ, uniemożliwia jego załadowanie, wywołując w czasie wykonywania wyjątek TypeLoadException. Zazwyczaj ta reguła uruchamiana jest tylko wtedy, gdy użytkownicy implementują równoważenie typu ręcznie, zamiast wykonać je, opierając się na otokach tlbimp i kompilatorach.|  
|[CA2132: Konstruktory domyślne muszą być co najmniej tak ważne, jak podstawowe konstruktory domyślne](../code-quality/ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors.md)|Typy i elementy członkowskie, które mają atrybut SecurityCriticalAttribute, nie mogą być używane przez kod aplikacji Silverlight. Typy krytyczne dla bezpieczeństwa i członkowie mogą być używani tylko przez zaufany kod w środowisku .NET Framework dla biblioteki klas Silverlight. Ze względu na to, że publiczna lub chroniona konstrukcja w klasie pochodnej musi mieć taką samą lub większą przejrzystość jak jej klasa podstawowa, klasy w aplikacji nie mogą pochodzić z klasy oznaczonej jako SecurityCritical.|  
|[CA2133: Delegatów należy powiązać z metodami ze spójną jawnością](../code-quality/ca2133-delegates-must-bind-to-methods-with-consistent-transparency.md)|To ostrzeżenie uruchamiane jest na metodzie wiążącej obiekt delegowany, oznaczony za pomocą atrybutu SecurityCriticalAttribute, do metody, która jest przezroczysta lub oznaczona za pomocą atrybutu SecuritySafeCriticalAttribute. Ostrzeżenie jest także uruchamiane na metodzie wiążącej obiekt delegowany, który jest przezroczysty lub bezpieczny-krytyczny dla metody krytycznej.|  
|[CA2134: Metody muszą przechowywać spójną jawność podczas nadpisywania metod bazowych](../code-quality/ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Ta reguła jest uruchamiana, gdy metoda oznaczona za pomocą atrybutu SecurityCriticalAttribute zastępuje metodę, która jest przezroczysta lub oznaczona za pomocą atrybutu SecuritySafeCriticalAttribute. Reguła ta jest również uruchamiana, gdy metoda przezroczysta lub oznaczona atrybutem SecuritySafeCriticalAttribute zastępuje metodę oznaczoną atrybutem SecurityCriticalAttribute. Reguła jest stosowana podczas zastępowania metody wirtualnej lub implementującej interfejs.|  
|[CA2135: Zestawy poziomu 2 nie powinny zawierać LinkDemands](../code-quality/ca2135-level-2-assemblies-should-not-contain-linkdemands.md)|LinkDemands są przestarzałe w zestawie reguł zabezpieczeń poziomu 2. Zamiast używania LinkDemands do wymuszenia zabezpieczeń w czasie kompilacji just in time (JIT), należy oznaczyć metody, typy i pola za pomocą atrybutu SecurityCriticalAttribute.|  
|[CA2136: Elementy członkowskie nie powinny mieć skonfliktowanych adnotacji przezroczystości](../code-quality/ca2136-members-should-not-have-conflicting-transparency-annotations.md)|Atrybuty przezroczystości są stosowane od elementów kodu o większym zakresie do elementów o mniejszym zakresie. Atrybuty przezroczystości elementów kodu z większym zakresem mają pierwszeństwo przed atrybutami przejrzystości elementów kodu, które są zawarte w pierwszym elemencie. Na przykład klasa, która jest oznaczona za pomocą atrybutu SecurityCriticalAttribute, nie może zawierać metody oznaczonej atrybutem SecuritySafeCriticalAttribute.|  
|[CA2137: Jawne metody muszą zawierać tylko weryfikowalne IL](../code-quality/ca2137-transparent-methods-must-contain-only-verifiable-il.md)|Metoda zawiera nieweryfikowalny kod lub zwraca typ przez odwołanie. Ta reguła jest uruchamiana podczas próby wykonywania przez kod przezroczysty pod względem zabezpieczeń nieweryfikowalnego MSIL (Microsoft Intermediate Language). Jednak reguła nie zawiera pełnej weryfikacji IL i używa heurystyki do wykrywania większości naruszeń weryfikacji MSIL.|  
|[CA2138: Jawne metody nie mogą wywoływać metod z atrybutem suppressunmanagedcodesecurity](../code-quality/ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute.md)|Metoda przezroczysta pod względem bezpieczeństwa wywołuje metodę, która jest oznaczona za pomocą atrybutu SuppressUnmanagedCodeSecurityAttribute.|  
|[CA2139: Jawne metody nie mogą używać atrybutu HandleProcessCorruptingExceptions](../code-quality/ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute.md)|Ta reguła jest wywoływana przez każdą metodę, która jest przejrzysta i próbuje obsłużyć wyjątek uszkodzenia procesu przy użyciu atrybutu HandleProcessCorruptedStateExceptionsAttribute. Wyjątek uszkadzający proces to klasyfikacja wyjątków CLR w wersji 4.0 wątków takich jak AccessViolationException. Atrybut HandleProcessCorruptedStateExceptionsAttribute może być używany tylko przez metody krytyczne pod względem bezpieczeństwa i będzie ignorowany, jeśli zostanie zastosowany do metody przezroczystej.|  
|[CA2140: Jawny kod nie może odwoływać elementów krytycznych dla zabezpieczeń](../code-quality/ca2140-transparent-code-must-not-reference-security-critical-items.md)|Element kodu, który jest oznaczony za pomocą atrybutu SecurityCriticalAttribute, jest krytyczny dla bezpieczeństwa. Przezroczysta metoda nie może użyć elementu krytycznego dla zabezpieczeń. Jeśli przezroczysty typ próbuje użyć typu krytycznego dla zabezpieczeń, zgłaszane są wyjątki TypeAccessException, MethodAccessException lub FieldAccessException.|  
|[CA2141: jawne metody nie mogą spełniać LinkDemands](../code-quality/ca2141-transparent-methods-must-not-satisfy-linkdemands.md)|Metoda przezroczysta pod względem zabezpieczeń wywołuje metodę z zestawu, która nie jest oznaczona atrybutem AllowPartiallyTrustedCallersAttribute (APTCA), lub metoda przezroczysta pod względem zabezpieczeń spełnia żądanie LinkDemand dla typu lub metody.|  
|[CA2142: Jawny kod nie powinien być chroniony za pomocą LinkDemands](../code-quality/ca2142-transparent-code-should-not-be-protected-with-linkdemands.md)|Ta reguła jest uruchamiana na przezroczystych metodach wymagających żądania LinkDemands, aby uzyskać do nich dostęp. Przezroczysty kod zabezpieczeń nie powinien być odpowiedzialny za weryfikację zabezpieczeń operacji, a zatem nie powinien wymagać uprawnień.|  
|[CA2143: Jawne metody nie powinny używać żądania kontroli zabezpieczeń](../code-quality/ca2143-transparent-methods-should-not-use-security-demands.md)|Przezroczysty kod zabezpieczeń nie powinien być odpowiedzialny za weryfikację zabezpieczeń operacji, a zatem nie powinien wymagać uprawnień. Przejrzysty pod względem bezpieczeństwa kod powinien używać pełnych żądań do podejmowania decyzji związanych z zabezpieczeniami, a kod krytyczny pod względem zabezpieczeń nie powinien opierać się na kodzie przezroczystym do wykonywania pełnego żądania.|  
|[CA2144: Jawny kod nie powinien ładować zestawów z tablic bajtowych](../code-quality/ca2144-transparent-code-should-not-load-assemblies-from-byte-arrays.md)|Przegląd zabezpieczeń dla kodu przezroczystego nie jest tak dokładny jak kodu krytycznego pod względem bezpieczeństwa, ponieważ przezroczysty kod nie może wykonywać czynności wrażliwych pod względem bezpieczeństwa. Zestawy, ładowane z tablicy bajtowej, mogą nie być niezauważone w przezroczystym kodzie, a ta tablica bajtów może zawierać krytyczny albo, co ważniejsze, krytyczny dla bezpieczeństwa kod, który powinien być poddany inspekcji.|  
|[CA2145: Jawne metody nie powinny być dekorowane za pomocą SuppressUnmanagedCodeSecurityAttribute](../code-quality/ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute.md)|Metody, które są oznaczone przez atrybut SuppressUnmanagedCodeSecurityAttribute, mają niejawne żądanie LinkDemand umieszczone na dowolnej metodzie, która je wywołuje. Ten element LinkDemand wymaga, aby kod wywołujący był krytyczny dla bezpieczeństwa. Oznaczanie metody, która używa zabezpieczenia SuppressUnmanagedCodeSecurity poprzez użycie atrybutu SecurityCriticalAttribute, sprawia, że wymóg ten jest bardziej oczywisty dla obiektów wywołujących metodę.|  
|[CA2146: Typy muszą być co najmniej tak ważne, jak ich typy podstawowe i interfejsy](../code-quality/ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)|Ta reguła jest uruchamiana, gdy typ pochodny ma atrybut przezroczystości pod względem zabezpieczeń, który nie jest tak krytyczny, jak jego typ podstawowy lub zaimplementowany interfejs. Tylko typy krytyczne pod względem zabezpieczeń mogą pochodzić od podstawowych typów krytycznych lub implementować interfejsy krytyczne, a tylko typy krytyczne lub krytyczne dla bezpieczeństwa mogą pochodzić od podstawowych typów krytycznych dla bezpieczeństwa lub implementować interfejsy krytyczne dla bezpieczeństwa.|  
|[CA2147: Jawne metody nie mogą używać zabezpieczeń potwierdzeń](../code-quality/ca2147-transparent-methods-may-not-use-security-asserts.md)|Kod, który jest oznaczony jako SecurityTransparentAttribute, nie ma przyznanego wystarczającego uprawnienia do potwierdzenia.|  
|[CA2149: Jawne metody nie mogą wywoływać kodu natywnego](../code-quality/ca2149-transparent-methods-must-not-call-into-native-code.md)|Ta reguła jest uruchamiana dla każdej przezroczystej metody, która wywołuje bezpośrednio kod natywny, na przykład przez metodę P/Invoke. Naruszenie tej zasady prowadzi do wyjątku MethodAccessException w poziomie 2 modelu przezroczystości i pełnego żądania dla UnmanagedCode w modelu przezroczystości poziomu 1.|  
|[CA2151: Pola typu krytycznego powinny być bezpieczne-krytyczne](../code-quality/ca2151-fields-with-critical-types-should-be-security-critical.md)|Aby używać typów krytycznych pod względem zabezpieczeń, kod odwołujący się do typu musi być albo krytyczny pod względem zabezpieczeń, albo bezpieczny-krytyczny pod względem zabezpieczeń. Ta zasada obowiązuje nawet w przypadku odwołania pośredniego. Dlatego pole mające zabezpieczenia przezroczyste lub pole bezpieczne-krytyczne pod względem zabezpieczeń jest mylące, ponieważ przezroczysty kod nadal nie będzie mógł uzyskać dostępu do pola.|  
|[Deklaracje CA5122 P/Invoke nie powinny być bezpieczne krytyczne](../code-quality/ca5122-p-invoke-declarations-should-not-be-safe-critical.md)|Metody są oznaczone jako SecuritySafeCritical, gdy wykonują operacje zależne od zabezpieczeń, ale mogą być również bezpiecznie używane przez kod przezroczystości. Kod przezroczystości może nigdy bezpośrednio nie wywołać kodu natywnego za pośrednictwem metody P/Invoke. Dlatego oznakowanie metody P/Invoke jako bezpiecznej-krytycznej pod względem zabezpieczeń nie umożliwi jej wywołania kodu przezroczystości i jest mylące dla analizy zabezpieczeń.|  
|[CA2153: Unikaj Obsługa wyjątków stan uszkodzony](../code-quality/ca2153-avoid-handling-corrupted-state-exceptions.md)|[Uszkodzony rozszerzenie stanu wyjątków (klienta)](https://msdn.microsoft.com/en-us/magazine/dd419661.aspx) wskazać, że pamięć uszkodzenie istnieje w procesie. Przechwytywanie tych zamiast zezwolenia na awarii procesu może prowadzić do luk w zabezpieczeniach, jeśli osoba atakująca może wykorzystać do obszaru uszkodzenia pamięci.|  
|[CA3075: Przetwarzanie DTD niezabezpieczonych](../code-quality/ca3075-insecure-dtd-processing.md)|Użyj niezabezpieczonych wystąpień DTDProcessing lub odwołania do jednostki zewnętrznej źródeł, analizator może zaakceptować niezaufanych danych wejściowych i wyjawiać poufnych informacji do osoby atakujące.|  
|[CA3076: Wykonywanie skryptu niezabezpieczonych XSLT](../code-quality/ca3076-insecure-xslt-script-execution.md)|Jeśli nimi wykonane arkusze stylów języka przekształcenia XSLT (Extensible) w aplikacjach .NET, procesor może rozwiązać niezaufanych odwołań do identyfikatora URI, które można ujawnić poufne informacje do osoby atakujące, co może prowadzić do odmowy usługi i Cross-Site ataki.|  
|[CA3077: Przetwarzanie niezabezpieczonych projekt interfejsu API, dokument XML i czytnika tekstu XML](../code-quality/ca3077-insecure-processing-in-api-design-xml-document-and-xml-text-reader.md)|Projektowanie interfejsu API otrzymane z XMLDocument i klasy XMLTextReader, można w trosce o DtdProcessing.  Za pomocą niezabezpieczonego DTDProcessing wystąpień, gdy odwołuje się do rozpoznawania źródeł zewnętrznej jednostki lub ustawienie niezabezpieczonych wartości w pliku XML może prowadzić do ujawnienie informacji.|