---
title: Dodawanie rozszerzeń do definicji DSL | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 07e133be-92ab-4936-a02b-45d2012bd0a6
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 9c3e74f66edc0a8b33ad1fe8205cc02cd0e80054
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49866158"
---
# <a name="adding-extensions-to-dsl-definitions"></a>Dodawanie rozszerzeń do definicji DSL
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Rozszerzenie definicji DSL umożliwia tworzenie pakietu rozszerzenia języka specyficznego dla domeny (DSL). Rozszerzenia DSL, który jest zawarty w Visual Studio Integration rozszerzenie (VSIX), można zainstalować na komputerze użytkownika w taki sam sposób jak element DSL. Dodatkowe funkcje można dynamicznie włączone i wyłączone w czasie wykonywania. Językami DSL nie muszą być jawnie zaprojektowane dla rozszerzenia, a rozszerzenia można zaprojektować później lub stron trzecich bez zmiany rozszerzonej DSL.  
  
 Dodatkowe funkcje mogą być następujące:  
  
- Właściwości elementów modelu i prezentacji  
  
- Dekoratory dla kształtów i łączników  
  
- Klasy, relacje, kształty i łączniki  
  
- Ograniczenia sprawdzania poprawności  
  
- Karty i elementów przybornika  
  
  Użytkownik rozszerzonej DSL można utworzyć i zapisać modelu, który zawiera wystąpienia dodatkowych funkcji i może zostać odczytany przez innych użytkowników, którzy mają zainstalowane odpowiednie rozszerzenie. Użytkownicy, którzy nie zainstalowano rozszerzenia nie można użyć dodatkowych funkcji, ale można zaktualizować i zapisywanie modelu bez utraty dodatkowe funkcje.  
  
  Przykładowy kod i więcej informacji na temat tej funkcji można znaleźć [Visual Studio Visualization i Modeling SDK](http://go.microsoft.com/fwlink/?LinkID=186128) witryny sieci Web.  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio Visualisation i Modeling SDK](http://go.microsoft.com/fwlink/?LinkID=186128)



