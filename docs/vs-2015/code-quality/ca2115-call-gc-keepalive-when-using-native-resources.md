---
title: 'CA2115: Wywołaj GC. KeepAlive podczas korzystania z zasobów natywnych | Dokumentacja firmy Microsoft'
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
- CallGCKeepAliveWhenUsingNativeResources
- CA2115
helpviewer_keywords:
- CA2115
- CallGCKeepAliveWhenUsingNativeResources
ms.assetid: f00a59a7-2c6a-4bbe-a1b3-7bf77d366f34
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e8f45b188945febcd3c81fc4be6a9427d8fe94ba
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49948749"
---
# <a name="ca2115-call-gckeepalive-when-using-native-resources"></a>CA2115: Wywołaj GC.KeepAlive gdy używasz zasobów natywnych
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|CallGCKeepAliveWhenUsingNativeResources|
|CheckId|CA2115|
|Kategoria|Microsoft.Security|
|Zmiana kluczowa|Bez podziału|

## <a name="cause"></a>Przyczyna
 Metody zadeklarowane w typie z finalizatorem odwołuje się do <xref:System.IntPtr?displayProperty=fullName> lub <xref:System.UIntPtr?displayProperty=fullName> pola, ale nie mogą wywoływać <xref:System.GC.KeepAlive%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Opis reguły
 Kończenie znajdujących obiektu wyrzucania elementów bezużytecznych, jeśli Brak odwołań do niego w kodzie zarządzanym. Niezarządzane odwołania do obiektów nie uniemożliwiają wyrzucania elementów bezużytecznych. Ta reguła wykrywa błędy, które mogą wystąpić, ponieważ kończy się działanie niezarządzanego zasobu, a wciąż jest on używany w kodzie niezarządzanym.

 Reguła ta zakłada, że <xref:System.IntPtr> i <xref:System.UIntPtr> pola Zapisz wskaźniki do niezarządzanych zasobów. Ponieważ finalizator ma na celu zwolnienie niezarządzanych zasobów, reguła zakłada, że finalizator zwolni niezarządzany zasób wskazywany przez wskaźnik pola. Reguła ta zakłada również, że metoda odwołuje się do pola wskaźnika do przekazania niezarządzany zasób do kodu niezarządzanego.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, należy dodać wywołanie <xref:System.GC.KeepAlive%2A> do metody, przekazując bieżącego wystąpienia (`this` w języku C# i C++) jako argument. Umieść wywołanie po ostatni wiersz kodu, gdzie obiekt muszą być chronione z wyrzucania elementów bezużytecznych. Natychmiast po wywołaniu <xref:System.GC.KeepAlive%2A>, obiekt ponownie jest uznawane za gotowe do wyrzucania elementów bezużytecznych, przy założeniu, że istnieją nie zarządzanych odwołania do niego.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Ta reguła zapewnia pewne założenia, które mogą prowadzić do wyników fałszywie dodatnich. Ostrzeżenie od tej reguły można bezpiecznie pominąć, jeśli:

- Finalizator nie spowoduje zwolnienia zawartość <xref:System.IntPtr> lub <xref:System.UIntPtr> przywoływane przez metody pól.

- Metoda nie zostały spełnione <xref:System.IntPtr> lub <xref:System.UIntPtr> pola do kodu niezarządzanego.

  Uważnie przeczytaj innych komunikatów przed ich wykluczenie. Ta zasada wykrywa błędy, które są trudne do odtworzenia i debugowania.

## <a name="example"></a>Przykład
 W poniższym przykładzie `BadMethod` nie zawiera wywołanie `GC.KeepAlive` i dlatego narusza regułę. `GoodMethod` zawiera kod poprawiony.

> [!NOTE]
>  W tym przykładzie jest pseudo-kodu, mimo że kod kompiluje i uruchamia, ostrzeżenie nie jest uruchamiany, ponieważ niezarządzany zasób zostanie utworzony lub nie zwolniona.

 [!code-csharp[FxCop.Security.IntptrAndFinalize#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.IntptrAndFinalize/cs/FxCop.Security.IntptrAndFinalize.cs#1)]

## <a name="see-also"></a>Zobacz też
 <xref:System.GC.KeepAlive%2A?displayProperty=fullName><xref:System.IntPtr?displayProperty=fullName>
 <xref:System.Object.Finalize%2A?displayProperty=fullName>
 <xref:System.UIntPtr?displayProperty=fullName>
 [Wzorzec Dispose](http://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)



