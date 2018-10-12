---
title: Właściwości elementów Decorator | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Domain-Specific Language, decorators
ms.assetid: f6322fe5-dc08-4d32-a6b3-0bd18879136d
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 2d7d6aec514cab53777840730dee6bafac51512e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49276890"
---
# <a name="properties-of-decorators"></a>Właściwości elementów Decorator
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dekoratory są ikony, tekst lub cudzysłów ostrokątny rozwijania/zwijania, które mogą być wyświetlane na kształtów i łączników na diagramie. W poniższej tabeli przedstawiono właściwości dla trzy rodzaje dekoratora. Niektóre właściwości są wyświetlane tylko dekoratory kształtu lub tylko dekoratory łącznika.  
  
 Aby uzyskać więcej informacji, zobacz [sposób definiowania języka specyficznego dla domeny](../modeling/how-to-define-a-domain-specific-language.md). Aby uzyskać więcej informacji o tym, jak korzystać z tych właściwości, zobacz [dostosowywanie i rozszerzanie języka specyficznego dla domeny](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
## <a name="expandcollapse-decorator"></a>Rozwiń/Zwiń Dekoratora  
  
|Właściwość|Opis|Domyślny|  
|--------------|-----------------|-------------|  
|Nazwa wyświetlana|Nazwa dekoratora, która będzie wyświetlana w wygenerowanym projektancie.|Rozwiń Zwiń Dekoratora|  
|Nazwa|Nazwa dekoratora.|ExpandCollapseDecorator|  
|Uwagi|Uwagi informacyjne, które są skojarzone z tego dekoratora.|\<Brak >|  
|HorizontalOffset|Przesunięcie w poziomie, względem domyślnej pozycji dekoratora, w calach. (Na tylko kształty.)|0|  
|Verticaloffset w razie|Przesunięcie w pionie, względem domyślnej pozycji dekoratora, w calach. (Na tylko kształty.)|0|  
|OffsetFromLine|Przesunięcie dekoratora od linii, względem jego bieżącej pozycji (w calach). (W łącznikach jedynie.)|0|  
|OffsetFromShape|Przesunięcie dekoratora od kształtu względem jego bieżącej pozycji (w calach). (W łącznikach jedynie.)|0|  
|Pozycja|Domyślnej pozycji dekoratora.|SourceTop|  
  
## <a name="icon-decorator"></a>Ikona Dekoratora  
  
|Właściwość|Opis|Domyślny|  
|--------------|-----------------|-------------|  
|DefaultIcon|Ścieżka pliku ikony lub obrazu do wyświetlenia.|\<Brak >|  
|Nazwa wyświetlana|Nazwa dekoratora, który ma być wyświetlana w wygenerowanym projektancie.|Ikona Dekoratora|  
|Nazwa|Nazwa dekoratora.|Elementu IconDecorator|  
|Uwagi|Uwagi informacyjne, które są skojarzone z dekoratora.|\<Brak >|  
|HorizontalOffset|Przesunięcie w poziomie, względem domyślnej pozycji dekoratora, w calach. (Na tylko kształty.)|0|  
|Verticaloffset w razie|Przesunięcie w pionie, względem domyślnej pozycji dekoratora, w calach. (Na tylko kształty.)|0|  
|OffsetFromLine|Przesunięcie dekoratora od linii, względem jego bieżącej pozycji (w calach). (W łącznikach jedynie.)|0|  
|OffsetFromShape|Przesunięcie dekoratora od kształtu względem jego bieżącej pozycji (w calach). (W łącznikach jedynie.)|0|  
|Pozycja|Domyślnej pozycji dekoratora.|SourceTop|  
  
## <a name="textdecorator"></a>Elementu TextDecorator  
  
|Właściwość|Opis|Domyślny|  
|--------------|-----------------|-------------|  
|DefaultText|Domyślny tekst, który ma być wyświetlany.|Etykieta|  
|Nazwa wyświetlana|Nazwa dekoratora, który ma być wyświetlana w wygenerowanym projektancie.|Etykieta|  
|FontSize|Rozmiar czcionki dla tekstu wyświetlanego w dekoratorze.|8|  
|fontStyle|Styl czcionki dla tekstu wyświetlanego w dekoratorze.|Regularne|  
|Nazwa|Nazwa dekoratora.|Etykieta|  
|Uwagi|Uwagi informacyjne, które są skojarzone z dekoratora.|\<Brak >|  
|HorizontalOffset|Przesunięcie w poziomie, względem domyślnej pozycji dekoratora, w calach. (Na tylko kształty.)|0|  
|Verticaloffset w razie|Przesunięcie w pionie, względem domyślnej pozycji dekoratora, w calach. (Na tylko kształty.)|0|  
|OffsetFromLine|Przesunięcie dekoratora od linii, względem jego bieżącej pozycji (w calach). (W łącznikach jedynie.)|0|  
|OffsetFromShape|Przesunięcie dekoratora od kształtu względem jego bieżącej pozycji (w calach). (W łącznikach jedynie.)|0|  
|Pozycja|Domyślnej pozycji dekoratora.|TargetBottom|  
  
## <a name="see-also"></a>Zobacz też  
 [Słownik narzędzi języka specyficznego dla domeny](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)



