---
title: Korzystanie z atrybutu DebuggerTypeProxy | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- attributes [C#], debugger
- DebuggerTypeProxyAttribute class
- DebuggerTypeProxy attribute
ms.assetid: 943f3bb1-993e-4800-a47e-0af78b063014
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ab54c754fdc3b7ae773e71a96936a1c17c6bc5ce
ms.sourcegitcommit: 9571742f4a808c75b1034aa72fc24b54bc50692e
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/18/2018
ms.locfileid: "49411069"
---
# <a name="using-debuggertypeproxy-attribute"></a>Korzystanie z atrybutu DebuggerTypeProxy

<xref:System.Diagnostics.DebuggerTypeProxyAttribute> Określa serwer proxy lub podstawiony dla typu i zmiany, które jej typ jest wyświetlana w oknach debugera. Po wyświetleniu zmiennej, która ma serwer proxy serwera proxy oznacza oryginalnego typu w **wyświetlić**. W oknie zmiennych debugera zostaną wyświetlone tylko publiczne składowe typ serwera proxy. Prywatne elementy członkowskie nie są wyświetlane.

Ten atrybut można zastosować do:

- Struktury
- Klasy
- Zestawy

Klasa proxy typu musi mieć konstruktora, który przyjmuje argument typu, który zastąpi serwer proxy. Debuger tworzy nowe wystąpienie klasy proxy typu za każdym razem, gdy wymaganych, aby wyświetlić zmienną typu docelowego. Może to mieć wpływ na wydajność. W rezultacie nie należy przeprowadzać więcej pracy w Konstruktorze niż jest to absolutnie konieczne.

Aby zminimalizować spadku wydajności, Ewaluator wyrażeń nie analizuje atrybuty na serwerze proxy wyświetlania tego typu, chyba że typ jest rozwinięta, użytkownika, klikając pozycję + symboli w oknie debugera lub przy użyciu <xref:System.Diagnostics.DebuggerBrowsableAttribute>. W związku z tym nie należy umieszczać atrybutów na sam typ wyświetlania. Atrybuty można i powinny być używane w treści typ wyświetlania.

Dobrym rozwiązaniem dla obiektu pośredniczącego typu jako prywatne klasa zagnieżdżona w klasie, docelowe atrybuty. Dzięki temu można łatwo dostęp do wewnętrznych składowych.

<xref:System.Diagnostics.DebuggerTypeProxyAttribute> mogą być dziedziczone, więc jeśli serwer proxy typ jest określony w klasie bazowej będzie stosowana do dowolnej klasy pochodnej, chyba że te klasy pochodne określić własne pośredniczącego typu.

Jeśli <xref:System.Diagnostics.DebuggerTypeProxyAttribute> jest używana na poziomie zestawu `Target` parametr określa typ, który zastąpi serwer proxy.

Aby uzyskać przykład sposobu użycia tego atrybutu, wraz z <xref:System.Diagnostics.DebuggerDisplayAttribute> i <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, zobacz[korzystanie z atrybutu DebuggerDisplay](../debugger/using-the-debuggerdisplay-attribute.md).

## <a name="using-generics-with-debuggertypeproxy"></a>Za pomocą typów ogólnych za pomocą DebuggerTypeProxy

Obsługa typów ogólnych jest ograniczona. Dla języka C# `DebuggerTypeProxy` obsługuje tylko Otwórz typy. Typem otwartym, jest określana skrótem typu unconstructed jest typ ogólny, który nie utworzono wystąpienia z argumentami dla jego parametrów typu. Zamknięte typy, nazywany również typy utworzone, nie są obsługiwane.

Składnia służąca do typu otwartego wygląda następująco:

`Namespace.TypeName<,>`

Jeśli używasz typu ogólnego jako cel w `DebuggerTypeProxy`, należy użyć następującej składni. `DebuggerTypeProxy` Mechanizm wnioskuje parametrów typu dla Ciebie.

Aby uzyskać więcej informacji o typach otwarte i zamknięte w języku C# zobacz [specyfikacji języka C#](/dotnet/csharp/language-reference/language-specification), otwórz sekcję 20.5.2 i zamknięte typy.

Visual Basic nie ma składni typu otwartego, więc nie możesz zrobić to samo w języku Visual Basic. Zamiast tego należy użyć ciąg reprezentujący nazwę typu otwartego.

`"Namespace.TypeName'2"`

## <a name="see-also"></a>Zobacz też

- [Używanie atrybutu DebuggerDisplay](../debugger/using-the-debuggerdisplay-attribute.md)
- [Tworzenie niestandardowych widoków obiektów .managed](../debugger/create-custom-views-of-dot-managed-objects.md)
- [Udoskonalanie debugowania za pomocą atrybutów wyświetlania debugera](/dotnet/framework/debug-trace-profile/enhancing-debugging-with-the-debugger-display-attributes)
