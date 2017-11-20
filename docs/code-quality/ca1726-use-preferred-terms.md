---
title: "CA1726: Używaj preferowanych terminów | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- UsePreferredTerms
- CA1726
helpviewer_keywords: UsePreferredTerms
ms.assetid: 642b2acd-3a33-4d1f-b0a7-67073ae73be2
caps.latest.revision: "23"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 2ae02d0eb136d45bc2b8af7dde5f897765493050
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1726-use-preferred-terms"></a>CA1726: Używaj preferowanych terminów
|||  
|-|-|  
|TypeName|UsePreferredTerms|  
|CheckId|CA1726|  
|Kategoria|Microsoft.Naming|  
|Zmiana kluczowa|Dzielenie — po zestawów<br /><br /> Dzielenie non - po w parametrach typu|  
  
## <a name="cause"></a>Przyczyna  
 Nazwa widocznego na zewnątrz identyfikatora zawiera termin, dla którego istnieje alternatywny, preferowany zamiennik. Nazwa zawiera również termin flagi lub flagi.  
  
## <a name="rule-description"></a>Opis reguły  
 Ta zasada analizuje identyfikator na tokeny. Każdego pojedynczego token i ciągłe kombinacja podwójną tokenu jest porównywany terminów, które są wbudowane w regule i w sekcji uznane za przestarzałe żadnych niestandardowych słowników. W poniższej tabeli przedstawiono warunki, które są wbudowane w zasady i ich preferowanego alternatyw.  
  
|Przestarzałe termin|Preferowany termin|  
|-------------------|--------------------|  
|nie są|AreNot|  
|Anulowane|Anulowane|  
|Nie można|Nie można|  
|ComPlus|EnterpriseServices|  
|Couldnt|CouldNot|  
|Didnt|DidNot|  
|Numer nie|Nie|  
|Nie|Nie|  
|Flaga lub flagi|Nie ma żadnego warunku zastąpienia. Nie używać.|  
|nie|HadNot|  
|Nie|HasNot|  
|nie zostało to jeszcze|HaveNot|  
|Indeksy|Indeksy|  
|nie jest|IsNot|  
|Logowanie|Logowanie|  
|Wyloguj|Wyloguj|  
|Shouldnt|ShouldNot|  
|Logować|Logowanie|  
|Wyrejestrowanie|Wyloguj się|  
|Wasnt|WasNot|  
|nie zostały|WereNot|  
|Nie można|Iść|  
|Wouldnt|WouldNot|  
|Zapisywalne|Zapisywalny|  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, Zamień termin na preferowany termin alternatywny.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Pomiń ostrzeżenie od tej zasady tylko wtedy, gdy nazwa identyfikatora jest zamierzone i dotyczy w szczególności pierwotny termin zamiast preferowanych terminów.  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [Ostrzeżenia nazewnictwa](../code-quality/naming-warnings.md)