---
title: Evaluate statement — polecenie | Dokumentacja firmy Microsoft
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
- debug.evaluatestatement
helpviewer_keywords:
- Debug.EvaluateStatement command
- Evaluate Statement command
ms.assetid: 032039bc-9477-4f93-9b9d-66d4be0e90f4
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: d3e50b519b162201d741f2460a8e9dbbe675c16e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49230324"
---
# <a name="evaluate-statement-command"></a>Evaluate Statement — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Oblicza i wyświetla daną instrukcję.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.EvaluateStatement text   
```  
  
## <a name="arguments"></a>Argumenty  
 `text`  
 Wymagane. Instrukcja do oceny.  
  
## <a name="remarks"></a>Uwagi  
 Okno służące do wprowadzania **EvaluateStatement** polecenie Określa, czy znak równości (=) jest interpretowany jako operator porównania lub operator przypisania.  
  
 W **polecenia** okna, znak równości (=) jest interpretowany jako operator porównania. Na przykład, jeśli wartości zmiennych `a` i `b` są różne, a następnie polecenie  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 Zwraca wartość `false`.  
  
 W **bezpośrednie** okna, z drugiej strony, znak równości (=) jest interpretowany jako operator przypisania. Tak na przykład polecenie  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 przypiszą do zmiennej `a` wartość zmiennej `b`.  
  
## <a name="example"></a>Przykład  
  
```  
>Debug.EvaluateStatement(a+b)  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Print — polecenie](../../ide/reference/print-command.md)   
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



