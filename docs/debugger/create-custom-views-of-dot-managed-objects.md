---
title: "Tworzenie niestandardowych widoków obiektów zarządzanych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.data.elements
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- data types [C#], custom
- custom data types
- managed code, custom data types
- autoexp.dat file
- mcee_cs.dat file
- debugger, expanding data types
- mcee_mc.dat file
ms.assetid: 9969e9b2-9008-4729-8a14-0d6deaa61576
caps.latest.revision: "34"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ae3149350bac7aca92ffbc8b308c75357c3edba4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="create-custom-views-of-managed-objects"></a>Tworzenie niestandardowych widoków obiektów zarządzanych
Można dostosować sposób Visual Studio Wyświetla typy danych w oknach zmiennych debugera.  
  
## <a name="attributes"></a>Atrybuty  
 W języku C# i Visual Basic, można dodać rozszerzenia do niestandardowych danych przy użyciu <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, <xref:System.Diagnostics.DebuggerDisplayAttribute>, i <xref:System.Diagnostics.DebuggerBrowsableAttribute>.  
  
 W [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)] kodu języka Visual Basic nie obsługuje atrybutu DebuggerBrowsable. To ograniczenie zostało usunięte w nowszych wersjach systemu .NET Framework.  
  
## <a name="visualizers"></a>Wizualizatory  
 Można napisać wizualizatora, aby wyświetlić dowolny typ danych zarządzanych. Aby uzyskać więcej informacji, zobacz [porady: pisanie wizualizatora](../debugger/how-to-write-a-visualizer.md).  
  
## <a name="native-code"></a>Kod natywny  
 Dla kodu natywnego można dodać rozszerzenia typu danych niestandardowych do autoexp.dat — plik, który znajduje się w katalogu 11.0\Common7\Packages\Debugger Program Files\Microsoft Visual Studio. Instrukcje dotyczące sposobu zapisu `autoexp` zasady znajdują się w samym pliku.  
  
> [!CAUTION]
>  Struktura tego pliku i składni reguł autoexp może zmienić od wydania programu Visual Studio do następnego.  
  
 Typ macierzysty widoków można również dostosować pisząc expression evaluator dodatku. Aby uzyskać więcej informacji, zobacz [EEAddIn próbki: debugowanie Expression Evaluator Add-In](http://msdn.microsoft.com/en-us/d4f6b068-c812-45bc-9ec0-7e0363c4bb9e).  
  
## <a name="see-also"></a>Zobacz też  
 [Korzystanie z atrybutu DebuggerTypeProxy](../debugger/using-debuggertypeproxy-attribute.md)   
 [Za pomocą atrybutu DebuggerDisplay](../debugger/using-the-debuggerdisplay-attribute.md)   
 [Oglądanie i QuickWatch systemu Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Udoskonalanie debugowania za pomocą atrybutów wyświetlania debugera](/dotnet/framework/debug-trace-profile/enhancing-debugging-with-the-debugger-display-attributes)