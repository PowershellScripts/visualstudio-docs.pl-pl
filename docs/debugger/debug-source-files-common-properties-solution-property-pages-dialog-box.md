---
title: "Debugowanie źródła plików, typowe właściwości rozwiązania właściwości strony — okno dialogowe | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.options.FindSource
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
- SQL
helpviewer_keywords:
- Debug Source Files property page
- debugging [Visual Studio], specifying source and symbol files
- source files, specifying in debugger
- debugger, source files
ms.assetid: 0af11464-eeb1-4d0b-87a6-0cc96779afb1
caps.latest.revision: "10"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 96ca9ef63a3823b942a6d7a160c31473f5db8962
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="debug-source-files-common-properties-solution-property-pages-dialog-box"></a>Debugowanie plików źródłowych, typowe właściwości, strony właściwości rozwiązania — Okno dialogowe
Ta strona właściwości określa, gdzie debuger będzie szukać plików źródłowych, podczas debugowania rozwiązania.  
  
 Aby uzyskać dostęp do **debugowania plików źródłowych** strony właściwości, kliknij prawym przyciskiem myszy na rozwiązania w **Eksploratora rozwiązań** i wybierz **właściwości** z menu skrótów. Rozwiń węzeł **wspólne właściwości** folder, a następnie kliknij przycisk **debugowania plików źródłowych** strony.  
  
 **Katalogi zawierające kod źródłowy**  
 Zawiera listę katalogów, w których debuger wyszukuje pliki źródłowe podczas debugowania rozwiązania. Podkatalogi określonych katalogach również będą wyszukiwane.  
  
 **Wyszukuje pliki źródłowe**  
 Wprowadź nazwy plików, które nie mają debugera do odczytu. Jeśli debuger znajdzie jednego z tych plików w jednym z katalogów podanych powyżej, zignoruje go. Jeśli **Znajdź źródło** okno dialogowe pojawia się podczas debugowania, a następnie kliknij **anulować**, plik zostanie pobiera dodane do tej listy, aby debuger nie będzie kontynuowana wyszukiwania dla tego pliku.  
  
## <a name="see-also"></a>Zobacz też  
 [Zabezpieczenia debugera](../debugger/debugger-security.md)   
 [Ustawienia debugowania i przygotowanie](../debugger/debugger-settings-and-preparation.md)