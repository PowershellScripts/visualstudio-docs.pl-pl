---
title: "CA2149: Jawne metody nie mogą wywoływać kodu natywnego | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CA2149
ms.assetid: 28951bd7-f3db-4871-99aa-bad68d1ead80
caps.latest.revision: "11"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 937b6c203b7ee5a2dbe2c77ba1c67ca7500c1fa4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2149-transparent-methods-must-not-call-into-native-code"></a>CA2149: Jawne metody nie mogą wywoływać kodu natywnego
|||  
|-|-|  
|TypeName|TransparentMethodsMustNotCallNativeCode|  
|CheckId|CA2149|  
|Kategoria|Microsoft.Security|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Metoda wywołania funkcji macierzystej za pośrednictwem szkieletu metody, takie jak P/Invoke.  
  
## <a name="rule-description"></a>Opis reguły  
 Ta reguła jest uruchamiana dla każdej przezroczystej metody, która wywołuje bezpośrednio kod natywny, na przykład przez metodę P/Invoke. Naruszeń tej reguły prowadzić do <xref:System.MethodAccessException> w modelu przezroczystość poziomu 2 i pełne żądanie dla <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> w modelu przezroczystość poziomu 1.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, oznacz metodę, która wywołuje kodu natywnego z <xref:System.Security.SecurityCriticalAttribute> lub <xref:System.Security.SecuritySafeCriticalAttribute> atrybutu.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Nie pomijaj ostrzeżeń dla tej reguły.  
  
## <a name="example"></a>Przykład  
 [!code-csharp[FxCop.Security.CA2149.TransparentMethodsMustNotCallNativeCode#1](../code-quality/codesnippet/CSharp/ca2149-transparent-methods-must-not-call-into-native-code_1.cs)]