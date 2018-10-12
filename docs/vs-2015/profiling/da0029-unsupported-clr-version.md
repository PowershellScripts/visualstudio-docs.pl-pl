---
title: 'DA0029: Nieobsługiwana wersja środowiska CLR | Dokumentacja firmy Microsoft'
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
- vs.performance.29
- vs.performance.rules.DA0029
helpviewer_keywords:
- vs.performance.29
- vs.performance.DA0029
- vs.performance.rules.DA0029
ms.assetid: 76247259-c6f3-44c4-b3f9-d8dac16b5e0d
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6334fc69607f6d39e75d20c3b3ca228507db169d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49265146"
---
# <a name="da0029-unsupported-clr-version"></a>DA0029: Nieobsługiwana wersja CLR
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Identyfikator reguły | DA0029 |  
| Kategoria | Profilowanie użycia narzędzia |  
| Metoda profilowania | Profilowanie z wiersza polecenia |  
| Komunikat | Podczas zbierania Wykryto nieobsługiwaną wersję środowiska CLR. Symbole zarządzane mogą nie być rozpoznawane poprawnie. |  
| Typ reguły | Informacje o. |  
  
## <a name="cause"></a>Przyczyna  
 Chcesz profilować aplikację, która używa [!INCLUDE[net_v11_long](../includes/net-v11-long-md.md)] nie jest obsługiwana przez narzędzia profilowania.  
  
## <a name="rule-description"></a>Opis reguły  
 To ostrzeżenie występuje, ponieważ narzędzia profilowania nie będzie można rozwiązać symbole dla kodu zarządzanego w aplikacji. Narzędzia profilowania nie można rozpoznać symbole kodu zarządzanego dla aplikacji, które są uruchomione [!INCLUDE[net_v11_long](../includes/net-v11-long-md.md)].  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Brak.



