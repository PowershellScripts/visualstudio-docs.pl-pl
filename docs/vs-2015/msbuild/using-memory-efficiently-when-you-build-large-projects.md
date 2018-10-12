---
title: Efektywne używanie pamięci podczas kompilowania dużych projektów | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- memory use (MSBuild)
- msbuild, efficient memory use building large trees
- caching (MSBuild)
ms.assetid: 853a21ed-69f7-4817-af00-57f73e2c74b5
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 89c7102a789f07cc9f0434dd5bf351ea4814d073
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49218520"
---
# <a name="using-memory-efficiently-when-you-build-large-projects"></a>Efektywne używanie pamięci podczas kompilowania dużych projektów
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Duże projekty często zawierają wiele projektów podrzędnych oraz inne zależności, a te mogą wykorzystywać duże ilości pamięci systemowej w czasie kompilacji. Gdy jest zmniejszenie ilości dostępnej pamięci systemowej, wydajność systemu również można zmniejszyć. Starsze wersje [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] projektów pozostaje w pamięci lub w wersji 3.5 projekty zostały usunięte, ale zachowane wyniki kompilacji w pamięci podręcznej pobierania nowsze.  
  
 Wersja 4.0 obsługuje to zarządzanie pamięcią automatycznie, zapisywanie projektów z konieczności używania właściwości, takie jak `UnloadProjectsOnCompletion` i `UseResultsCache`.  
  
## <a name="see-also"></a>Zobacz też  
 [Równoległe tworzenie wielu projektów](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)



