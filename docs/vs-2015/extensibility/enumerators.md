---
title: Moduły wyliczające | Dokumentacja firmy Microsoft
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
- source control plug-ins, enumerators
ms.assetid: a60030c5-e1d1-47e1-84bb-cbfe838ab479
caps.latest.revision: 20
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4dcc660ba5aacf1b8014e7c4ca15443f2fdf881b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49258508"
---
# <a name="enumerators"></a>Modułów wyliczających
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W tej sekcji przedstawiono typy danych modułu wyliczającego w interfejsie API wtyczki kontroli źródła wtyczka do kontroli źródła należy wiedzieć o.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Kod polecenia](../extensibility/command-code-enumerator.md)  
 Wylicza opcje [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md) i [SccPopulateList](../extensibility/sccpopulatelist-function.md) funkcji.  
  
 [Komunikat](../extensibility/message-enumerator.md)  
 Wylicza flagi używane do drukowania wywołanie zwrotne, [LPTEXTOUTPROC](../extensibility/lptextoutproc.md).  
  
 [Kod stanu pliku](../extensibility/file-status-code-enumerator.md)  
 Zawiera nazwanych stałych, określające stan pliku objętego kontrolą źródła.  
  
 [Kod stanu katalogu](../extensibility/directory-status-code-enumerator.md)  
 Zawiera nazwanych stałych, określające stan katalogu pod kontrolą źródła.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Tworzenie wtyczki kontroli kodu źródłowego](../extensibility/internals/creating-a-source-control-plug-in.md)  
 Definiuje zestaw SDK wtyczki kontroli źródła i opisuje dołączone zasoby.  
  
 [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)  
 Monituje użytkownika o zaawansowane opcje dla danego polecenia.  
  
 [SccPopulateList](../extensibility/sccpopulatelist-function.md)  
 Sprawdza, czy lista plików dla ich bieżący stan. Ponadto używa `pfnPopulate` funkcję, aby powiadomić obiekt wywołujący, gdy plik jest niezgodny z kryteriami, które dla `nCommand`.  
  
 [LPTEXTOUTPROC](../extensibility/lptextoutproc.md)  
 Zawiera opis funkcji wywołania zwrotnego, który jest używany przez [SccOpenProject](../extensibility/sccopenproject-function.md) umożliwiające wyświetlanie komunikatów z kontroli źródła wtyczek za pośrednictwem środowiska IDE.  
  
 [Wtyczki kontroli źródła](../extensibility/source-control-plug-ins.md)  
 Zawiera pełną listę wszystkich elementów w interfejsie API wtyczki kontroli źródła.

