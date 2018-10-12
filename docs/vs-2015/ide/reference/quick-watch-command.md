---
title: Szybka czujka — polecenie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- debug.quickwatch
helpviewer_keywords:
- Quick Watch command
- Debug.Quickwatch command
ms.assetid: 9670ac3a-8f2f-4874-974d-cb87d3b0cde1
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: afe27d567601e43b10323f9dcc3417bcf15e9298
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49269415"
---
# <a name="quick-watch-command"></a>Szybka czujka — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Wyświetla zaznaczony lub określony tekst w polu wyrażenie [okno dialogowe QuickWatch](http://msdn.microsoft.com/library/ffaee1dd-e5ce-4ef2-9401-d28329398867). To okno dialogowe służy do obliczania wartości bieżącej zmiennej lub wyrażenia uznane przez debuger lub zawartości rejestru. Ponadto można zmienić wartość dowolnej zmiennej niestały lub zawartość dowolnego rejestru.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.QuickWatchq [text]  
```  
  
## <a name="arguments"></a>Argumenty  
 `text`  
 Opcjonalna. Tekst do dodania do **QuickWatch** okno dialogowe.  
  
## <a name="remarks"></a>Uwagi  
 Jeśli `text` jest pominięty, aktualnie zaznaczonego tekstu lub word przy kursorze jest dodawany do okna czujki.  
  
## <a name="example"></a>Przykład  
  
```  
>Debug.QuickWatch  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: Użyj okna dialogowego QuickWatch](http://msdn.microsoft.com/library/ffaee1dd-e5ce-4ef2-9401-d28329398867)   
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



