---
title: Polecenie DslTextTransform | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Domain-Specific Language, commands
ms.assetid: 7d025d0b-6543-4a49-9f6b-8b8cfcad77ee
caps.latest.revision: 32
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 1dbbf44a4adfe20f1940da32540eaad81c97251b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49269376"
---
# <a name="the-dsltexttransform-command"></a>DslTextTransform — Polecenie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

DslTextTransform.cmd to skrypt, który wywołuje TextTransform.exe i uruchamia je przy użyciu typowe opcje. DslTextTransformation.cmd można użyć do zautomatyzowania nocna kompilacja z Twojej [!INCLUDE[dsl](../includes/dsl-md.md)] projektów. Aby uzyskać więcej informacji, zobacz [Generowanie plików za pomocą narzędzia TextTransform](../modeling/generating-files-with-the-texttransform-utility.md).  
  
 DslTextTransform.cmd znajduje się w następującym katalogu:  
  
 **\<Ścieżka instalacji zestawu SDK programu Visual Studio > \VisualStudioIntegration\Tools\Bin**  
  
 Jako dane wejściowe DslTextTransform.cmd, należy określić następujące argumenty:  
  
-   Katalog wyjściowy projektu modelu domeny.  
  
-   Katalog wyjściowy projektu Projektanta definicji.  
  
-   Lokalizacja pliku szablonu tekstu.  
  
 DslTextTransform.cmd przetwarza plik szablonu określony tekst przy użyciu domyślnego procesorów dyrektyw i zestawów. Jeśli utworzono niestandardowe procesory dyrektyw, można utworzyć własny plik wsadowy, który wywołuje TextTransform.exe. W tym pliku wsadowego można określić zestawy i skojarzone niestandardowe procesory dyrektyw.



