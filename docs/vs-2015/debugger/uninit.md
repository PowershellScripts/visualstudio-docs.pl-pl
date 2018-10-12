---
title: UnInit | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4cd4fc0b-974a-4e61-9ea8-0aaa1a0c52ea
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 485a00c5e05b04873cfdcbf10c428786408e3a72
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49298106"
---
# <a name="uninit"></a>UnInit
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kończenie znajdujących się w pliku dziennika grafiki, a następnie zamyka i zwalnia zasoby, które były używane podczas, gdy aplikacja została aktywnie rejestrowanie informacji graficznych.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
void UnInit();  
```  
  
## <a name="remarks"></a>Uwagi  
 `UnInit` jest wywoływana automatycznie, gdy wystąpienie `VsgDbg` klasa jest niszczona. Jeśli `VsgDbg` wystąpienia nie została aktywnie rejestrowanie informacji graficznych, nie ma to wpływu.  
  
 Po `UnInit` została wywołana w wystąpieniu `VsgDbg` klasy grafiki nowy plik dziennika można utworzyć przez wywołanie metody `Init` i opracowane przez wywołanie `UnInit`. To można powtarzać dowolną liczbę razy używać tego samego `VsgDbg` wystąpienia, aby utworzyć kilka niezależnych grafiki pliki dziennika.  
  
## <a name="see-also"></a>Zobacz też  
 [Init](../debugger/init.md)



