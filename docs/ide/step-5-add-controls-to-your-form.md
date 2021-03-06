---
title: 'Krok 5: Dodawanie formantów do formularza'
ms.custom: ''
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: conceptual
ms.assetid: dc2746f4-0b5c-4674-9ef7-f40f94150f52
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a7a0167d4d5af125e706350002ccf8a17e459414
ms.sourcegitcommit: 58052c29fc61c9a1ca55a64a63a7fdcde34668a4
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34748559"
---
# <a name="step-5-add-controls-to-your-form"></a>Krok 5: Dodawanie formantów do formularza
W tym kroku zostanie Dodaj formanty, takie jak <xref:System.Windows.Forms.PictureBox> kontroli i <xref:System.Windows.Forms.CheckBox> sterowania do formularza. Następnie dodaj <xref:System.Windows.Forms.Button> formantów do formularza.

 ![łącze do wideo](../data-tools/media/playvideo.gif)wersję wideo tego tematu, zobacz [samouczek 1: Tworzenie podglądu obrazów w języku Visual Basic - 2 wideo](http://go.microsoft.com/fwlink/?LinkId=205211) lub [samouczek 1: Tworzenie podglądu obrazów w języku C# - 2 wideo](http://go.microsoft.com/fwlink/?LinkId=205200). Tych klipów wideo korzysta z wcześniejszej wersji programu Visual Studio, dlatego są niewielkie różnice w niektórych poleceń menu i inne elementy interfejsu użytkownika. Jednak koncepcje i procedury działają podobnie w bieżącej wersji programu Visual Studio.

## <a name="to-add-controls-to-your-form"></a>Do dodawania formantów do formularza

1.  Przejdź do **przybornika** kartę (znajdujący się po lewej stronie programu Visual Studio IDE) i rozwiń **formanty standardowe** grupy. Przedstawia najbardziej typowych formantów, które widać w formularzach.

2.  Wybierz **TableLayoutPanel** formantu w formularzu. Aby sprawdzić, czy wybrano TableLayoutPanel, upewnij się, że jego nazwa jest wyświetlana w polu listy rozwijanej w górnej części **właściwości** okna. Możesz również kontrolek formularza za pomocą pola listy rozwijanej w górnej części **właściwości** okna. Wybieranie formantu w ten sposób można łatwiejsze niż wybieranie niewielki rozmiar formantu za pomocą myszy.

3.  Kliknij dwukrotnie **PictureBox** element, aby dodać formantu PictureBox do formularza. Ponieważ TableLayoutPanel jest zadokowana wypełnienie formularza, IDE dodaje PictureBox — formant do pierwszej pustej komórce (lewym górnym rogu).

4.  Wybierz nowy **PictureBox** sterowania, aby go zaznaczyć, a następnie wybierz czarny trójkąt na nowe formantu PictureBox, aby wyświetlić jego Lista zadań, jak pokazano na poniższej ilustracji.

     ![Zadania PictureBox](../ide/media/express_pictureboxtasks.png)
**PictureBox** zadań

    > [!NOTE]
    >  Jeśli dodasz przypadkowo niewłaściwego typu formantu do Twojej TableLayoutPanel, możesz go usunąć. Kliknij prawym przyciskiem myszy formantu, a następnie wybierz **usunąć** na jego menu kontekstowego. Można również usunąć formantów w formularzu, za pomocą paska menu. Na pasku menu wybierz **Edytuj** > **Cofnij**, lub **Edytuj** > **usunąć**.

5.  Wybierz **Zadokuj w kontenerze nadrzędnym** łącza. To są automatycznie ustawiane w polu PictureBox **dokowania** właściwości **wypełnienia**. Aby zobaczyć, wybierz **PictureBox** sterowania, wybierz ją, przejdź do **właściwości** oknie i upewnij się, że **dokowania** właściwość jest ustawiona na **wypełnienia**.

6.  Wprowadź PictureBox obejmuje zarówno kolumn, zmieniając jej **ColumnSpan** właściwości. Wybierz **PictureBox** kontroli i ustawić jej **ColumnSpan** właściwości **2**. Ponadto po elemencie PictureBox jest pusta, chcesz pokazać pustej ramki. Ustaw jego **BorderStyle** właściwości **Fixed3D**.

    > [!NOTE]
    >  Jeśli nie widzisz **ColumnSpan** właściwość PictureBox Twoje, to jest prawdopodobne, że element PictureBox został dodany do formularza zamiast TableLayoutPanel. Aby rozwiązać ten problem, wybierz **PictureBox**, usuń go, wybierz polecenie **TableLayoutPanel**, a następnie dodaj nowy element PictureBox.

7.  Wybierz **TableLayoutPanel** na formularzu, a następnie dodać kontrolkę pola wyboru w formularzu. Kliknij dwukrotnie **wyboru** elementu **przybornika** Aby dodać nową kontrolkę wyboru do następnej komórki wolnego w tabeli. Ponieważ elementu PictureBox zajmuje dwóch pierwszych komórek w TableLayoutPanel, formant wyboru został dodany do lewej dolnej komórki. Wybierz **tekst** właściwości i wpisz wyraz **Stretch**, jak pokazano na poniższej ilustracji.

     ![TextBox — formant z właściwością Stretch](../ide/media/express_pictureviewercheckbox.png)
**pole tekstowe** sterować za pomocą **Stretch** właściwości

8.  Wybierz **TableLayoutPanel** na formularzu, a następnie przejdź do **kontenery** w **przybornika** (gdzie masz formantu TableLayoutPanel) i kliknij dwukrotnie **FlowLayoutPanel** element, aby dodać nową kontrolkę do ostatniej komórki w elemencie PictureBox (prawy dolny róg). Następnie dock FlowLayoutPanel w TableLayoutPanel (przez wybranie **Zadokuj w kontenerze nadrzędnym** na liście zadań czarny trójkąt FlowLayoutPanel lub przez ustawienie FlowLayoutPanel **Dock** dla właściwości **wypełnienia**).

    > [!NOTE]
    >  A <xref:System.Windows.Forms.FlowLayoutPanel> jest kontenerem, który rozmieszcza innych kontrolek w przejrzysty wierszy w kolejności. Podczas zmiany rozmiaru FlowLayoutPanel, jeśli ma ona miejsca do określania układu wszystkich jej kontrolek w jednym wierszu, robi to. W przeciwnym razie tworzy je w wierszach, jeden nad drugim. FlowLayoutPanel — użyje do przechowywania czterech przycisków. Jeśli Rozmieść przyciski jedną na innego po dodaniu top, upewnij się, że przed dodaniem przycisków jest zaznaczone FlowLayoutPanel. Mimo że wcześniej stwierdzono, że każda komórka może zawierać tylko jeden formant, komórkę prawym dolnym TableLayoutPanel zawiera cztery kontrolki przycisku. Jest to spowodowane przełączeniem formant w komórce, który zawiera inne formanty. Tego rodzaju kontroli nosi nazwę kontenera, a FlowLayoutPanel jest kontenerem.

## <a name="to-add-buttons"></a>Aby dodać przyciski

1.  Wybierz nowe FlowLayoutPanel, który został dodany. Przejdź do **formanty standardowe** w **przybornika** i kliknij dwukrotnie **przycisk** element, aby dodać kontrolkę przycisku o nazwie **button1** do użytkownika FlowLayoutPanel —. Powtórz, aby dodać inny przycisk. IDE Określa, że jest już przycisku o nazwie **button1** i wywołuje kolejnego **button2**.

2.  Zazwyczaj dodaje się przyciski, za pomocą **przybornika**. Tym razem wybierz **button2**, a następnie na pasku menu wybierz pozycję **Edytuj** > **kopiowania** (lub naciśnij klawisz **Ctrl** + **C**). Na pasku menu wybierz **Edytuj** > **Wklej** (lub naciśnij klawisz **Ctrl**+**V**) Wklej kopię tego przycisku. Wklej go teraz ponownie. Teraz dodał IDE **button3** i **button4** do FlowLayoutPanel.

    > [!NOTE]
    >  Można skopiować i wkleić żadnego formantu. IDE nazwy i umieszcza nowe formanty w sposób logiczny. Po wklejeniu formantu do kontenera IDE wybiera następny logicznego miejsca do umieszczenia.

3.  Kliknij pierwszy przycisk i ustawić jej **tekst** właściwości **Pokaż obraz**. Następnie ustaw **tekst** właściwości trzech kolejnych przycisków **Wyczyść obraz**, **kolor tła**, i **Zamknij**.

4.  Następnym krokiem jest rozmiar przycisków i rozmieszcza je tak one Wyrównaj do prawej strony panelu. Wybierz **FlowLayoutPanel** i przyjrzyj się jego **wartość FlowDirection** właściwości. Zmień ją, dlatego jest ustawiona **RightToLeft**. Natychmiast po wykonaniu czynności przycisków powinien umożliwia im dopasowanie się do prawej krawędzi komórki, a ich ostatniej strony, aby **Pokaż obraz** znajduje się przycisk po prawej stronie.

    > [!NOTE]
    >  W przypadku przycisków nadal w niewłaściwej kolejności, możesz przeciągnąć przycisków wokół FlowLayoutPanel do zmiany rozmieszczenia ich w dowolnej kolejności. Wybierz przycisk i przeciągnij go w lewo lub w prawo.

5.  Wybierz **Zamknij** przycisk, aby go wybrać. Naciśnij i przytrzymaj **Ctrl** klucza i wybierz inne trzy przyciski, dzięki czemu są wszystkie zaznaczone. Natomiast w przypadku wybrania wszystkich przycisków Przejdź do **właściwości** okno i przewiń w górę do **AutoSize** właściwości. Ta właściwość określa, że przycisk, aby automatycznie Zmień rozmiar dopasuje wszystkie jego tekstu. Ustaw ją na **true**. Przyciski komputera należy teraz prawidłowo ustalać i znajdować się w odpowiedniej kolejności. (Tak długo, jak wybrane są wszystkie cztery przyciski, można zmienić wszystkie cztery **AutoSize** właściwości w tym samym czasie.) Na poniższej ilustracji przedstawiono cztery przyciski.

     ![Obraz podglądu z czterech przycisków](../ide/media/express_autosize.png)
**obraz podglądu** z czterech przycisków

6.  Teraz należy uruchomić program ponownie, aby zobaczyć nowo ustanowione limit formularza. Wybieranie przycisków i pola wyboru nic nie robi jeszcze, ale będzie ona działać wkrótce.

## <a name="to-continue-or-review"></a>Aby kontynuować lub przeglądnąć

-   Aby przejść do następnego kroku samouczka, zobacz [krok 6: nazw formantom przycisków](../ide/step-6-name-your-button-controls.md).

-   Aby powrócić do poprzedniego kroku samouczka, zobacz [krok 4: określenie układu formularza przy użyciu formantu TableLayoutPanel](../ide/step-4-lay-out-your-form-with-a-tablelayoutpanel-control.md).
