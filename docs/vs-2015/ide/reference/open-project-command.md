---
title: Otwórz projekt — polecenie | Dokumentacja firmy Microsoft
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
- file.openproject
helpviewer_keywords:
- op command
- File.OpenProject command
- Open Project command
ms.assetid: baa85f86-041b-49f4-9ced-0c397dc180e1
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b25ee0e6ba4dfa5c29d5a009087afb55509d0c08
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49263924"
---
# <a name="open-project-command"></a>Otwórz projekt — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Otwiera istniejący projekt.  
  
## <a name="syntax"></a>Składnia  
  
```  
File.OpenProject filename  
```  
  
## <a name="arguments"></a>Argumenty  
 `filename`  
 Wymagane. Pełna ścieżka i nazwa projektu, aby otworzyć.  
  
 Składnia `filename` argument wymaga, że ścieżki zawierające spacje, użyj znaków cudzysłowu.  
  
## <a name="remarks"></a>Uwagi  
 Automatyczne uzupełnianie próbuje zlokalizować poprawną ścieżkę i nazwę pliku podczas wpisywania.  
  
 To polecenie nie jest dostępne podczas debugowania.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie otwiera [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] projektu Test1.  
  
```  
>File.OpenProject "C:\My Projects\Test1\Test1.vbproj"  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



