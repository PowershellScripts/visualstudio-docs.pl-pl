---
title: "CA1400: Powinny istnieć punkty wejścia P Invoke | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1400
- PInvokeEntryPointsShouldExist
helpviewer_keywords:
- PInvokeEntryPointsShouldExist
- CA1400
ms.assetid: 1d64e470-7b2f-4cca-8fb0-ac92829e6332
caps.latest.revision: "19"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: dd92619a652255f67c1e1558c40ea05840cd0eb5
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1400-pinvoke-entry-points-should-exist"></a>CA1400: Powinny istnieć punkty wejścia P/Invoke
|||  
|-|-|  
|TypeName|PInvokeEntryPointsShouldExist|  
|CheckId|CA1400|  
|Kategoria|Microsoft.Interoperability|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Metody publiczne lub chronione jest oznaczony atrybutem <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>. Nie można zlokalizować biblioteki niezarządzanej lub dopasować metody do funkcji w bibliotece. Jeśli reguła nie może znaleźć nazwę metody, dokładnie tak, jak określono, szuka ANSI lub wersji znaków dwubajtowych metody przez suffixing nazwę metody "" lub "W". Jeśli nie znaleziono, reguła próbuje zlokalizować funkcję przy użyciu formatu nazwy __stdcall (_MyMethod@12, gdzie 12 reprezentuje długość argumenty). Jeśli nie znaleziono nazwy metody rozpoczyna się od '#', reguły będzie przeszukiwana funkcji jako odwołanie do liczby porządkowej zamiast odwołania do nazwy.  
  
## <a name="rule-description"></a>Opis reguły  
 Bez sprawdzania kompilacji jest dostępny dla upewnij się, że metody oznaczone za pomocą <xref:System.Runtime.InteropServices.DllImportAttribute> znajdują się w bibliotece DLL niezarządzanych do którego istnieje odwołanie. Jeśli żadna funkcja, która ma określoną nazwę znajduje się w bibliotece lub argumentów dla metody są niezgodne z argumentów funkcji, środowisko uruchomieniowe języka wspólnego zgłasza wyjątek.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby rozwiązać naruszenie tej reguły, Popraw metodę, która ma <xref:System.Runtime.InteropServices.DllImportAttribute> atrybutu. Upewnij się, czy biblioteka niezarządzane istnieje i znajduje się w tym samym katalogu co zestaw, który zawiera metodę. Biblioteka jest obecny i prawidłowo przywoływany, sprawdź, że nazwa metody, zwracany typ i podpisu argumentu zgodne funkcji biblioteki.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Nie pomijaj ostrzeżenie od tej reguły, gdy biblioteka niezarządzane znajduje się w tym samym katalogu co zestaw zarządzany, która odwołuje się on. Może być bezpiecznie pominąć ostrzeżenie od tej reguły w przypadku, gdy niezarządzany biblioteki nie można zlokalizować.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład przedstawia typu, który narusza zasady. Żadnej funkcji o nazwie `DoSomethingUnmanaged` występuje w kernel32.dll.  
  
 [!code-csharp[FxCop.Interoperability.DLLExists#1](../code-quality/codesnippet/CSharp/ca1400-p-invoke-entry-points-should-exist_1.cs)]  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>