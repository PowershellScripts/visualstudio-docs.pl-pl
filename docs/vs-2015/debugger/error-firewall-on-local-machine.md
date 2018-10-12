---
title: 'Błąd: Zapora na zdalnym komputerze | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.firewall.localmachine
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: ab60dda9-7934-4891-aa2f-001380d2ed83
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: cbca2e944e7313e54fd469dd41774f40931ee3d2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49245352"
---
# <a name="error-firewall-on-local-machine"></a>Błąd: Zapora na zdalnym komputerze
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nie skonfigurowano Zapora połączenia internetowego na komputerze lokalnym komputerze, na którym używasz programu Visual Studio, aby zezwolić na zdalne debugowanie. Zarządzane lub natywne zdalne debugowanie przy użyciu transportu domyślnego, należy otworzyć port TCP 135 dla ruchu modelu DCOM. Udostępnianie plików i drukarek muszą być otwarte i devenv.exe, należy dodać do listy wyjątków. Otwieranie Niektóre porty protokołu IPSEC może być konieczne także.  
  
 Aby uzyskać więcej informacji, zobacz [Ustaw się narzędzi zdalnych na urządzeniu](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c).



