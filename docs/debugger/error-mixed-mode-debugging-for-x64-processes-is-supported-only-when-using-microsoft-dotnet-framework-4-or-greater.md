---
title: 'Błąd: Trybu mieszanego debugowania x64 procesów jest obsługiwana tylko w przypadku korzystania z programu Microsoft .NET Framework 4 lub nowszego | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.interop_unsupported_x64
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: b1e7159c67ab104156f2dccd6d89413594ded33c
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49874413"
---
# <a name="error-mixed-mode-debugging-for-x64-processes-is-supported-only-when-using-microsoft-net-framework-4-or-greater"></a>Błąd: debugowanie w trybie mieszanym dla procesów x64 jest obsługiwane tylko w przypadku korzystania z programu Microsoft .NET Framework 4 lub nowszej wersji
Aby debugować kod mieszany natywnych i zarządzanych w procesie 64-bitowym, konieczne jest posiadanie [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] w wersji 4. Debugowanie trybu mieszanego procesów 64-bitowe o [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] w wersji wcześniejszej niż 4 nie jest obsługiwane.  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
- Wykonaj jedną z następujących czynności:  
  
  - Uaktualnij swoje [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] do wersji 4.  
  
  - Twórz 32-bitowej wersji aplikacji do debugowania.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie zdalne](../debugger/remote-debugging.md)