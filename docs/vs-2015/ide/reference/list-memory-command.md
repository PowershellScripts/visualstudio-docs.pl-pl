---
title: Lista pamięci — polecenie | Dokumentacja firmy Microsoft
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
- debug.listmemory
helpviewer_keywords:
- Debug.ListMemory command
- ListMemory command
- list memory command
ms.assetid: a84de361-a6a6-4f6d-96aa-a0d4a424371e
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 25be71041f0ab127037a25a03cff1d6ffe42ac97
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49224500"
---
# <a name="list-memory-command"></a>Lista pamięci — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Wyświetla zawartość określonego zakresu pamięci.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.ListMemory [/ANSI|Unicode] [/Count:number] [/Format:formattype]  
[/Hex|Signed|Unsigned] [expression]  
```  
  
## <a name="arguments"></a>Argumenty  
 `expression`  
 Opcjonalna. Adres pamięci, od którego należy rozpocząć wyświetlanie pamięci.  
  
## <a name="switches"></a>Przełączniki  
 / ANSI&#124;Unicode  
 Opcjonalna. Wyświetl pamięć jako znaki odpowiadający bajtów pamięci, ANSI lub Unicode.  
  
 / Liczba:`number`  
 Opcjonalna. Określa liczbę bajtów pamięci, aby wyświetlić, zaczynając od `expression`.  
  
 / Format:`formattype`  
 Opcjonalna. Formatowanie typ do wyświetlania informacji o pamięci w **pamięci** okna; może być OneByte TwoBytes, FourBytes, EightBytes, Float (32-bitowa) lub dwukrotnie (64-bitowe). Jeśli OneByte `/Unicode` jest niedostępny.  
  
 / Szesnastkowy&#124;podpisany&#124;bez znaku  
 Opcjonalna. Określa format wyświetlania liczb: jak podpisem, bez znaku lub szesnastkową.  
  
## <a name="remarks"></a>Uwagi  
 Zamiast pisania się kompletna **Debug.listmemory —** polecenia wszystkich przełączników, można wywołać polecenia przy użyciu wstępnie zdefiniowanych aliasów z przełącznikami, niektórych ustawień do określonej wartości. Na przykład zamiast wprowadzania:  
  
```  
>Debug.ListMemory /Format:float /Count:30 /Unicode  
```  
  
 można napisać:  
  
```  
>df /Count:30 /Unicode  
```  
  
 W tym miejscu znajduje się lista dostępnych aliasów dla **Debug.listmemory —** polecenia:  
  
|Alias|Polecenia i przełączniki|  
|-----------|--------------------------|  
|**d**|Debug.listmemory —|  
|**Akcelerator deweloperski w wersji**|Debug.listmemory — /Ansi|  
|**bazy danych**|Debug.listmemory — /Format:OneByte|  
|**Kontroler domeny**|Debug.listmemory — /Format:FourBytes /Ansi|  
|**dd**|Debug.listmemory — /Format:FourBytes|  
|**DF**|Debug.listmemory — /Format:Float|  
|**dq**|Debug.listmemory — /Format:EightBytes|  
|**jednostka bazy danych**|Debug.listmemory — /Unicode|  
  
## <a name="example"></a>Przykład  
  
```  
>Debug.ListMemory /Format:float /Count:30 /Unicode  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Lista stosu wywołań — polecenie](../../ide/reference/list-call-stack-command.md)   
 [Lista wątków — polecenie](../../ide/reference/list-threads-command.md)   
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)




