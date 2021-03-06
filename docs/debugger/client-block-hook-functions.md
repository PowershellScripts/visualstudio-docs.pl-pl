---
title: Funkcje punktu zaczepienia bloku klienta | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.hooks
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
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e9de7c0533d3ea55e7b78ca645735a60f84e66df
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49938022"
---
# <a name="client-block-hook-functions"></a>Funkcje punktu zaczepienia bloku klienta
Jeśli chcesz sprawdzić lub zgłosić zawartość danych przechowywanych w `_CLIENT_BLOCK` blokuje, można napisać funkcję specjalnie do tego celu. Napisana funkcja musi mieć podobny do poniższego, prototyp, zgodnie z definicją w CRTDBG. GODZ.:  

```cpp
void YourClientDump(void *, size_t)  
```  

 Innymi słowy, funkcja podłączania powinna obsługiwać **void** wskaźnika na początku bloku alokacji, wraz z **size_t** wpisz wartość wskazującą, rozmiar alokacji i zwracać `void`. Innych niż jego zawartość, zależą od Ciebie.  

 Po zainstalowaniu, używając funkcji punktów zaczepienia [_CrtSetDumpClient](/cpp/c-runtime-library/reference/crtsetdumpclient), będzie ona wywoływana zawsze `_CLIENT_BLOCK` jest zrzucany bloku. Następnie można użyć [_CrtReportBlockType](/cpp/c-runtime-library/reference/crtreportblocktype) można pobrać informacji na temat typu lub podtypu zrzut bloków.  

 Wskaźnik do funkcji, możesz przekazać do `_CrtSetDumpClient` typu **_crt_dump_client —**, zgodnie z definicją w CRTDBG. GODZ.:  

```cpp
typedef void (__cdecl *_CRT_DUMP_CLIENT)  
   (void *, size_t);  
```  

## <a name="see-also"></a>Zobacz też  
 [Debugowanie pisanie funkcji punktów zaczepienia](../debugger/debug-hook-function-writing.md)   
 [Przykładowe crt_dbg2](https://msdn.microsoft.com/library/21e1346a-6a17-4f57-b275-c76813089167)   
 [_CrtReportBlockType](/cpp/c-runtime-library/reference/crtreportblocktype)
