---
title: "Evaluate statement — polecenie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: debug.evaluatestatement
helpviewer_keywords:
- Debug.EvaluateStatement command
- Evaluate Statement command
ms.assetid: 032039bc-9477-4f93-9b9d-66d4be0e90f4
caps.latest.revision: "12"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 46c80a49d0e043d7cdbffbc74698a29e10ab4795
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="evaluate-statement-command"></a>Evaluate Statement — Polecenie
Oblicza i wyświetla podanej instrukcji.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.EvaluateStatement text   
```  
  
## <a name="arguments"></a>Argumenty  
 `text`  
 Wymagany. Instrukcja do oceny.  
  
## <a name="remarks"></a>Uwagi  
 Okno służy do wprowadzania **EvaluateStatement** polecenie Określa, czy znak równości (=) jest interpretowany jako operator porównania lub operator przypisania.  
  
 W **polecenia** okna, znak równości (=) jest interpretowana jako operator porównania. Na przykład, jeśli wartości zmiennych `a` i `b` są różne, a następnie polecenie  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 Zwraca wartość `false`.  
  
 W **Immediate** okna, natomiast znak równości (=) jest interpretowana jako operatora przypisania. Tak na przykład, polecenie  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 zostanie przypisana do zmiennej `a` wartość zmiennej `b`.  
  
## <a name="example"></a>Przykład  
  
```  
>Debug.EvaluateStatement(a+b)  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Print — polecenie](../../ide/reference/print-command.md)   
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Find/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)