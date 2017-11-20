---
title: "CA1714: Typy wyliczeniowe flag powinny mieć nazwy w liczbie mnogiej | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- FlagsEnumsShouldHavePluralNames
- CA1714
helpviewer_keywords:
- CA1714
- FlagsEnumsShouldHavePluralNames
ms.assetid: 95ef5b43-7681-49e9-a5a3-ac0357cf1be7
caps.latest.revision: "14"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b83cb82dab5f723c656b51a5322df7d7aad4570c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1714-flags-enums-should-have-plural-names"></a>CA1714: Typy wyliczeniowe flag powinny mieć nazwy w liczbie mnogiej
|||  
|-|-|  
|TypeName|FlagsEnumsShouldHavePluralNames|  
|CheckId|CA1714|  
|Kategoria|Microsoft.Naming|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Wyliczenie publiczne ma <xref:System.FlagsAttribute?displayProperty=fullName> i jego nazwa nie kończy się w jego ".  
  
## <a name="rule-description"></a>Opis reguły  
 Typy, które są oznaczone ikoną z <xref:System.FlagsAttribute> mają nazwy, które nie są mnogiej, ponieważ ten atrybut wskazuje, że można określić więcej niż jedną wartość. Na przykład wyliczenie definiuje dni tygodnia może być przeznaczona do użycia w aplikacji, której można określić wiele dni. To wyliczenie ma <xref:System.FlagsAttribute> i można go wywołać "Dni". Wyliczenie podobne, która umożliwia określenie tylko jednego dnia nie może mieć atrybut — można wywołać "Dzień".  
  
 Konwencje nazewnictwa Podaj wygląd wspólnej dla bibliotek przeznaczonych środowisko uruchomieniowe języka wspólnego. Zmniejsza to nauki jest wymagany dla nowej biblioteki oprogramowania, którą można tworzyć bardziej niezawodne klienta, czy biblioteka został opracowany przez osobę, która ma doświadczenia w rozwijającym się kodu zarządzanego.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Wprowadź nazwę wyliczenia mnogiej programu word lub usuń <xref:System.FlagsAttribute> atrybut, jeśli wiele wartości wyliczenia nie można określić jednocześnie.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Można bezpiecznie pominąć naruszenie, jeśli nazwa jest słowem mnogiej, ale nie kończy się na ". Na przykład jeśli wyliczenie wiele dni, który został opisany wcześniej nazwany "DaysOfTheWeek", to naruszyć logiką reguły, ale nie jej celem. Te naruszenia powinny być suppressd.  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1027: Oznaczaj wyliczenia za pomocą FlagsAttribute](../code-quality/ca1027-mark-enums-with-flagsattribute.md)  
  
 [CA2217: Nie oznaczaj typów wyliczeniowych atrybutem FlagsAttribute](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.FlagsAttribute?displayProperty=fullName>   
 [Projekt wyliczenia](/dotnet/standard/design-guidelines/enum)