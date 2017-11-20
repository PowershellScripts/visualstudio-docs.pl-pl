---
title: "CA1032: Implementowanie standardowych konstruktorów wyjątków | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1032
- ImplementStandardExceptionConstructors
helpviewer_keywords:
- CA1032
- ImplementStandardExceptionConstructors
ms.assetid: a8623c56-273a-4c95-8d83-95911a042be7
caps.latest.revision: "16"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7300465ce9cef97cf322a7667e775852e22edb4e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1032-implement-standard-exception-constructors"></a>CA1032: Implementowanie standardowych konstruktorów wyjątków
|||  
|-|-|  
|TypeName|ImplementStandardExceptionConstructors|  
|CheckId|CA1032|  
|Kategoria|Microsoft.Design|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Rozszerza typ <xref:System.Exception?displayProperty=fullName> i nie deklaruje wszystkie wymagane konstruktorów.  
  
## <a name="rule-description"></a>Opis reguły  
 Typy wyjątków musi implementować następujących konstruktorów:  
  
-   NewException() publiczne  
  
-   NewException(string) publiczne  
  
-   publiczny NewException (ciąg, wyjątków)  
  
-   NewException chroniona lub prywatnej (SerializationInfo, StreamingContext)  
  
 Niepowodzenie podczas dostarczenia pełnego zestawu konstruktorów może utrudnić poprawną obsługę wyjątków. Na przykład konstruktora, który ma podpis `NewException(string, Exception)` służy do tworzenia wyjątki, które są spowodowane przez inne wyjątki. Bez tego konstruktora nie może utworzyć i zgłosić wystąpienia niestandardowego wyjątku, który zawiera wyjątek wewnętrzny (zagnieżdżonych), która jest w takiej sytuacji należy wykonać, jakie kodu zarządzanego. Pierwszy konstruktorów wyjątków trzy są publicznie udostępniane przez Konwencję. Konstruktor czwarty jest chroniona w niezapieczętowanych klas i prywatny w klasie zapieczętowanej. Aby uzyskać więcej informacji, zobacz [CA2229: zaimplementować konstruktory serializacji](../code-quality/ca2229-implement-serialization-constructors.md)  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, Dodaj brakujące konstruktory wyjątek i upewnij się, że poprawne ułatwień dostępu.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Jest to bezpieczne Pomiń ostrzeżenie od tej reguły, gdy naruszenie jest spowodowany przy użyciu poziomu dostępu różnych dla konstruktorów publicznych.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład zawiera typ wyjątku, który narusza tę regułę i typ wyjątku, który jest poprawnie zaimplementowana.  
  
 [!code-csharp[FxCop.Design.ExceptionMultipleCtors#1](../code-quality/codesnippet/CSharp/ca1032-implement-standard-exception-constructors_1.cs)]