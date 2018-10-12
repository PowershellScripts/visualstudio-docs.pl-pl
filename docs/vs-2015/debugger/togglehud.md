---
title: ToggleHUD | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 7261e01d-3c72-46ce-9fb3-5f33b2ddb901
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 62d202bfca33619c14d00ec99dc44857cb01bb6a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49250450"
---
# <a name="togglehud"></a>ToggleHUD
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Włącza/wyłącza diagnostyki grafiki *HUD* nakładki (wyświetlanie Head telefoniczny), lub wyłączyć.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
void ToggleHUD();  
```  
  
## <a name="remarks"></a>Uwagi  
 HUD diagnostyki grafiki jest wyświetlany w lewym górnym rogu aplikacji, która jest uruchomiona w ramach diagnostyki grafiki. Wyświetla informacje czasu wykonywania dotyczące aplikacji i przechwytywanie informacji graficznych i komunikaty, które są dodawane przez wywołanie metody [AddMessage](../debugger/addmessage.md) funkcja elementu członkowskiego.  
  
 Aby przełączyć HUD, nie trzeba być aktywnie przechwytywanie informacji graficznych — czyli może być przełączane przez wystąpienie `VsgDbg` klasy, ale [Init](../debugger/init.md) funkcji składowej nie musi być wywołana jako pierwsza.



