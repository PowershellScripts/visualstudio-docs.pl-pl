---
title: Układ dla programu Visual Studio | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
ms.assetid: c19e3022-047c-43b6-a046-a82717efed4f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 638cfc29ed2aa05a8576a2244b81f0625453076d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49816700"
---
# <a name="layout-for-visual-studio"></a>Układ dla programu Visual Studio
Większość okien dialogowych programu Visual Studio jest [układ okna dialogowego narzędzia](../../extensibility/ux-guidelines/layout-for-visual-studio.md#BKMK_UtilityDialogLayout), które są unthemed okien dialogowych standardzie postępuj zgodnie z [zasad układu okna dialogowego pulpitu Windows](/windows/desktop/uxguide/win-dialog-box). Przemieszcza się w programie Visual Studio można odświeżyć jego interfejsie użytkownika, niektóre ważniejszej okien dialogowych mają nowy projekt, który ustanawia je jak definiowanie produktu środowiska. Te [układ okna dialogowego motywem](../../extensibility/ux-guidelines/layout-for-visual-studio.md#BKMK_ThemedDialogLayout) ma wygląd kompozycji.  
  
##  <a name="BKMK_UtilityDialogLayout"></a> Układ okna dialogowego narzędzia  
  
-   Wszystkie kontrolki w oknie dialogowym narzędzia należy rozpoczynają się od góry/do lewej i przepływu w dół.  
  
-   Nigdy nie środka kontrolki w oknie dialogowym w celu wypełnienia obszaru dużych.  
  
-   Czcionka środowiska na użytek cały tekst okna dialogowego. Podczas pisania visual specyfikacji, należy określić czcionka środowiska zamiast zaznaczania określonej czcionki i rozmiar. Zobacz [czcionka środowiska](../../extensibility/ux-guidelines/fonts-and-formatting-for-visual-studio.md#BKMK_TheEnvironmentFont).  
  
-   Umożliwia obsługę celem jakości w craftsmanship w odstępy spójną kontrolę i położenia.  
  
-   Okna dialogowe może stać się bardziej złożone z większej liczby kontrolek i/lub unikatowe zestawienie kontrolki. W tych złożonych sytuacjach na odpowiednia ilość miejsca między kontroli grupowania, aby przyznać użytkownikowi przepływ logiczny można przeanalizować.  
  
### <a name="utility-dialog-layout-examples"></a>Przykłady układu okna dialogowego narzędzia  
 Wszystkie wymiary są wyrażane jako pikseli.  
  
 ![Okno dialogowe odstępy dla etykiety powyżej kontrolki](../../extensibility/ux-guidelines/media/0801-a_utilityspacingabove.png "0801 a_UtilitySpacingAbove")  
  
 **Rysunek 08.01-a: Odstępy wytycznych w oknach dialogowych narzędzia, za pomocą etykiet powyżej formantów**  
  
 ![Okno dialogowe odstępy dla etykiety z lewej strony kontrolki](../../extensibility/ux-guidelines/media/0801-b_utilityspacingleft.png "0801 b_UtilitySpacingLeft")  
  
 **Rysunek 08.01-b: Odstępy wytycznych w oknach dialogowych narzędzia, za pomocą etykiety z lewej strony kontrolki**  
  
### <a name="layout-details"></a>Szczegóły układu  
  
#### <a name="margins"></a>Marginesy  
  
-   Wszystkie okna dialogowe powinny mieć 12-pikselowe obramowanie wokół krawędzi wszystkich.  
  
-   Marginesy w ramce grupy powinna być 9 pikseli od krawędzi ramki.  
  
-   Marginesy w kontrolce karty powinny być 6 pikseli z krawędzią formantu karty.  
  
#### <a name="command-buttons"></a>Przyciski poleceń  
  
- Przyciski poleceń działają na ramki okna dialogowego, a nie na zawartość. One będzie umieszczona w dolnej prawej i powinien mieć wystarczającej ilości miejsca zmiennej powyżej, aby ustawić wyraźnie oddzielne przycisków.  
  
- W przypadku przyciski poziome, które działają w obrębie okna dialogowego konfiguracji przycisku polecenia jest pionowy stos w prawym górnym rogu. Zobacz [przycisków poleceń posługiwanie się nimi](../../extensibility/ux-guidelines/layout-for-visual-studio.md#BKMK_InteriorCommandButtons) poniżej.  
  
- Miejsce na lewo od przycisków poleceń (niższe po lewej stronie/środka okna dialogowego) jest uważany za część "poza pasmem" formantów operacji okna dialogowego. Jedyną czynnością, który powinna mającym w tym miejscu jest łącza pomocy, która jest odpowiednia dla całego zadania lub okna dialogowego.  
  
- Przyciski poleceń powinny być 75 x 23 pikseli.  
  
- Przyciski poleceń powinna być 6 pikseli od siebie.  
  
  ![Wyrównanie podstawowe przycisku](../../extensibility/ux-guidelines/media/0801-c_buttonalign.png "0801 c_ButtonAlign")  
  
  **Rysunek 08.01 — c: Wyrównanie podstawowe przycisku**  
  
#### <a name="labels"></a>Etykiety  
  
-   Wyrównaj do lewej wszystkie etykiety.  
  
-   Dla etykiet, które znajdują się powyżej kontrolki one powinien wyrównuj do lewej dokładnie kontrolką poniżej i dolnej części etykieta powinna być 5 pikseli powyżej górnej części innego formantu (na przykład pole kombi).  
  
-   Dla etykiet, które znajdują się na lewo od formantów minimalna szerokość pomiędzy etykietą i kontrolki wprowadzania jest 10 pikseli. Powinno zostać ustanowione dorozumianych drugiej kolumny do wyrównywania pola tekstowe, pola kombi lub innych kontrolek.  
  
-   Etykiety liter i są z dwukropkiem. Zobacz [styl tekstu](../../extensibility/ux-guidelines/fonts-and-formatting-for-visual-studio.md#BKMK_TextStyle).  
  
#### <a name="distance-between-controls"></a>Odległość między kontrolkami  
 Stos jest kontrolki. Nie ma żadnych bezwzględne wytyczne dotyczące odstępów między formantami skumulowany. Szczelność między kontrolkami mogą się nieco różnić między okien dialogowych. Zalecane jest 20 pikseli dla par pionowych formant/etykiety i 9 pikseli dla par pozioma kontrolka/etykiety. Odstępy minimalne kontroli dla par poziomy to 6 pikseli.  
  
 ![Zalecane odległość między kontrolkami](../../extensibility/ux-guidelines/media/0801-d_controldistance.png "0801 d_ControlDistance")  
  
 **Rysunek 08.01 — d: Zalecenia dotyczące odległość między kontrolkami**  
  
#### <a name="control-indentation"></a>Wcięcie kontroli  
 Gdy są zagnieżdżone formanty, wyrównać wewnętrzny kontrolki w poziomie z lewą krawędzią kontrolki powyżej, zwykle etykiety.  
  
 ![Zagnieżdżone kontroli nad położeniem](../../extensibility/ux-guidelines/media/0801-e_controlalign.png "0801 e_ControlAlign")  
  
 **Rysunek 08.01 — e: Zagnieżdżone kontroli nad położeniem kontrolki**  
  
#### <a name="control-width"></a>Szerokość formantu  
 Szerokość pola tekstowego lub innych podobnych kontrolek, należy nie dłuższą niż średnia dane wejściowe dla pola. Średnia słowa angielskiego jest pięć znaków. Na przykład pola tekstowego, który wymaga długiej nazwy powinna być tak długo, jak w układzie poziomym pozwala, podczas gdy listy rozwijanej dla nazw platform powinny być tylko długości, która pozwala na zapis najdłuższy.  
  
#### <a name="helper-text"></a>Tekst pomocy  
  
-   Okno dialogowe można wyświetlić tekst pomocy, który zawiera więcej informacji o przeznaczeniu okna dialogowego. To zwykle znajduje się u góry i może być zdania 1-2.  
  
-   Długość wiersza powinna być dobrze szerokości dla użytkownika przeanalizować i odczytać. Średnie okna dialogowego powinna być co najwyżej 550 pikseli szerokości.  
  
####  <a name="BKMK_InteriorCommandButtons"></a> Przyciski poleceń posługiwanie się nimi  
 W oknach dialogowych bardziej złożone wewnętrznej kontroli może być własną powiązane przycisków, które mogą mieć wpływ na, gdzie znajdują się okno dialogowe zatwierdzenia przycisków.  
  
- Wyrównanie w pionie (kolumna) wnętrza przyciski, gdy użycie **OK**/**anulować** w poziomie są ukierunkowane w prawym dolnym rogu.  
  
- Wyrównanie w poziomie (wiersz) wnętrza przyciski, gdy użycie **OK**/**anulować** w pionie są ukierunkowane w prawym górnym rogu. Ta sytuacja jest rzadziej używane.  
  
- Rozmiar przycisku posługiwanie się nimi powinien dotyczyć rozmiar przycisk standardowy, 75 x 23 pikseli, dopasowywanie rozmiaru **OK**/**anulować** przyciski, gdy jest to możliwe. Jeśli etykieta przycisku sprawia, że przycisk przekracza rozmiar przycisk standardowy, inne przyciski, w tym zestawie należy wyrównać za pomocą tego rozmiaru szersze.  
  
  ![Przyciski poziome OK i Anuluj](../../extensibility/ux-guidelines/media/0801-f_horizokcan.png "0801 f_HorizOKCan")  
  
  **Rysunek 08.01-f: Pionowy wnętrza przycisków z poziomy OK/anulować**  
  
  ![Przyciski pionowy OK i Anuluj](../../extensibility/ux-guidelines/media/0801-g_vertokcan.png "0801 g_VertOKCan")  
  
  **Rysunek 08.01-g: Poziomy przyciski posługiwanie się nimi pionowy OK/anulować**  
  
#### <a name="browse-button"></a>[Przeglądaj …] przycisk  
 **[Przeglądaj …]**  przycisków poniżej pola tekstowego powinien zawierają bardziej "Przeglądaj..." w całości, w tym wielokropka. Jeśli ilość miejsca jest ścisła lub dostępnych jest wiele **[Przeglądaj …]**  przyciski na ekranie przycisku można zmniejszyć do właśnie wielokropka.  
  
##  <a name="BKMK_ThemedDialogLayout"></a> Układ okna dialogowego motywów  
 Motywem okien dialogowych w programie Visual Studio mają jaśniejszy wygląd i oferują więcej biały. Typografia zapewnia więcej wyróżnienia i zainteresowań, oferując bardziej otwarty i ustawić odmianą rozmiary czcionek i wagi. Jeśli to możliwe, chrome i paska tytułu zostały obniżone lub usunięte. Układ tych okien dialogowych należy stosować tego podstawowego wzorca:  
  
1.  Tło okna dialogowego jest białe.  
  
2.  Istnieje reguła 1-pikselowe obramowanie kolorem szarym wartości średniej.  
  
3.  Tytuł okna dialogowego nie jest już znajduje się w pasku tytułu, ale zapewnia wizualnego zainteresowania i wyróżnić w punkcie o większym rozmiarze. (Zobacz sekcję rozmiar czcionki w [styl tekstu](../../extensibility/ux-guidelines/fonts-and-formatting-for-visual-studio.md#BKMK_TextStyle).)  
  
4.  Dzięki połączeniu z usługami dodatkowe tekstu, na przykład opis etykiety powinny być **czcionka środowiska + Bold**.  
  
5.  Posługiwanie się nimi kolumny są rozdzielane przez regułę 1-pikselowe w kolorze szarym światła.  
  
6.  Domyślne łącza mają nie znaku podkreślenia. Ustaw kursor po naciśnięciu stany się zmiana koloru oraz podkreślenia.  
  
7.  Zatwierdź przycisków (takich jak **OK**/**anulować**) znajdują się w prawym dolnym rogu.  
  
### <a name="themed-dialog-layout-examples"></a>Przykłady układu okna dialogowego motywów  
 ![Układ okna dialogowego motywem](../../extensibility/ux-guidelines/media/0801-h_themeddialog.png "0801 h_ThemedDialog")  
  
 **Rysunek 08.01-h: Okno dialogowe motywem**  
  
 ![Wymiary okna dialogowego motywem](../../extensibility/ux-guidelines/media/0801-i_themeddialogdimensions.png "0801 i_ThemedDialogDimensions")  
  
 **Rysunek 08.01-i: Motywem okno dialogowe - wymiarów**  
  
 ![Czcionki okna dialogowego motywem](../../extensibility/ux-guidelines/media/0801-j_themeddialogfonts.png "0801 j_ThemedDialogFonts")  
  
 **Rysunek 08.01-j: Motywem okno dialogowe - czcionek**  
  
 ![Okno motywem kolorów](../../extensibility/ux-guidelines/media/0801-k_themeddialogcolors.png "0801 k_ThemedDialogColors")  
  
 **Rysunek 08.01-k: Dialogowe motywem — kolory**  
  
## <a name="see-also"></a>Zobacz też  
 [Wzorce aplikacji dla programu Visual Studio](../../extensibility/ux-guidelines/application-patterns-for-visual-studio.md)   
 [Formanty (Windows)](/windows/desktop/uxguide/controls)   
 [Okna dialogowe (Windows)](/windows/desktop/uxguide/win-dialog-box)