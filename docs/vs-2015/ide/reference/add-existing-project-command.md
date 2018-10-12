---
title: Dodaj istniejący projekt polecenie | Dokumentacja firmy Microsoft
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
- file.addexistingproject
helpviewer_keywords:
- Add Existing Project command
- File.AddExistingProject
ms.assetid: 71cf3e31-c76b-405b-ad6a-1b1bc654bd40
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: c881f32594ee6327dfba9792fa83bd2d092efcf9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49267647"
---
# <a name="add-existing-project-command"></a>Dodaj istniejący projekt — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Dodaje istniejący projekt do bieżącego rozwiązania.  
  
## <a name="syntax"></a>Składnia  
  
```  
File.AddExistingProject filename  
```  
  
## <a name="arguments"></a>Argumenty  
 `filename`  
 Opcjonalna. Pełna ścieżka i projektu nazwa, z rozszerzeniem projekt, aby dodać do rozwiązania.  
  
 Jeśli `filename` argument zawiera spacje, muszą być ujęte w znaki cudzysłowu.  
  
 Jeśli nazwa pliku nie zostanie określony, polecenie spowoduje otwarcie okna dialogowego plików, dzięki czemu użytkownik może wybrać projekt.  
  
## <a name="remarks"></a>Uwagi  
 Automatyczne uzupełnianie próbuje zlokalizować poprawną ścieżkę i nazwę pliku podczas wpisywania.  
  
## <a name="example"></a>Przykład  
 Ten przykład dodaje [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] projektu TestProject1, do bieżącego rozwiązania.  
  
```  
>File.AddExistingProject "c:\visual studio projects\TestProject1.vbproj"  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



