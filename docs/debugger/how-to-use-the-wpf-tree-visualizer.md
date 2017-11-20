---
title: 'Porady: Korzystanie z wizualizatora drzewa WPF | Dokumentacja firmy Microsoft'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- WPF, debugging
- debugging, WPF
ms.assetid: 2a1bf1cd-90f9-4d06-9fb4-1bfc925afef3
caps.latest.revision: "18"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e30d1fbd8cd23a514d1036bc43c809626c665d73
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-use-the-wpf-tree-visualizer"></a>Porady: korzystanie z wizualizatora drzewa WPF
Można użyć z wizualizatora drzewa WPF, aby zapoznać się z drzewa wizualnego obiektu WPF i aby wyświetlić właściwości zależności WPF dla obiektów, które są zawarte w tym drzewie. Aby uzyskać więcej informacji na temat drzewa wizualnego, zobacz [drzewa WPF](/dotnet/framework/wpf/advanced/trees-in-wpf). Aby uzyskać więcej informacji na temat właściwości zależności, zobacz [Przegląd właściwości zależności](/dotnet/framework/wpf/advanced/dependency-properties-overview).  
  
 Po otwarciu wizualizatora drzewa WPF zostanie wyświetlone dwa okienka: **drzewa wizualnego** po lewej stronie i **właściwości** *nazwa***:**  *Typ* w okienku po prawej stronie. Zaznacz dowolny obiekt w **drzewa wizualnego** okienku i **właściwości** *nazwa***:***typu* okienko automatycznie aktualizowane, aby wyświetlić właściwości tego obiektu.  
  
### <a name="to-open-the-wpf-tree-visualizer"></a>Aby otworzyć z wizualizatora drzewa WPF  
  
1.  W etykietek danych **czujki** okna, **automatycznych** okna, lub **zmiennych lokalnych** okna obok nazwy obiektów WPF kliknij strzałkę obok ikonę lupy.  
  
     Zostanie wyświetlona lista wizualizatorów.  
  
2.  Kliknij przycisk **wizualizatora drzewa WPF**.  
  
### <a name="to-search-the-visual-tree"></a>Aby przeszukać drzewo wizualne  
  
-   W **drzewa wizualnego** okienku, wpisz ciąg chcesz wyszukać w **wyszukiwania** pole.  
  
     Z wizualizatora drzewa WPF natychmiast znajduje pierwszy obiekt w drzewie wizualnym pasującej do ciągu wpisany. Wpisz więcej znaków, aby znaleźć bardziej dokładne dopasowanie.  
  
    -   Aby przejść do następnego dopasowania w obrębie drzewa wizualnego, kliknij przycisk **dalej**.  
  
    -   Aby powrócić do poprzedniego dopasowania, kliknij przycisk **Prev**.  
  
    -   Aby usunąć kryteria wyszukiwania, kliknij przycisk **wyczyść**.  
  
### <a name="to-search-the-properties-list"></a>Do listy właściwości wyszukiwania  
  
-   W **właściwości** *nazwa***:***typu* okienku, wpisz ciąg chcesz wyszukać w **filtrować**pole.  
  
     Z wizualizatora drzewa WPF natychmiast wyszukuje właściwości, które zgodny z ciągiem, który został wpisany; teraz na liście zostaną wyświetlone tylko właściwości dopasowywania ciągu wpisany. Wpisz więcej znaków, aby znaleźć bardziej dokładne dopasowanie.  
  
    -   Aby usunąć kryteria wyszukiwania, kliknij przycisk **wyczyść**.  
  
### <a name="to-close-the-visualizer"></a>Aby zamknąć wizualizatora  
  
-   Kliknij przycisk **Zamknij** ikonę w prawym górnym rogu okna dialogowego.  
  
## <a name="see-also"></a>Zobacz też  
 [Utwórz niestandardowe Wizualizatory](../debugger/create-custom-visualizers-of-data.md)   
 [Drzewa na platformie WPF](/dotnet/framework/wpf/advanced/trees-in-wpf)   
 [Przegląd właściwości zależności](/dotnet/framework/wpf/advanced/dependency-properties-overview)