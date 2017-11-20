---
title: "Obszar testu 6: Usuń | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- source control [Visual Studio SDK], deleting items
- source control plug-ins, deleting items
ms.assetid: 6f2e872c-5ba2-4303-9f50-a90cef9a6225
caps.latest.revision: "12"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2a8949135bb7354ba0279ac1b6c2f0ba99fb1b2a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="test-area-6-delete"></a>Testowanie obszaru 6: usuwanie
Ten obszar testu wtyczkę kontroli źródła obejmuje akcje usuwania.  
  
 Odpowiada usunąć akcje w kontroli źródła **Eksploratora rozwiązań**.  
  
 Poniżej znajduje się lista elementów, które mogą zostać usunięte:  
  
-   Pliki  
  
-   Foldery  
  
-   Project  
  
 W zależności od typu projektu może mieć możliwość **Usuń** projektu (pozostawia pliki na dysku) lub **usunąć** projektu (spowoduje usunięcie plików na dysku). Każda akcja usuwa projektów lub elementów z **Eksploratora rozwiązań**.  
  
## <a name="expected-behavior"></a>Oczekiwane zachowanie  
 Oczekiwane zachowanie dla przypadków testowych w obszarze testu delete jest:  
  
-   Usunięty element nie jest już widoczna w **Eksploratora rozwiązań**.  
  
-   Usunięto projektu lub elementu nadrzędnego jest wyewidencjonowany, zgodnie z potrzebami (prawdopodobnie z wierszem.)  
  
-   Po usunięciu wyewidencjonowany lub dodać elementu, nie ma w **oczekujących zaewidencjonowań** okna.  
  
-   Element nadal istnieje w magazynie kontroli źródła, nawet po usunięciu i musi ręcznie przeczyścić.  
  
|Akcja|Kroki testu|Oczekiwanych rezultatów, aby sprawdzić|  
|------------|----------------|--------------------------------|  
|Usuwanie projektu klienta|1.  Utwórz projekt klienta.<br />2.  Dodaj rozwiązanie do kontroli źródła.<br />3.  Usuń cały projekt z rozwiązania|Typowe oczekiwane zachowanie.|  
|Usuń pusty plik|1.  Utwórz projekt klienta.<br />2.  Dodaj plik zero bajtów do projektu.<br />3.  Dodaj rozwiązanie do kontroli źródła.<br />4.  Wybierz plik, usuń go.|Typowe oczekiwane zachowanie.|  
|Usuwanie folderu z plikami|1.  Tworzenie rozwiązania pojedynczego projektu.<br />2.  Dodaj folder.<br />3.  Dodaj jeden plik do folderu.<br />4.  Dodaj rozwiązanie do kontroli źródła.<br />5.  Zapoznaj się z projektu, aby uniknąć monitów.<br />6.  Usuń folder.|Typowe oczekiwane zachowanie.|  
|Usuwanie projektu sieci Web systemu plików|1.  Utwórz projekt sieci Web systemu plików (Użyj przycisk Przeglądaj, aby określić ścieżkę UNC).<br />2.  Dodaj rozwiązanie do kontroli źródła.<br />3.  Usuń cały projekt z rozwiązania.<br />4.  Powtórz kroki od 1 do 3 dla lokalnych projektu sieci Web (wykonuje różne ścieżki do kodu, ale ma tego samego interfejsu zewnętrznego i zachowanie).|Typowe oczekiwane zachowanie.|  
|Usuń plik z projektu sieci Web systemu plików|1.  Utwórz projekt sieci Web systemu plików.<br />2.  Dodaj rozwiązanie do kontroli źródła.<br />3.  Usuń plik z projektu.<br />4.  Powtórz kroki od 1 do 3 dla lokalnych projektu sieci Web (wykonuje różne ścieżki do kodu, ale ma tego samego interfejsu zewnętrznego i zachowanie).|Typowe oczekiwane zachowanie.|  
  
## <a name="see-also"></a>Zobacz też  
 [Przewodnik po testowym dla plug-in kontroli źródła](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)