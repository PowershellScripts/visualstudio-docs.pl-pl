---
title: 'CA1401: P-Invoke nie powinny być widoczne | Dokumentacja firmy Microsoft'
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
- PInvokesShouldNotBeVisible
- CA1401
helpviewer_keywords:
- CA1401
- PInvokesShouldNotBeVisible
ms.assetid: 0f4d96c1-f9de-414e-b223-4dc7f691bee3
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1b811f57a3939a026152e70babbf263244aed056
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49211701"
---
# <a name="ca1401-pinvokes-should-not-be-visible"></a>CA1401: P/Invokes nie powinny być widoczne
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|PInvokesShouldNotBeVisible|
|CheckId|CA1401|
|Kategoria|Microsoft.Interoperability|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Metoda publiczna lub chroniona w typie publicznym ma <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName> atrybutu (również implementowany przez `Declare` — słowo kluczowe w [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]).

## <a name="rule-description"></a>Opis reguły
 Metody, które są oznaczone <xref:System.Runtime.InteropServices.DllImportAttribute> atrybutów (lub metody, które są zdefiniowane przy użyciu `Declare` — słowo kluczowe w [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]) umożliwia dostęp do kodu niezarządzanego platformę wywołania usług. Takie metody nie powinny być udostępniane. Dzięki przechowywaniu tych metod, prywatne lub wewnętrzne, należy upewnić się, że biblioteki nie można użyć do naruszenia bezpieczeństwa, umożliwiając dostęp do niezarządzanych interfejsów API, który może nie wywoływać w przeciwnym razie obiekty wywołujące.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, należy zmienić poziom dostępu do metody.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły.

## <a name="example"></a>Przykład
 Poniższy przykład deklaruje metodę, która narusza tę regułę.

 [!code-csharp[FxCop.Interoperability.DllImports#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.DllImports/cs/FxCop.Interoperability.DllImports.cs#1)]
 [!code-vb[FxCop.Interoperability.DllImports#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Interoperability.DllImports/vb/FxCop.Interoperability.DllImports.vb#1)]



