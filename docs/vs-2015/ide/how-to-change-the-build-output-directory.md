---
title: 'Porady: zmiana katalogu wyjściowego kompilacji | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- output directory, changing
ms.assetid: a8333c89-afb2-4b1d-b2e2-9146da852402
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: cc0f6b30abd8c737db018bbc2bb761afc996d6c6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49263565"
---
# <a name="how-to-change-the-build-output-directory"></a>Porady: zmiana budowy katalogu wyjściowego
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Należy określić lokalizację danych wyjściowych, na podstawie — konfiguracja (w przypadku debugowania, wersji lub obie) wygenerowany przez projekt.  
  
> [!NOTE]
>  Jeśli masz **Instalatora** projektu patrz Uwaga na końcu tego artykułu.  
  
## <a name="changing-the-build-output-directory"></a>Zmiana katalogu wyjściowego kompilacji  
  
#### <a name="to-change-the-build-output-directory"></a>Aby zmienić katalog wyjściowy kompilacji  
  
1.  Na pasku menu wybierz **projektu**, *Appname* **właściwości**. Również kliknięciu prawym przyciskiem myszy węzeł projektu w **Eksploratora rozwiązań** i wybierz **właściwości**.  
  
2.  Jeśli masz projekt języka Visual Basic, wybierz **skompilować** kartę. Jeśli masz projekt Visual C#, wybierz **kompilacji** kartę. Jeśli masz projekt języka C++ lub projektu w języku JavaScript, wybierz opcję **ogólne** kartę.  
  
3.  W konfiguracji listy rozwijanej u góry wybierz konfigurację, której dane wyjściowe pliku lokalizacji, aby zmienić (debugowanie, wydanie lub wszystkie).  
  
     Znajdź pozycję Ścieżka danych wyjściowych (**ścieżkę wyjściową kompilacji** w języku Visual Basic **katalog wyjściowy** w programie Visual C++ **ścieżkę wyjściową** w języku JavaScript i C#). Określ nowy katalog danych wyjściowych kompilacji względem katalogu projektu.  
  
> [!NOTE]
>  W projekcie programu Instalatora **nazwę pliku wyjściowego** okno zmienia lokalizację pliku Setup.exe, a nie lokalizacja plików projektów. Aby uzyskać więcej informacji, zobacz **kompilacji, właściwości konfiguracji, okno dialogowe właściwości projektu wdrożenia**.  
  
## <a name="see-also"></a>Zobacz też  
 [Strona kompilacji, Projektant projektu (C#)](../ide/reference/build-page-project-designer-csharp.md)   
 [Strona właściwości ogólnych (projekt)](http://msdn.microsoft.com/library/593b383c-cd0f-4dcd-ad65-9ec9b4b19c45)   
 [Kompilowanie i tworzenie](../ide/compiling-and-building-in-visual-studio.md)



