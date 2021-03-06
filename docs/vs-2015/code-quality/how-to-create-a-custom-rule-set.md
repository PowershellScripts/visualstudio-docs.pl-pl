---
title: 'Porady: Tworzenie niestandardowego zestawu reguł | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.codeanalysis.addremoverulesets
helpviewer_keywords:
- Development Edition, rule sets
ms.assetid: bcc42508-9592-4802-9f66-a50111641d73
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a5d8a5cb7e29cfd900ce81fa5f4b6253f0c49014
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49812468"
---
# <a name="how-to-create-a-custom-rule-set"></a>Porady: tworzenie niestandardowego zestawu reguł
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W [!INCLUDE[vsUltShort](../includes/vsultshort-md.md)], [!INCLUDE[vsPreShort](../includes/vspreshort-md.md)], i [!INCLUDE[vsPro](../includes/vspro-md.md)], można tworzyć i modyfikować niestandardowego *zestaw reguł* do potrzeb określonego projektu skojarzony z analizy kodu. Aby utworzyć niestandardową regułę zestaw, otwórz jedną lub więcej standardowe reguły ustawia z edytora zestawu reguł. Można następnie dodać lub usunąć określone zasady i możesz zmienić akcję wykonywaną podczas analizy kodu Określa, że reguły zostały naruszone.  
  
 Aby utworzyć nową regułę niestandardową zestawu, zapisz go przy użyciu nowej nazwy pliku. Niestandardowego zestawu reguł jest przypisywany do projektu.  
  
## <a name="opening-the-rule-set-editor"></a>Otwarcie reguły edytorze zestawu  
  
#### <a name="to-open-an-empty-rule-set-file-in-the-rule-set-editor"></a>Aby otworzyć pusty zestaw reguł plik w edytorze zestawu reguł  
  
1.  Na **pliku** menu [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)], wskaż polecenie **New** a następnie kliknij przycisk **pliku**.  
  
2.  W **nowy plik** okno dialogowe, kliknij przycisk **ogólne** w **zainstalowane szablony** listy, a następnie wybierz **zestawu reguł analizy kodu**.  
  
3.  Pojawia się z edytora zestawu reguł. Na liście edytora nie zaznaczono żadnych reguł.  
  
#### <a name="to-create-a-custom-rule-from-a-single-existing-rule-set"></a>Aby utworzyć niestandardową regułę z jednego istniejącego zestawu reguł  
  
1. W Eksploratorze rozwiązań kliknij prawym przyciskiem myszy projekt, a następnie wybierz **właściwości**.  
  
2. Na **właściwości** kliknij pozycję **analizy kodu**.  
  
3. W **zestaw reguł** listy rozwijanej, wykonaj jedną z następujących czynności:  
  
   - Wybierz zestaw reguł, który chcesz dostosować.  
  
     \- lub —  
  
   - Wybierz  **\<Przeglądaj … >** do określenia zestawu istniejącą regułę, która nie jest na liście.  
  
4. Kliknij przycisk **Otwórz** reguły są wyświetlane w edytorze zestawu reguł.  
  
#### <a name="to-create-a-custom-rule-set-from-multiple-existing-rule-sets"></a>Aby utworzyć regułę niestandardową zestaw z wielu istniejących zestawów reguł  
  
1.  W Eksploratorze rozwiązań kliknij prawym przyciskiem myszy projekt, a następnie wybierz **właściwości**.  
  
2.  Na **właściwości** kliknij pozycję **analizy kodu**.  
  
3.  Wybierz  **\<Wybierz wiele reguł ustawia... >** z **Uruchom ten zestaw reguł**.  
  
4.  W **apletu Dodaj lub Usuń zestawy reguł** okno dialogowe, wybierz opcję zestawów reguł, w której chcesz podstawowa Twojego nowego zestawu reguł, a następnie kliknij przycisk **OK**.  
  
5.  Zapisz nowy zestaw reguł.  
  
     Nazwa nowego zestawu reguł wybrano **Uruchom ten zestaw reguł** listy. Można zmienić nazwę wyświetlaną zestawu w następnym kroku reguł.  
  
6.  (Opcjonalnie) Aby zmienić nazwę wyświetlaną zestawu reguł na **widoku** menu, kliknij przycisk **okno właściwości**. Wpisz nazwę wyświetlaną w **nazwa** pole.  
  
7.  Aby dodać, usunąć, lub zmodyfikować zasady analizy kodu określonego w nowy zestaw reguł, kliknij przycisk **Otwórz**.  
  
## <a name="modifying-a-rule-set"></a>Modyfikowanie zestawu reguł  
  
#### <a name="to-modify-a-rule-set-in-the-rule-set-editor"></a>Aby zmodyfikować regułę ustawić w edytorze zestawu reguł  
  
-   Aby zmienić nazwę wyświetlaną zestawu reguł na **widoku** menu, kliknij przycisk **okno właściwości**. Wprowadź nazwę wyświetlaną w **nazwa** pole. Należy zauważyć, że nazwa wyświetlana może się różnić od nazwy pliku.  
  
-   Aby dodać zasady grupy do niestandardowego zestawu reguł, zaznacz pole wyboru grupy. Aby usunąć wszystkie zasady grupy, wyczyść pole wyboru.  
  
-   Aby dodać daną regułę do niestandardowego zestawu reguł, zaznacz pole wyboru reguły. Aby usunąć regułę z zestawu reguł, wyczyść pole wyboru.  
  
-   Aby zmienić akcję wykonywaną, gdy naruszenia reguły analizy kodu, kliknij w **akcji** pola dla tej reguły, a następnie wybierz jedną z następujących wartości:  
  
     **Ostrzegaj** — generuje ostrzeżenie.  
  
     **Błąd** — generuje błąd.  
  
     **Brak** — wyłącza reguły. Ta akcja jest taka sama jak usunięcie reguły z zestawu reguł.  
  
## <a name="changing-the-rule-set-editor-display"></a>Zmiana reguły Ustaw wyświetlania edytora  
  
#### <a name="to-group-filter-or-change-the-fields-in-the-rule-set-editor-by-using-the-rule-set-editor-toolbar"></a>Do grupy, filtrowanie lub zmiany pól w edytorze zestawu reguł za pomocą paska narzędzi edytora zestawu reguł  
  
-   Aby rozwinąć reguł we wszystkich grupach, kliknij **Rozwiń wszystko**.  
  
-   Aby zwinąć reguł we wszystkich grupach, kliknij **Zwiń wszystkie**.  
  
-   Aby zmienić pola, które reguły są grupowane według, zaznacz pole z **Group By** listy. Aby wyświetlić reguły niezgrupowane, wybierz  **\<Brak >**.  
  
-   Aby dodać lub usunąć pola w kolumnach regułę, kliknij przycisk **opcje kolumny**.  
  
-   Aby ukryć reguł, które nie mają zastosowanie do bieżącego rozwiązania **Ukryj reguł, które nie mają zastosowanie do bieżącego rozwiązania**.  
  
-   Aby przełączać się między pokazywaniu i ukrywaniu reguł, które są przypisane akcji błędu, kliknij przycisk **Pokaż reguły, które mogą generować błędy analizy kodu**.  
  
-   Aby przełączać się między pokazywaniu i ukrywaniu reguł, które są przypisane ostrzeżenie akcję, kliknij przycisk **Pokaż reguły, które mogą generować ostrzeżenia analizy kodu**.  
  
-   Aby przełączać się między pokazywaniu i ukrywaniu reguł, które są przypisane **Brak** działania, kliknij przycisk **Pokaż reguły, które nie są włączone**.  
  
-   Aby dodać lub usunąć domyślnej reguły ustawia bieżący zestaw reguł firmy Microsoft, kliknij przycisk **apletu Dodaj lub usuń podrzędne zestawy reguł**.  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: Konfigurowanie analizy kodu dla projektu kodu zarządzanego](../code-quality/how-to-configure-code-analysis-for-a-managed-code-project.md)   
 [Informacje o zestawie reguł analizy kodu](../code-quality/code-analysis-rule-set-reference.md)



