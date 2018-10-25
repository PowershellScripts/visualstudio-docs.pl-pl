---
title: DslTextTransform — Polecenie
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, commands
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: 8c1be8b041fcf5f4eb70b37a53b7c32705f6cfcf
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49876623"
---
# <a name="the-dsltexttransform-command"></a>DslTextTransform — Polecenie
DslTextTransform.cmd to skrypt, który wywołuje TextTransform.exe i uruchamia je przy użyciu typowe opcje. DslTextTransformation.cmd można użyć do zautomatyzowania nocna kompilacja z Twojej [!INCLUDE[dsl](../modeling/includes/dsl_md.md)] projektów. Aby uzyskać więcej informacji, zobacz [Generowanie plików za pomocą narzędzia TextTransform](../modeling/generating-files-with-the-texttransform-utility.md).

 DslTextTransform.cmd znajduje się w następującym katalogu:

 **\<Ścieżka instalacji zestawu SDK programu Visual Studio > \VisualStudioIntegration\Tools\Bin**

 Jako dane wejściowe DslTextTransform.cmd, należy określić następujące argumenty:

- Katalog wyjściowy projektu modelu domeny.

- Katalog wyjściowy projektu Projektanta definicji.

- Lokalizacja pliku szablonu tekstu.

  DslTextTransform.cmd przetwarza plik szablonu określony tekst przy użyciu domyślnego procesorów dyrektyw i zestawów. Jeśli utworzono niestandardowe procesory dyrektyw, można utworzyć własny plik wsadowy, który wywołuje TextTransform.exe. W tym pliku wsadowego można określić zestawy i skojarzone niestandardowe procesory dyrektyw.