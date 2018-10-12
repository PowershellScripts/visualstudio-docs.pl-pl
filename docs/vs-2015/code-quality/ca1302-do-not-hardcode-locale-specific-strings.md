---
title: 'CA1302: Nie umieszczaj w kodzie ciągów specyficznych dla ustawień regionalnych | Dokumentacja firmy Microsoft'
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
- DoNotHardcodeLocaleSpecificStrings
- CA1302
helpviewer_keywords:
- DoNotHardcodeLocaleSpecificStrings
- CA1302
ms.assetid: 05ed134a-837d-43d7-bf97-906edeac44ce
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 9ec69304b945fb716b3921433b0755088744624d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49189751"
---
# <a name="ca1302-do-not-hardcode-locale-specific-strings"></a>CA1302: Nie należy kodować ciągów określonych dla ustawień regionalnych
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|DoNotHardcodeLocaleSpecificStrings|
|CheckId|CA1302|
|Kategoria|Microsoft.Globalization|
|Zmiana kluczowa|Bez podziału|

## <a name="cause"></a>Przyczyna
 Metoda używa literał ciągu reprezentujący części ścieżki niektórych folderów systemowych.

## <a name="rule-description"></a>Opis reguły
 <xref:System.Environment.SpecialFolder?displayProperty=fullName> Wyliczenia zawiera elementy członkowskie, które odwołują się do folderów specjalnych systemu. Lokalizacje tych folderów mogą mieć różne wartości w różnych systemach operacyjnych, użytkownik może zmienić niektóre z tych lokalizacji i lokalizacje są zlokalizowane. Przykładem specjalny folder jest folder systemowy, który jest "C:\WINDOWS\system32" na [!INCLUDE[winxp](../includes/winxp-md.md)] , ale "C:\WINNT\system32" na [!INCLUDE[win2kfamily](../includes/win2kfamily-md.md)]. <xref:System.Environment.GetFolderPath%2A?displayProperty=fullName> Metoda zwraca lokalizacje, które są skojarzone z <xref:System.Environment.SpecialFolder> wyliczenia. Lokalizacje, które są zwracane przez <xref:System.Environment.GetFolderPath%2A> są zlokalizowane i odpowiednie dla danego komputera.

 Ta zasada tokenizes ścieżek folderów, które są pobierane za pomocą <xref:System.Environment.GetFolderPath%2A> metody na poziomy oddzielny katalog. Literał ciągu jest porównywany z tokenów. Jeśli zostanie znalezione dopasowanie, zakłada się, że metoda tworzy ciąg, który odwołuje się do lokalizacji w systemie, który jest skojarzony z tokenem. W przypadku przenoszenia i przeglądu możliwości lokalizacji używać <xref:System.Environment.GetFolderPath%2A> metodę, która pobierze lokalizacje folderów specjalnych systemu, zamiast literałów ciągów.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, należy pobrać lokalizacji przy użyciu <xref:System.Environment.GetFolderPath%2A> metody.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Pomijaj ostrzeżeń dla tej reguły, jeśli literał ciągu nie jest używana do odwoływania się do jednej z lokalizacji systemu, które jest skojarzone z można bezpiecznie <xref:System.Environment.SpecialFolder> wyliczenia.

## <a name="example"></a>Przykład
 Poniższy przykład tworzy ścieżkę do wspólnego folderu dane aplikacji, która powoduje wygenerowanie ostrzeżenia trzy od tej reguły. Następnie przykład pobiera ścieżki przy użyciu <xref:System.Environment.GetFolderPath%2A> metody.

 [!code-csharp[FxCop.Globalization.HardcodedLocaleStrings#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.HardcodedLocaleStrings/cs/FxCop.Globalization.HardcodedLocaleStrings.cs#1)]
 [!code-vb[FxCop.Globalization.HardcodedLocaleStrings#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Globalization.HardcodedLocaleStrings/vb/FxCop.Globalization.HardcodedLocaleStrings.vb#1)]

## <a name="related-rules"></a>Powiązane reguły
 [CA1303: Nie przekazuj literałów jako parametrów zlokalizowanych](../code-quality/ca1303-do-not-pass-literals-as-localized-parameters.md)



