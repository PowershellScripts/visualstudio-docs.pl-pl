---
title: 'CA1724: Nazwy typów nie powinny odpowiadać nazwom | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- TypeNamesShouldNotMatchNamespaces
- CA1724
helpviewer_keywords:
- TypeNamesShouldNotMatchNamespaces
- CA1724
ms.assetid: 329af3b5-5600-4101-831d-531ab3eb7060
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 64999653e326cc99ca9b1880966406dde41ce52e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49246770"
---
# <a name="ca1724-type-names-should-not-match-namespaces"></a>CA1724: Nazwy typów nie powinny odpowiadać nazwom pól
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|TypeNamesShouldNotMatchNamespaces|
|CheckId|CA1724|
|Kategoria|Microsoft.Naming|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Nazwa typu odpowiada [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] nazwy przestrzeni nazw w porównania bez uwzględniania wielkości liter.

## <a name="rule-description"></a>Opis reguły
 Nazwy typów nie powinny odpowiadać nazwom przestrzeni nazw, które są zdefiniowane w [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] biblioteki klas. Naruszenie tej zasady może zmniejszyć użyteczność biblioteki.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Wybierz nazwę typu, który nie jest zgodna z nazwą elementu [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] biblioteki klas w przestrzeni nazw.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 W nowych wdrożeniach Brak znanego scenariusze wystąpić, gdy trzeba Pomijaj ostrzeżeń dla tej reguły. Zanim można pominąć to ostrzeżenie, zastanów się, jak użytkownicy biblioteki mogą być pomylone według tej nazwy. Do wysłania biblioteki, trzeba będzie Pomijaj ostrzeżeń dla tej reguły.



