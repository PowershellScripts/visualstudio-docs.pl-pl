---
title: Implementacja dostawcy portu | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], implementing port suppliers
- port suppliers, implementing
ms.assetid: 6b8579df-58df-4c7f-8112-6015993e8765
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3bc985bf9fb55b67b5a332f007abe98c6718fbf2
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="implementing-a-port-supplier"></a>Implementacja dostawcy portu
Dostawca portu udostępnia porty na żądanie do menedżera sesji debugowania (SDM). Dostawca portu musi wykonywane podczas debugowania na maszynę z systemem innym niż DCOM lub gdy nowe urządzenie musi być obsługiwany. Na przykład aby umożliwić debugowanie na telefon komórkowy, może implementować dostawcy port udostępniający nawiązać połączenia z telefonem komórkowym (być może przy użyciu IR lub połączenie komórki) i wylicza procesy i programy uruchomione na telefonie porty.  
  
 W przypadku debugowania programów na komputerach z systemem Windows (w tym zdalnego debugowania) programu Visual Studio udostępnia dostawców portu dla macierzystego i procesy środowiska uruchomieniowego języka wspólnego (CLR), nie istnieje potrzeba do implementowania dostawcy portu w takich przypadkach.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Wdrażanie i rejestrowanie dostawcy portu](../../extensibility/debugger/implementing-and-registering-a-port-supplier.md)  
 W tym artykule omówiono, jak SDM współdziała z portu dostawcy i jego portów.  
  
 [Wymagany Port dostawcy interfejsów](../../extensibility/debugger/required-port-supplier-interfaces.md)  
 Dokumenty interfejsów, które muszą zostać zaimplementowane uzyskać portu dostawcy.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Pojęcia dotyczące debugera](../../extensibility/debugger/debugger-concepts.md)  
 Zawiera opis głównych pojęć architektury debugowania.  
  
## <a name="see-also"></a>Zobacz też  
 [Rozszerzalność debugera programu Visual Studio](../../extensibility/debugger/visual-studio-debugger-extensibility.md)