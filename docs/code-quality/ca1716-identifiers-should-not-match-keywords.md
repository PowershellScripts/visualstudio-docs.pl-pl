---
title: 'CA1716: Identyfikatory nie powinny odpowiadać słowom kluczowym'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
helpviewer_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
ms.assetid: 900cc8a1-1089-4069-a4ce-10b109ac4fab
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cfaef87f8463c43c412c5db3c83a899fb22b4f66
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49862440"
---
# <a name="ca1716-identifiers-should-not-match-keywords"></a>CA1716: Identyfikatory nie powinny odpowiadać słowom kluczowym

|||
|-|-|
|TypeName|IdentifiersShouldNotMatchKeywords|
|CheckId|CA1716|
|Kategoria|Microsoft.Naming|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna

Nazwa przestrzeni nazw, typu lub elementu członkowskiego viritual lub interfejs odpowiada zastrzeżonym słowem kluczowym w języku programowania.

## <a name="rule-description"></a>Opis reguły

Identyfikatory przestrzeni nazw, typów, jak i wirtualnych i składowe interfejsu nie powinny odpowiadać słowom, które są definiowane przez języki przeznaczone dla środowiska uruchomieniowego języka wspólnego. W zależności od języka, który jest używany i słowo kluczowe błędy kompilatora i niejednoznaczności może utrudnić bibliotekę do użycia.

Ta reguła sprawdza, czy przed słów kluczowych w następujących językach:

- Visual Basic

- C#

- C++/CLI

Porównanie bez uwzględniania wielkości liter jest używana do [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] słów kluczowych i porównywanie uwzględniające wielkość liter jest używana w innych językach.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia

Wybierz nazwę, która nie ma na liście słów kluczowych.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia

Ostrzeżenie od tej reguły można pominąć, jeśli są przekonane, że identyfikator nie należy mylić użytkowników interfejsu API i czy biblioteki można używać we wszystkich językach w programie .NET Framework.