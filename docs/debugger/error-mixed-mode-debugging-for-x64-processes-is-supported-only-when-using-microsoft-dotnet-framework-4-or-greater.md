---
title: "Błąd: Trybu mieszanego debugowania dla x64 procesów jest obsługiwana tylko w przypadku korzystania z programu Microsoft .NET Framework 4 lub nowszego | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.error.interop_unsupported_x64
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: e4b0216c-7006-4832-883f-08e982ba8d3f
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 80487995064f01c61e21e067e92b9fb5eb0c53f4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="error-mixed-mode-debugging-for-x64-processes-is-supported-only-when-using-microsoft-net-framework-4-or-greater"></a>Błąd: debugowanie w trybie mieszanym dla procesów x64 jest obsługiwane tylko w przypadku korzystania z programu Microsoft .NET Framework 4 lub nowszej wersji
Aby debugować kod mieszany natywnych i zarządzanych w ramach procesu 64-bitowych, należy mieć [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] w wersji 4. Debugowanie w trybie mieszanym procesów 64-bitowe o [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] w wersji wcześniejszej niż 4 nie jest obsługiwane.  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Wykonaj jedną z następujących czynności:  
  
    -   Uaktualnienie programu [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] do wersji 4.  
  
    -   Tworzenie 32-bitowej wersji do debugowania aplikacji.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie zdalne](../debugger/remote-debugging.md)