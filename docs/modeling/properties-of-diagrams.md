---
title: "Właściwości diagramów | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.dsltools.dsldesigner.dsldiagram
helpviewer_keywords: Domain-Specific Language, diagram
ms.assetid: 00bba4b8-6aa6-4027-96cb-4f4c41a77d3c
caps.latest.revision: "25"
author: alancameronwills
ms.author: awills
manager: douge
ms.openlocfilehash: fcd30a30bdae896be5aceb9dc685a5fb762ee4af
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="properties-of-diagrams"></a>Właściwości diagramów
Można ustawić właściwości, które określają wygląd diagramy w Projektancie wygenerowany. Na przykład można określić domyślnego koloru tekstu na diagramie.  
  
 Aby uzyskać więcej informacji, zobacz [sposób definiowania języka specyficznego dla domeny](../modeling/how-to-define-a-domain-specific-language.md). Aby uzyskać więcej informacji na temat używania tych właściwości, zobacz [dostosowywanie i rozszerzanie języka specyficznego dla domeny](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
 W poniższej tabeli wymieniono właściwości diagramy.  
  
|Właściwość|Opis|Domyślny|  
|--------------|-----------------|-------------|  
|Kolor wypełnienia|Kolor wypełnienia diagramu.|biały|  
|Kolor tekstu|Kolor tekstu, który jest wyświetlany na diagramie.|czarne|  
|Modyfikator dostępu|Modyfikator dostępu klasy (wewnętrzny lub publiczny).|Public|  
|Atrybuty niestandardowe|Można dodawać atrybuty do klasy wygenerowanego kodu.|\<Brak >|  
|Generuje o podwójnej precyzji pochodnych|Jeśli `True`, zarówno klasy podstawowej i częściowej klasy (obsługuje dostosowywania przy użyciu zastąpień) zostanie wygenerowany. Aby uzyskać więcej informacji, zobacz [zastępowanie i rozszerzenie klasy generowane](../modeling/overriding-and-extending-the-generated-classes.md).|False|  
|Ma niestandardowy konstruktora|Jeśli `True`, niestandardowe konstruktora znajdzie się w kodzie źródłowym. Aby uzyskać więcej informacji, zobacz [zastępowanie i rozszerzenie klasy generowane](../modeling/overriding-and-extending-the-generated-classes.md)...|False|  
|Modyfikator dziedziczenia|Opisuje rodzaj dziedziczenia klasy kodu źródłowego, która jest generowana z diagramu (`none`, `abstract` lub `sealed`).|Brak|  
|Diagram podstawowego|Klasa podstawowa tego diagramu.|(Brak)|  
|Nazwa|Nazwa tego diagramu.|Bieżąca nazwa|  
|Przestrzeń nazw|Przestrzeń nazw, która jest połączona z tym diagramie.|Bieżącej przestrzeni nazw|  
|Reprezentowane — klasa|Klasa domeny głównego reprezentuje tego diagramu.|Bieżącej klasy głównym, jeśli to konieczne|  
|Uwagi|Nieformalne uwagi, które są skojarzone z tym elementem.|\<Brak >|  
|Kolor wypełnienia ujawnia jako właściwość|Jeśli `True`, użytkownik może ustawić kolor wypełnienia diagramu projektanta wygenerowany. Aby to ustawić, kliknij prawym przyciskiem myszy kształtu diagramu, a następnie kliknij przycisk **dodać Explosed**.|False|  
|Opisuje kolor tekstu jako właściwość|Jeśli `True`, użytkownik może ustawić kolor tekstu diagramu w Projektancie wygenerowany. Aby to ustawić, kliknij prawym przyciskiem myszy kształtu diagramu, a następnie kliknij przycisk **dodać Explosed**.|False|  
|Opis|Opis, który służy do dokumentów wygenerowanych projektanta.|\<Brak >|  
|Nazwa wyświetlana|Nazwa, która będzie wyświetlana w wygenerowanym projektanta dla tego diagramu.|\<Brak >|  
|Słowo kluczowe pomocy|Słowo kluczowe jest używana do indeksowania pomocy F1 dla tego diagramu.|\<Brak >|  
  
## <a name="see-also"></a>Zobacz też  
 [Słownik narzędzia języka specyficznego dla domeny](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)