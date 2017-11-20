---
title: "CA2233: Operacje nie powinny powodować przepełnienia | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- OperationsShouldNotOverflow
- CA2233
helpviewer_keywords:
- OperationsShouldNotOverflow
- CA2233
ms.assetid: 3a2b06ba-6d1b-4666-9eaf-e053ef47ffaa
caps.latest.revision: "19"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: d8b602d83eee4be49f63eef0ee8d2cd3d77f5040
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2233-operations-should-not-overflow"></a>CA2233: Operacje nie powinny prowadzić do przepełnienia
|||  
|-|-|  
|TypeName|OperationsShouldNotOverflow|  
|CheckId|CA2233|  
|Kategoria|Microsoft.Usage|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Metoda wykonuje operacji arytmetycznej i nie można zweryfikować wcześniej operandów w celu uniknięcia przepełnienia.  
  
## <a name="rule-description"></a>Opis reguły  
 Operacje arytmetyczne powinien nie można wykonać bez uprzedniego sprawdzenia operandów, aby upewnić się, że wynik operacji nie jest poza zakresem możliwych wartości dla typów danych związane. W zależności od kontekstu wykonywania i typy danych przepełnienia arytmetycznego może spowodować albo <xref:System.OverflowException?displayProperty=fullName> lub odrzucone najbardziej znaczących bitów wyniku.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby rozwiązać naruszenie tej reguły, należy zweryfikować argumenty operacji przed wykonaniem operacji.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Jest bezpieczne pominąć ostrzeżenie od tej reguły, jeśli możliwe wartości operandy nigdy nie spowoduje operacji arytmetycznej przepełnienie buforu.  
  
## <a name="example-of-a-violation"></a>Przykładem naruszenia  
  
### <a name="description"></a>Opis  
 Metoda w poniższym przykładzie manipuluje liczba całkowita, która narusza tę regułę. [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]wymaga **Usuń** całkowitą przepełnienie opcję można wyłączyć dla to uruchomienie.  
  
### <a name="code"></a>Kod  
 [!code-vb[FxCop.Usage.OperationOverflow#1](../code-quality/codesnippet/VisualBasic/ca2233-operations-should-not-overflow_1.vb)]
 [!code-csharp[FxCop.Usage.OperationOverflow#1](../code-quality/codesnippet/CSharp/ca2233-operations-should-not-overflow_1.cs)]  
  
### <a name="comments"></a>Komentarze  
 Jeśli metoda w tym przykładzie zostanie przekazany <xref:System.Int32.MinValue?displayProperty=fullName>, niedopełnienie czy wykonać operację. Powoduje to najbardziej znaczącego bitu wynik, który ma zostać odrzucone. Poniższy kod przedstawia sposób występuje.  
  
 [C#]  
  
```  
public static void Main()  
{  
    int value = int.MinValue;    // int.MinValue is -2147483648   
    value = Calculator.Decrement(value);   
    Console.WriteLine(value);  
}  
```  
  
 [VB]  
  
```  
Public Shared Sub Main()       
    Dim value = Integer.MinValue    ' Integer.MinValue is -2147483648   
    value = Calculator.Decrement(value)   
    Console.WriteLine(value)   
End Sub  
```  
  
### <a name="output"></a>Dane wyjściowe  
  
```  
2147483647  
```  
  
## <a name="fix-with-input-parameter-validation"></a>Usuń ze sprawdzaniem poprawności parametru wejściowego  
  
### <a name="description"></a>Opis  
 Poniższy przykład poprawki poprzedniej naruszenie weryfikując wartość w danych wejściowych.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Usage.OperationOverflowFixed#1](../code-quality/codesnippet/CSharp/ca2233-operations-should-not-overflow_2.cs)]
 [!code-vb[FxCop.Usage.OperationOverflowFixed#1](../code-quality/codesnippet/VisualBasic/ca2233-operations-should-not-overflow_2.vb)]  
  
## <a name="fix-with-a-checked-block"></a>Usuń z sprawdzonego bloku  
  
### <a name="description"></a>Opis  
 Poniższy przykład poprawki poprzedniej naruszenie zawijania operacji w sprawdzonego bloku. Jeśli operacja powoduje przepełnienie <xref:System.OverflowException?displayProperty=fullName> zostanie wygenerowany.  
  
 Należy pamiętać, że zaznaczone bloki nie są obsługiwane w [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)].  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Usage.OperationOverflowChecked#1](../code-quality/codesnippet/CSharp/ca2233-operations-should-not-overflow_3.cs)]  
  
## <a name="turn-on-checked-arithmetic-overflowunderflow"></a>Włącz zaznaczony arytmetyczne przepełnienie/niedopełnienie  
 Jeśli włączysz zaznaczone arytmetyczne przepełnienie/niedopełnienie w języku C# jest odpowiednikiem zawijania każdej operacji całkowitą w sprawdzonego bloku.  
  
 **Aby włączyć zaznaczone arytmetyczne przepełnienie/niedopełnienie w języku C#**  
  
1.  W **Eksploratora rozwiązań**, kliknij prawym przyciskiem myszy projekt i wybierz **właściwości**.  
  
2.  Wybierz **kompilacji** i kliknij polecenie **zaawansowane**.  
  
3.  Wybierz **sprawdzaj przepełnienie/niedopełnienie arytmetyczne** i kliknij przycisk **OK**.  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.OverflowException?displayProperty=fullName>   
 [Operatory C#](/dotnet/csharp/language-reference/operators/index)   
 [Zaznaczony i niezaznaczony](/dotnet/csharp/language-reference/keywords/checked-and-unchecked)