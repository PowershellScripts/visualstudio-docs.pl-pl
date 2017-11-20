---
title: "Rozszerzalność usługi starszej wersji języka | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- language services
- Visual Studio, language services
ms.assetid: 2700cd4d-5f68-43fc-b62f-dc80c3f3aa85
caps.latest.revision: "42"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a5072aef90e08d645bff2a1bb6800e409e7d2104
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="legacy-language-service-extensibility"></a>Rozszerzalność usługi starszej wersji języka
Usługa języka zapewnia obsługę specyficzny dla języka edycji kodu źródłowego w środowisku IDE.  
  
 Usługi w starszej wersji języka są zaimplementowane jako część pakiet VSPackage, ale jest nowsza sposób implementowania funkcji usługi języka Aby korzystać z rozszerzeń MEF. Aby dowiedzieć się więcej o nowy sposób wdrożenia usługi języka, zobacz [edytora i rozszerzenia usługi języka](../../extensibility/editor-and-language-service-extensions.md).  
  
 W tej sekcji omówiono struktury i implementacji usługi starszej wersji języka.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Migrowanie usługi języka starsza wersja](../../extensibility/internals/migrating-a-legacy-language-service.md)  
 Opisano sposób aktualizowania usługi języka z programu Visual Studio 2008 do najnowszej wersji.  
  
 [Podstawowe informacje dotyczące języka starszej wersji usługi](../../extensibility/internals/legacy-language-service-essentials.md)  
 Zawiera ważne informacje dotyczące sposobu tworzenia usługi języka Aby zintegrować język programowania Visual Studio.  
  
 [Tworzenie usługi języka starsza wersja](../../extensibility/internals/developing-a-legacy-language-service.md)  
 Zawiera łącza do tematów, które ułatwiają tworzenie usługi języka.  
  
 [Kolorowania w starsza wersja usługi języka](../../extensibility/internals/syntax-coloring-in-a-legacy-language-service.md)  
 Zawiera informacje dotyczące obsługi wyróżniania składni za pośrednictwem usługi języka.  
  
 [Wdrażanie usługi języka starsza wersja](../../extensibility/internals/implementing-a-legacy-language-service1.md)  
 Zawiera informacje o sposobie używania framework zarządzanego pakietu (MPF) do wdrożenia usługi oferujący wszystkie funkcje języka w kodzie zarządzanym.  
  
 [Obsługa narzędzia do przeglądania Symbol](../../extensibility/internals/supporting-symbol-browsing-tools.md)  
 Opisuje, biblioteki i narzędzia umożliwiające przeglądanie widok drzewa symboli w IDE.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Edytora i rozszerzenia usługi języka](../../extensibility/editor-and-language-service-extensions.md)  
 Zawiera omówienie programu Visual Studio edytory.  
  
 [Obsługa usługi języka do debugowania](../../extensibility/internals/language-service-support-for-debugging.md)  
 Zawiera informacje i łącza do programu Visual Studio debugowanie SDK, który zawiera informacje wymagane do tworzenia i dostosowywania debugera składniki używane do debugowania programów.