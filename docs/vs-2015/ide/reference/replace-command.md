---
title: Zastąp — polecenie | Dokumentacja firmy Microsoft
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
- edit.replace
helpviewer_keywords:
- Edit.Replace command
- Replace command
ms.assetid: a15767f1-5a3d-44f5-8c77-7b0f1157f340
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 83281a656d553dfa677d7ae25bf043fc0b588978
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49283208"
---
# <a name="replace-command"></a>Zastąp — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Zastępuje tekst w plikach za pomocą podzestawu opcji dostępnych w **Zamień w plikach** karcie **Znajdź i Zamień** okna.  
  
## <a name="syntax"></a>Składnia  
  
```  
Edit.Replace findwhat replacewith [/all] [/case]  
[/doc|/proc|/open|/sel] [/hidden] [/options] [/reset] [/up]  
[/wild|/regex] [/word]  
```  
  
## <a name="arguments"></a>Argumenty  
 `findwhat`  
 Wymagane. Tekst do dopasowania.  
  
 `replacewith`  
 Wymagane. Tekst do podstawienia w dopasowany tekst.  
  
## <a name="switches"></a>Przełączniki  
 / all lub /a  
 Opcjonalna. Zamienia wszystkie wystąpienia tekstu wyszukiwania tekst zastępczy.  
  
 /Case lub /c  
 Opcjonalna. Dopasowuje występują tylko wtedy, gdy po wielkich i małych liter dokładnie odpowiadać określone w `findwhat` argumentu.  
  
 / doc lub /d  
 Opcjonalna. Wyszukuje w bieżącym dokumencie. Określ tylko jeden zakres wyszukiwania dostępnych `/doc`, `/proc`, `/open`, lub `/sel`.  
  
 / ukryte lub/h  
 Opcjonalna. Wyszukiwanie ukryte i zwiniętego tekstu, takich jak metadane kontroli czasu projektowania, ukryty region konspektu dokumentu lub zwinięty klasy lub metody.  
  
 / Open lub /o  
 Opcjonalna. Przeszukuje wszystkie otwarte dokumenty, jakby pochodziły z jednego dokumentu. Określ tylko jeden zakres wyszukiwania dostępnych `/doc`, `/proc`, `/open`, lub `/sel`.  
  
 / Options lub/t  
 Opcjonalna. Wyświetla listę bieżących ustawień opcji wyszukiwania, a nie wyszukiwania.  
  
 /proc lub /p  
 Opcjonalna. Wyszukuje bieżącą procedurę. Określ tylko jeden zakres wyszukiwania dostępnych `/doc`, `/proc`, `/open`, lub `/sel`.  
  
 /regex lub/r  
 Opcjonalna. Używa wstępnie zdefiniowanych znaków specjalnych w `findwhat` argument jako notacji, które reprezentują wzorców tekstu, a nie jako znaki literału. Aby uzyskać pełną listę znaki wyrażenia regularnego, zobacz [wyrażeń regularnych](../../ide/using-regular-expressions-in-visual-studio.md).  
  
 / Reset i/e  
 Opcjonalna. Zwraca opcje wyszukiwania do ustawień domyślnych, a nie wyszukiwania.  
  
 /SEL lub /s  
 Opcjonalna. Wyszukuje w bieżącym zaznaczeniu. Określ tylko jeden zakres wyszukiwania dostępnych `/doc`, `/proc`, `/open`, lub `/sel`.  
  
 /Up lub /u  
 Opcjonalna. Wyszukiwanie w bieżącej lokalizacji w pliku w górnej części pliku. Domyślnie wyszukiwanie rozpoczyna się w bieżącej lokalizacji w pliku i Zaawansowane w kierunku końca pliku.  
  
 /Wild lub/l  
 Opcjonalna. Używa wstępnie zdefiniowanych znaków specjalnych w `findwhat` argument jako notacji do reprezentowania znaku lub sekwencji znaków.  
  
 opcji lub Wn  
 Opcjonalna. Wyszukiwanie tylko całe wyrazy.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie zastępuje `btnSend` z `btnSubmit` we wszystkich otwartych dokumentach.  
  
```  
>Edit.Replace btnSend btnSubmit /open  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Znajdowanie i zastępowanie tekstu](../../ide/finding-and-replacing-text.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



