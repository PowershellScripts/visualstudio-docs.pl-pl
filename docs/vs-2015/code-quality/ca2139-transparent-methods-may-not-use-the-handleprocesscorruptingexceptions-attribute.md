---
title: 'CA2139: Metody przezroczyste nie mogą używać atrybutu HandleProcessCorruptingExceptions | Dokumentacja firmy Microsoft'
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
- CA2139
ms.assetid: 45a0328a-add7-40f9-8934-dff59beb02b3
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b7780698296815da73b9862b586bc256a87f7d42
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49827066"
---
# <a name="ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute"></a>CA2139: Jawne metody mogą nie używać atrybutu HandleProcessCorruptingExceptions
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TransparentMethodsMustNotHandleProcessCorruptingExceptions|
|CheckId|CA2139|
|Kategoria|Microsoft.Security|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Metoda przezroczysta pod względem jest oznaczona atrybutem <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> atrybutu.

## <a name="rule-description"></a>Opis reguły
 Ta reguła jest uruchamiana każdą metodę, która jest przejrzysta i próbuje obsłużyć wyjątek uszkadzający proces przy użyciu <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> atrybutu. Wyjątek uszkadzający proces to klasyfikacja wyjątków CLR w wersji 4.0 wyjątków takich <xref:System.AccessViolationException>. Atrybut HandleProcessCorruptedStateExceptionsAttribute może być używany tylko przez metody krytyczne pod względem bezpieczeństwa i będzie ignorowany, jeśli zostanie zastosowany do metody przezroczystej. Aby obsłużyć wyjątki błędny procesu, ta metoda musi stać się krytyczny pod względem zabezpieczeń lub bezpieczny krytyczny dla bezpieczeństwa.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, Usuń <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> atrybut lub oznaczyć metody <xref:System.Security.SecurityCriticalAttribute> lub <xref:System.Security.SecuritySafeCriticalAttribute> atrybutu.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły.

## <a name="example"></a>Przykład
 W tym przykładzie metoda przezroczysta pod względem jest oznaczony za pomocą <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> atrybutu i zakończy się niepowodzeniem reguły. Metoda również powinien być oznaczony przez <xref:System.Security.SecurityCriticalAttribute> lub <xref:System.Security.SecuritySafeCriticalAttribute> atrybutu.

 [!code-csharp[FxCop.Security.CA2139.TransparentMethodsMustNotHandleProcessCorruptingExceptions#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2139.transparentmethodsmustnothandleprocesscorruptingexceptions/cs/ca2139 - transparentmethodsmustnothandleprocesscorruptingexceptions.cs#1)]



