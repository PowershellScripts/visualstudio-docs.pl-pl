---
title: 'CA2138: Jawne metody nie mogą wywoływać metod z atrybutem SuppressUnmanagedCodeSecurity'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2138
ms.assetid: a14c4d32-f079-4f3a-956c-a1657cde0f66
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- cplusplus
ms.openlocfilehash: 3ba7a1c25387349ba78b198a37b709d6bdd10b64
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49948638"
---
# <a name="ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute"></a>CA2138: Jawne metody nie mogą wywoływać metod z atrybutem SuppressUnmanagedCodeSecurity

|||
|-|-|
|TypeName|TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods|
|CheckId|CA2138|
|Kategoria|Microsoft.Security|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Metoda przezroczysta pod względem bezpieczeństwa wywołuje metodę, która jest oznaczona za pomocą <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> atrybutu.

## <a name="rule-description"></a>Opis reguły
 Ta reguła jest uruchamiana na każdej przezroczystej metody metodę, która wywołuje bezpośrednio kod natywny, na przykład za pomocą metody P/Invoke (Wywołanie platformy) wywołań. P/Invoke i COM międzyoperacyjny metody, które są oznaczone <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> atrybutu wynik na liście LinkDemand wykonywana względem wywoływania metody. Ponieważ przezroczysty kod zabezpieczeń nie mogą spełniać LinkDemands, kod również nie można wywołać metody, które są oznaczone atrybutem SuppressUnmanagedCodeSecurity lub metody klasy, która jest oznaczona atrybutem SuppressUnmanagedCodeSecurity. Metoda zakończy się niepowodzeniem lub żądanie zostaną przekonwertowane na pełnego żądania.

 Naruszenie tej zasady prowadzi do <xref:System.MethodAccessException> zabezpieczeń na poziomie 2 modelu przezroczystości i pełnego żądania dla <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> w modelu przezroczystości poziomu 1.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, Usuń <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> atrybutu i oznacz metodę z <xref:System.Security.SecurityCriticalAttribute> lub <xref:System.Security.SecuritySafeCriticalAttribute> atrybutu.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły.

## <a name="example"></a>Przykład
 [!code-csharp[FxCop.Security.CA2138.TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods#1](../code-quality/codesnippet/CSharp/ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute_1.cs)]