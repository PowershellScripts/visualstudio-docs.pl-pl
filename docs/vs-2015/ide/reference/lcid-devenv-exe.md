---
title: — Identyfikator LCID (devenv.exe) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- language default
- locale IDs, setting for IDE
- Devenv, /LCID switch
- locale IDs
- /l Devenv switch
- LCID devenv switch
- /lcid Devenv switch
ms.assetid: 3a3f4e70-ea66-4351-9d62-acb1dec30e8e
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 242e0055e59312cba616859e08a2a61a45064e66
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49301915"
---
# <a name="lcid-devenvexe"></a>/LCID (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Ustawia domyślny język używany dla tekstu, waluty i innych wartości w ramach zintegrowanego środowiska programistycznego (IDE).  
  
## <a name="syntax"></a>Składnia  
  
```  
devenv {/LCID|/l} LocaleID  
```  
  
## <a name="arguments"></a>Argumenty  
 `LocaleID`  
 Wymagane. Identyfikator LCID (identyfikator ustawień regionalnych) języka, które określisz.  
  
## <a name="remarks"></a>Uwagi  
 Ładuje środowisko IDE i ustawia domyślny język naturalny dla środowiska. Ta zmiana jest zachowywane między sesjami i przedstawiane na **ustawienia międzynarodowe** okienku **środowiska** opcji na liście **opcje** okno dialogowe w środowisku IDE.  
  
 Jeśli określony język nie jest dostępne w systemie użytkownika, przełącznik/LCID jest ignorowany.  
  
 Poniższa tabela zawiera identyfikatory LCID języków obsługiwanych przez [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
|Język|LCID|  
|--------------|----------|  
|Chiński uproszczony|2052|  
|Chiński (tradycyjny)|1028|  
|Angielski|1033|  
|Francuski|1036|  
|niemiecki|1031|  
|Włoski|1040|  
|japoński|1041|  
|koreański|1042|  
|Hiszpański|3082|  
  
## <a name="example"></a>Przykład  
 W tym przykładzie ładuje środowisko IDE z ciągów zasobów w języku angielskim.  
  
```  
devenv /LCID 1033  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)   
 [Okno dialogowe Opcje ustawienia międzynarodowe, środowisko,](../../ide/reference/international-settings-environment-options-dialog-box.md)   
 [Dostosowywanie układów okien](../../ide/customizing-window-layouts-in-visual-studio.md)



