---
title: "CA2115: Wywołaj GC. KeepAlive, gdy używasz zasobów natywnych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CallGCKeepAliveWhenUsingNativeResources
- CA2115
helpviewer_keywords:
- CA2115
- CallGCKeepAliveWhenUsingNativeResources
ms.assetid: f00a59a7-2c6a-4bbe-a1b3-7bf77d366f34
caps.latest.revision: "18"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 98833f1feccd70c3bdf140b4d2be7a4ad1a5d6bf
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2115-call-gckeepalive-when-using-native-resources"></a>CA2115: Wywołaj GC.KeepAlive gdy używasz zasobów natywnych
|||  
|-|-|  
|TypeName|CallGCKeepAliveWhenUsingNativeResources|  
|CheckId|CA2115|  
|Kategoria|Microsoft.Security|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Metody zadeklarowane w typie z finalizatorem odwołuje się do <xref:System.IntPtr?displayProperty=fullName> lub <xref:System.UIntPtr?displayProperty=fullName> pól, ale nie wywołuje <xref:System.GC.KeepAlive%2A?displayProperty=fullName>.  
  
## <a name="rule-description"></a>Opis reguły  
 Wyrzucanie elementów bezużytecznych Kończenie znajdujących obiektu, jeśli w kodzie zarządzanym nie Brak odwołań do niego. Niezarządzane odwołania do obiektów nie uniemożliwiają wyrzucanie elementów bezużytecznych. Ta reguła wykrywa błędy, które mogą wystąpić, ponieważ kończy się działanie niezarządzanego zasobu, a wciąż jest on używany w kodzie niezarządzanym.  
  
 Ta zasada przy założeniu, że <xref:System.IntPtr> i <xref:System.UIntPtr> pól Zapisz wskaźniki do niezarządzanych zasobów. Ponieważ finalizator ma na celu zwolnienie niezarządzanych zasobów, reguła przyjęto założenie, że finalizator zwolni niezarządzanego zasobu wskazywana przez wskaźnik pola. Ta zasada założono również, że metoda odwołuje się do pola wskaźnika do przekazania do niezarządzanego kodu niezarządzanego zasobu.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, dodaj wywołanie <xref:System.GC.KeepAlive%2A> do metody, przekazywanie bieżącego wystąpienia (`this` w języku C# i C++) jako argumentu. Umieść wywołanie po ostatnim wierszu kodu, gdzie obiekt musi być chroniony z wyrzucanie elementów bezużytecznych. Natychmiast po wywołaniu <xref:System.GC.KeepAlive%2A>, obiekt ponownie jest uznawany za gotowe do wyrzucanie elementów bezużytecznych, przy założeniu, że nie nie zarządzanych odwołania do niego.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Ta reguła zapewnia pewne założenia, które mogą prowadzić do fałszywych alarmów. Ostrzeżenie od tej reguły można bezpiecznie pominąć, jeśli:  
  
-   Finalizator nie spowoduje zwolnienia zawartość <xref:System.IntPtr> lub <xref:System.UIntPtr> odwołania przez metodę pola.  
  
-   Metoda nie zostały spełnione <xref:System.IntPtr> lub <xref:System.UIntPtr> pole do kodu niezarządzanego.  
  
 Dokładnie sprawdź inne komunikaty przed wyłączając je. Ta zasada wykrywa błędy, które są trudne do odtworzenia i debugowania.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie `BadMethod` nie zawiera wywołanie `GC.KeepAlive` i dlatego narusza zasady. `GoodMethod`zawiera kod poprawiony.  
  
> [!NOTE]
>  W tym przykładzie jest pseudo-kodu, chociaż kod kompiluje i uruchamia, ostrzeżenia nie jest uruchamiany, ponieważ nie utworzony lub zwolnienie niezarządzanych zasobów.  
  
 [!code-csharp[FxCop.Security.IntptrAndFinalize#1](../code-quality/codesnippet/CSharp/ca2115-call-gc-keepalive-when-using-native-resources_1.cs)]  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.GC.KeepAlive%2A?displayProperty=fullName>   
 <xref:System.IntPtr?displayProperty=fullName>   
 <xref:System.Object.Finalize%2A?displayProperty=fullName>   
 <xref:System.UIntPtr?displayProperty=fullName>   
 [Wzorzec Dispose](/dotnet/standard/design-guidelines/dispose-pattern)