---
title: "Alias — polecenie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: tools.alias
helpviewer_keywords:
- aliases, Visual Studio commands
- commands, aliases
- Tools.Alias command
- command aliases
- alias command
ms.assetid: bdf857df-b5d5-450f-8c10-a6fd4dccc130
caps.latest.revision: "12"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: cac24838cd848770c45794637620b70cea3e1bd6
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="alias-command"></a>Alias — Polecenie
Tworzy nowy alias pełne polecenie, pełny polecenia i argumentów lub inny alias.  
  
> [!TIP]
>  Wpisywanie `>alias` bez żadnych argumentów Wyświetla bieżącą listę aliasów i ich definicje.  
  
## <a name="syntax"></a>Składnia  
  
```  
Tools.Alias [/delete] [/reset] [aliasname] [aliasstring]  
```  
  
## <a name="arguments"></a>Argumenty  
 `aliasname`  
 Opcjonalny. Nazwa nowego aliasu. Jeśli żadna wartość nie jest dostarczony dla `aliasname`, zostanie wyświetlona lista aliasów bieżący oraz ich definicje.  
  
 `aliasstring`  
 Opcjonalny. Nazwa pełne polecenie lub istniejącego aliasu i wszelkie parametry, które ma zostać utworzony jako alias. Jeśli żadna wartość nie jest dostarczony dla `aliasstring`, nazwa aliasu i alias ciąg Wyświetla określony alias.  
  
## <a name="switches"></a>Przełączniki  
 / DELETE lub/DEL lub /d  
 Opcjonalny. Usuwa określony alias, usuwa ją z autocompletion.  
  
 / Reset  
 Opcjonalny. Resetuje listę wstępnie zdefiniowane aliasy pierwotne ustawienia. To, że wszystkie wstępnie zdefiniowane aliasy przywraca i usuwa wszystkie aliasy zdefiniowane przez użytkownika.  
  
## <a name="remarks"></a>Uwagi  
 Ponieważ aliasy stanowią poleceń, muszą one być znajduje się na początku wiersza polecenia.  
  
 Po wykonaniu tego polecenia, należy uwzględnić przełączników natychmiast po poleceniu, nie po aliasy, w przeciwnym razie tego samego przełącznika dołączane jako część ciąg aliasu.  
  
 `/reset` Przełącznika prosi o potwierdzenie przed aliasy zostaną przywrócone. Brak nie krótkiej formy `/reset`.  
  
## <a name="examples"></a>Przykłady  
 W tym przykładzie jest tworzony nowy alias `upper`, aby uzyskać pełną polecenia Edit.MakeUpperCase.  
  
```  
>Tools.Alias upper Edit.MakeUpperCase  
```  
  
 W tym przykładzie Usuwa alias, `upper`.  
  
```  
>Tools.alias /delete upper  
```  
  
 W tym przykładzie wyświetla listę wszystkich bieżącego aliasy i definicje.  
  
```  
>Tools.Alias  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Find/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)