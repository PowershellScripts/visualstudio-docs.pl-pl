---
title: "Krok 9: Sprawdź, komentowanie i testowanie kodu | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-acquisition
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: f26f79ba-c91b-4164-b87f-679a1b231c09
caps.latest.revision: "29"
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 181462529b4e66f894328d099298408a91145c6b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="step-9-review-comment-and-test-your-code"></a>Krok 9. Przejrzenie, komentowanie i testowanie kodu
Obok możesz dodać komentarz do kodu. Należy pamiętać, że nie powoduje zmiany zachowania programu jest komentarz. Ułatwi osobie, która odczytuje swój kod, aby zrozumieć, jakie operacje. Dodawanie komentarzy w kodzie jest dobrym nawyk umożliwia pobranie do. W środowisku Visual C#, dwa przekazywania ukośniki (/ /) zaznacz wiersz jako komentarz. W języku Visual Basic pojedynczego cudzysłowu (') służy do zaznacz wiersz jako komentarz. Po dodaniu komentarza, należy przetestować programu. Jest dobrym rozwiązaniem jest uruchamianie i testowanie kodu często podczas pracy w projektach, aby można było catch i rozwiązywania problemów z wcześniej, zanim ten kod pobiera bardziej skomplikowane. Ta metoda jest wywoływana *iteracyjne testowanie*.  
  
 Coś, który właśnie utworzony, a mimo że nie jest jeszcze zrobione, już można załadować obrazu. Przed Dodaj komentarz do kodu i przetestować go czasu zapoznać się z pojęciami kodu, ponieważ będzie często używane następujące pojęcia:  
  
-   Po dwukrotnym kliknięciu **Pokaż obraz** przycisk Projektant formularzy systemu Windows, IDE automatycznie dodawane *metody* do kodu programu.  
  
-   Metody to sposób organizowania kodu: jest jak kodu są grupowane razem.  
  
-   W większości przypadków, metody jest niewielka liczba elementów w określonej kolejności, takich jak jak Twoje `showButton_Click()` metoda Wyświetla okno dialogowe, a następnie załadowanie obrazu.  
  
-   Metoda składa się z kodu *instrukcje*, lub wierszy kodu. Metoda można traktować jako sposób połączyć ze sobą instrukcje kodu.  
  
-   Podczas wykonywania metody lub *o nazwie*, instrukcje w metodzie są wykonywane w kolejności, jeden po drugim, rozpoczynając od pierwszego z nich.  
  
     Oto przykład instrukcji.  
  
    ```csharp  
    pictureBox1.Load(openFileDialog1.FileName);  
    ```  
  
    ```vb  
    pictureBox1.Load(openFileDialog1.FileName)  
    ```  
  
     Instrukcje są programy wykonywanie czynności, jakie wprowadzać. W środowisku Visual C#, instrukcję zawsze kończy się średnikiem. W języku Visual Basic koniec wiersza jest końca instrukcji. (Nie średnik jest niezbędne w języku Visual Basic). Informuje powyższych instrukcji z `PictureBox` kontrolce załadować plik, który użytkownik wybrał z **OpenFileDialog** składnika.  
  
 ![łącze do wideo](../data-tools/media/playvideo.gif "PlayVideo")wersję wideo tego tematu, zobacz [samouczek 1: Tworzenie podglądu obrazów w języku Visual Basic - 5 wideo](http://go.microsoft.com/fwlink/?LinkId=205216) lub [samouczek 1: Tworzenie podglądu obrazów w C# — wideo 5](http://go.microsoft.com/fwlink/?LinkId=205206). Tych klipów wideo korzysta z wcześniejszej wersji programu Visual Studio, dlatego są niewielkie różnice w niektórych poleceń menu i inne elementy interfejsu użytkownika. Jednak koncepcje i procedury działają podobnie w bieżącej wersji programu Visual Studio.  
  
### <a name="to-add-comments"></a>Aby dodać komentarze  
  
1.  Dodaj poniższy komentarz do kodu.  
  
     [!code-vb[VbExpressTutorial1Step9_10#1](../ide/codesnippet/VisualBasic/step-9-review-comment-and-test-your-code_1.vb)]
     [!code-csharp[VbExpressTutorial1Step9_10#1](../ide/codesnippet/CSharp/step-9-review-comment-and-test-your-code_1.cs)]  
  
    > [!NOTE]
    >  Twoje **Pokaż przycisk** kliknięcia przycisku program obsługi zdarzeń jest zakończone, a działa. Uruchomieniu pisania kodu, począwszy od `if` instrukcji. `if` Instrukcja jest jak sprawdzić program, "Sprawdź tego rzecz, a w przypadku wartości true, wykonaj te akcje." W takim przypadku można stwierdzić, aby otworzyć program **Otwieranie pliku** okno dialogowe i jeśli użytkownik wybierze plik i wybiera **OK** przycisku, załadowania tego pliku w polu PictureBox.  
  
    > [!TIP]
    >  IDE korzysta z wbudowanej ułatwiają pisanie kodu, i *wstawki kodu* są tak, że jedną z metod. Fragment jest skrót, który pobiera rozwinięty w małych bloku kodu.  
    >   
    >  Widoczne są wszystkie dostępne fragmentów. Na pasku menu wybierz **narzędzia**, **Menedżerze fragmentów kodu**. Visual C#, `if` fragment jest **Visual C#** . W języku Visual Basic `if` fragmenty kodu są w **warunków i pętli**, **wzorce kodu**. Ten Menedżer umożliwia przeglądanie istniejących wstawki lub dodać własne wstawki.  
    >   
    >  Aby aktywować fragment podczas pisania kodu, wpisz ją i wybierz klawisz TAB. Wiele fragmenty kodu są wyświetlane w **IntelliSense** okna, dlatego wybierz dwa razy klawisz TAB: najpierw, aby wybrać fragment z **IntelliSense** okna, a następnie sprawdzić IDE, aby użyć fragment kodu. (Obsługuje IntelliSense `if` fragment, ale nie `ifelse` fragment.)  
  
2.  Przed uruchomieniem programu zapisać program, wybierając **Zapisz wszystko** przycisku paska narzędzi, która wygląda następująco.  
  
     ![Zapisz wszystkie przycisku paska narzędzi](../ide/media/express_iconsaveall.png "Express_IconSaveAll")  
Zapisz wszystkie przycisku  
  
     Alternatywnie, aby zapisać programu, na pasku menu, wybierz **pliku**, **Zapisz wszystko**. Jest najlepszym rozwiązaniem, aby zapisać wczesne i często.  
  
     Jest uruchomiony program powinien wyglądać poniższej ilustracji.  
  
     ![Obraz podglądu](../ide/media/express_pictureviewerdonerun.png "Express_PictureViewerDoneRun")  
Obraz podglądu  
  
### <a name="to-test-your-program"></a>Do testowania programu  
  
1.  Wybierz klawisz F5 lub **Rozpocznij debugowanie** przycisku paska narzędzi.  
  
2.  Wybierz **Pokaż obraz** przycisku do uruchomienia kodu zostało napisane. Po pierwsze, zostanie otwarty program **Otwórz plik** okno dialogowe. Sprawdź, czy filtry są widoczne w **pliki typu** listy rozwijanej w dolnej części okna dialogowego. Następnie przejdź do obrazu i otwórz go. Zazwyczaj można znaleźć przykładowe obrazy, które są dostarczane z systemem operacyjnym Windows w Twojej **Moje dokumenty** folder, wewnątrz **Moje obrazy Pictures\Sample** folderu.  
  
    > [!NOTE]
    >  Jeśli nie widać żadnych obrazów w **wybierz plik obrazu** okna dialogowego, upewnij się, że "wszystkie pliki (*.\*)" filtr jest zaznaczony na liście rozwijanej w prawej dolnej okna dialogowego.  
  
3.  Dodawanie zdjęcia i wyświetlone w Twojej PictureBox. Spróbuj zmiana rozmiaru formularz przez przeciągnięcie jego krawędzi. Ponieważ Twoje PictureBox zadokowana wewnątrz TableLayoutPanel, które jest zadokowany wewnątrz formularza obszaru obrazu będzie zmieniany tak, aby szerokość całego formularza i wypełnia top 90 procent formularza. Dlatego używane kontenerów TableLayoutPanel i FlowLayoutPanel: prowadzą formularza o rozmiarze poprawnie, gdy użytkownik zmienia jego rozmiar.  
  
     Obrazy teraz prawo, większy wykracza poza granice przeglądarkę obrazu. W następnym kroku zostanie dodana kod, aby obrazy mieści się w oknie.  
  
### <a name="to-continue-or-review"></a>Aby kontynuować lub przeglądnąć  
  
-   Aby przejść do następnego kroku samouczka, zobacz [kroku 10: pisanie kodu dla dodatkowych przycisków i pola wyboru](../ide/step-10-write-code-for-additional-buttons-and-a-check-box.md).  
  
-   Aby powrócić do poprzedniego kroku samouczka, zobacz [krok 8: wpisywanie kodu dla programu obsługi zdarzeń obrazu przycisku](../ide/step-8-write-code-for-the-show-a-picture-button-event-handler.md).