---
title: "MSBuild najlepszych rozwiązań | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- best practices, MSBuild
- MSBuild, best practices
ms.assetid: 90ef8693-e921-410a-a377-fe4d13f58c48
caps.latest.revision: "5"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 881075ee32ccac155237035dbe1a2f6d17a82893
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="msbuild-best-practices"></a>Najlepsze praktyki w programie MSBuild
Zaleca się następujące najlepsze rozwiązania dotyczące pisania skryptów programu MSBuild:  
  
-   Domyślne wartości właściwości najlepiej są obsługiwane przy użyciu `Condition` atrybutu, a nie przez deklarowanie właściwości, której domyślna wartość może zostać zastąpiona w wierszu polecenia. Na przykład użyć  
  
     `<MyProperty Condition="'$(MyProperty)' == ''">`  
  
     `MyDefaultValue`  
  
     `</MyProperty>`  
  
-   Po wybraniu elementów, należy unikać symboli wieloznacznych. Zamiast tego należy jawnie określić pliki. Ułatwia to śledzenie błędów, które mogą wystąpić podczas dodawania i usuwania plików.  
  
## <a name="see-also"></a>Zobacz też  
 [Pojęcia zaawansowane](../msbuild/msbuild-advanced-concepts.md)