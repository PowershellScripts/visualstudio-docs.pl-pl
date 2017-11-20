---
title: Funkcje punktu zaczepienia bloku klienta | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.hooks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- client blocks, validating and reporting data
- debugging [C++], hook functions
- _CrtSetDumpClient function
- client blocks, hook functions
- hooks, client block
ms.assetid: f21c197e-565d-4e3f-9b27-4c018c9b87fc
caps.latest.revision: "15"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7761690ee905ffd65ded9498de7422857b31f455
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="client-block-hook-functions"></a>Funkcje punktu zaczepienia bloku klienta
Jeśli chcesz zweryfikować lub zgłosić zawartości danych przechowywanych w `_CLIENT_BLOCK` blokuje, można napisać funkcję specjalnie do tego celu. Funkcja, który można zapisać musi mieć prototyp podobny do następującego, zgodnie z definicją w CRTDBG. H:  
  
```  
void YourClientDump(void *, size_t)  
  
```  
  
 Innymi słowy, należy zaakceptować funkcji punktów zaczepienia **void** wskaźnika na początku bloku alokacji, wraz z **size_t** wpisz wartość wskazującą, rozmiar alokacji i zwracać `void`. Inną niż jego zawartość jest od użytkownika.  
  
 Po zainstalowaniu, używając funkcji punktów zaczepienia [_crtsetdumpclient —](/cpp/c-runtime-library/reference/crtsetdumpclient), będzie ona wywoływana zawsze `_CLIENT_BLOCK` bloku jest utworzyć zrzutu. Następnie można użyć [_crtreportblocktype —](/cpp/c-runtime-library/reference/crtreportblocktype) Aby uzyskać informacje na temat typu lub podtypu zrzut bloków.  
  
 Wskaźnik do funkcji, które są przekazywane do `_CrtSetDumpClient` jest typu **_crt_dump_client —**, zgodnie z definicją w CRTDBG. H:  
  
```  
typedef void (__cdecl *_CRT_DUMP_CLIENT)  
   (void *, size_t);  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie pisanie funkcji punktów zaczepienia](../debugger/debug-hook-function-writing.md)   
 [Przykładowe crt_dbg2](http://msdn.microsoft.com/en-us/21e1346a-6a17-4f57-b275-c76813089167)   
 [_Crtreportblocktype —](/cpp/c-runtime-library/reference/crtreportblocktype)