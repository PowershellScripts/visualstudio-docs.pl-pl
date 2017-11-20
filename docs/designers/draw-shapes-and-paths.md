---
title: "Rysowanie kształtów i ścieżek | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-designers
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d5378c59-e2e5-49f0-91f1-aa82d984a33c
caps.latest.revision: "10"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 2e5162a9da6fcafaaf27691081d9782191efb551
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="draw-shapes-and-paths"></a>Rysowanie kształtów i ścieżek
W Projektancie XAML *kształtu* jest dokładnie, czego można oczekiwać. Na przykład: prostokąta, okręgu lub elipsy. A *ścieżki* jest bardziej elastyczne wersji kształtu. Można wykonywać czynności, takie jak zmienić je lub połączenie ich kształtów nowego formularza.  
  
 Kształtów i ścieżek używać grafiki wektorowej, dlatego ich skaluje właściwie do wyświetlacze o wysokiej rozdzielczości. Jeśli chcesz dowiedzieć się więcej na temat grafiki wektorowej, zobacz [co to są grafiki wektorowej](https://www.youtube.com/watch?v=MoCSwF0n-io) lub [grafika wektorowa](http://www.webopedia.com/TERM/V/vector_graphics.html).  
  
 **W tym temacie:**  
  
-   [Rysuj kształt](#Shape)  
  
-   [Rysowanie ścieżki](#Path)  
  
-   [Konwertuj na ścieżkę kształtu](#Convert)  
  
-   [Łączenie ścieżek](#Combine)  
  
-   [Ścieżek złożonych](#Compound)  
  
-   [Tworzenie ścieżki przycinania](#Clipping)  
  
##  <a name="Shape"></a>Rysuj kształt  
 Można znaleźć kształtów w **zasoby** panelu.  
  
 ![Kategoria kształtów na panelu Zasoby](../designers/media/b4_shapes_assetspanel.png "b4_Shapes_AssetsPanel")  
  
 Przeciągnij dowolnego kształtu, który ma obszaru roboczego. Następnie można dojść do kształtu skalowanie, obracanie, przenoszenie i pochylanie kształtu.  
  
 ![](../designers/media/84261e83-3091-4490-ab58-4218b188439e.png "84261e83-3091-4490-ab58-4218b188439e")  
  
##  <a name="Path"></a>Rysowanie ścieżki  
 Ścieżka jest szereg połączonych linii i krzywych. Użyj ścieżki do kształtów interesujące, które nie są dostępne w **zasoby** panelu.  
  
 Ścieżkę można zdefiniować przy użyciu linii, Pióro lub ołówka. Następujące narzędzia można znaleźć **narzędzia** panelu.  
  
 ![](../designers/media/717956a8-b6a5-4e37-8af3-70bcfc78c82a.png "717956a8-b6a5-4e37-8af3-70bcfc78c82a")![](../designers/media/8fbbbb21-be83-4cf6-903b-3a49f00c9860.png "8fbbbb21-be83-4cf6-903b-3a49f00c9860")  
  
### <a name="draw-a-straight-line"></a>Rysowanie prostej  
 Użyj **pióra** narzędzie ![](../designers/media/894f8612-e0ed-4e00-84cf-a9bc8f38fc54.png "894f8612-e0ed-4e00-84cf-a9bc8f38fc54"), lub **wiersza** narzędzia ![](../designers/media/eb618397-5283-48be-8396-3449be7b6fbf.png "eb618397-5283-48be-8396-3449be7b6fbf").  
  
 **Za pomocą pióra**![](../designers/media/894f8612-e0ed-4e00-84cf-a9bc8f38fc54.png "894f8612-e0ed-4e00-84cf-a9bc8f38fc54")  
  
 W obszarze roboczym kliknij raz, aby zdefiniować punkt początkowy, a następnie kliknij ponownie, aby zdefiniować końca wiersza.  
  
 **Narzędzia wiersza**![](../designers/media/eb618397-5283-48be-8396-3449be7b6fbf.png "eb618397-5283-48be-8396-3449be7b6fbf")  
  
 W obszarze roboczym przeciągnij, z którym chcesz wiersza, aby uruchomić, a następnie zwolnij w momencie, w którym ma punktu końcowego linii.  
  
### <a name="draw-a-curve"></a>Rysowanie krzywych  
 Użyj **pióra** narzędzia ![](../designers/media/894f8612-e0ed-4e00-84cf-a9bc8f38fc54.png "894f8612-e0ed-4e00-84cf-a9bc8f38fc54").  
  
 W obszarze roboczym kliknij raz zdefiniować punkt początkowy wiersza, kliknij i przeciągnij wskaźnik do utworzenia żądanego krzywą.  
  
 Jeśli chcesz zamknąć ścieżkę, kliknij pierwszy punkt w wierszu.  
  
### <a name="change-the-shape-of-a-curve"></a>Zmiana kształtu krzywej  
 Użyj **bezpośredni wybór** narzędzia ![](../designers/media/6dd6571f-c116-451d-8dd2-1f88b8406362.png "6dd6571f-c116-451d-8dd2-1f88b8406362").  
  
 Kliknij kształt, a następnie przeciągnij dowolnego punktu kształtu, aby zmienić krzywej kształtów.  
  
### <a name="draw-a-free-form-path"></a>Rysowanie ścieżki dowolnej  
 Użyj **ołówka** narzędzia ![](../designers/media/509dc167-734f-46c9-b012-987ee63450cd.png "509dc167-734f-46c9-b012-987ee63450cd").  
  
 W obszarze roboczym narysować ścieżkę dowolnych tak samo, jak przy użyciu rzeczywistego ołówka.  
  
### <a name="remove-part-of-a-path"></a>Usuń części ścieżki  
 Użyj **bezpośredni wybór** narzędzia ![](../designers/media/6dd6571f-c116-451d-8dd2-1f88b8406362.png "6dd6571f-c116-451d-8dd2-1f88b8406362").  
  
 Wybierz ścieżkę, która zawiera segment chcesz usunąć, a następnie kliknij przycisk **usunąć** przycisku.  
  
### <a name="remove-a-point-in-a-path"></a>Usuń punkt w ścieżce  
 Użyj **wybór** narzędzie ![](../designers/media/2ff91340-477e-4efa-a0f7-af20851e4daa.png "2ff91340-477e-4efa-a0f7-af20851e4daa")i **pióra** narzędzia ![](../designers/media/894f8612-e0ed-4e00-84cf-a9bc8f38fc54.png "894f8612-e0ed-4e00-84cf-a9bc8f38fc54").  
  
 Użyj **wybór** narzędzie ![](../designers/media/2ff91340-477e-4efa-a0f7-af20851e4daa.png "2ff91340-477e-4efa-a0f7-af20851e4daa") aby wybrać ścieżkę. Następnie należy użyć **pióra** narzędzie ![](../designers/media/894f8612-e0ed-4e00-84cf-a9bc8f38fc54.png "894f8612-e0ed-4e00-84cf-a9bc8f38fc54") kliknij punkt, który chcesz usunąć.  
  
### <a name="add-a-point-to-a-path"></a>Dodaj punkt do ścieżki  
 Użyj **wybór** narzędzie ![](../designers/media/2ff91340-477e-4efa-a0f7-af20851e4daa.png "2ff91340-477e-4efa-a0f7-af20851e4daa")i **pióra** narzędzia ![](../designers/media/894f8612-e0ed-4e00-84cf-a9bc8f38fc54.png "894f8612-e0ed-4e00-84cf-a9bc8f38fc54").  
  
 Użyj **wybór** narzędzie ![](../designers/media/2ff91340-477e-4efa-a0f7-af20851e4daa.png "2ff91340-477e-4efa-a0f7-af20851e4daa") aby wybrać ścieżkę. Użyj **pióra** narzędzia ![](../designers/media/894f8612-e0ed-4e00-84cf-a9bc8f38fc54.png "894f8612-e0ed-4e00-84cf-a9bc8f38fc54") można kliknąć ścieżkę, w której chcesz dodać punkt.  
  
##  <a name="Convert"></a>Konwertuj na ścieżkę kształtu  
 Aby zmodyfikować kształtu w taki sam sposób, aby zmodyfikować ścieżkę, przekonwertuj kształt do ścieżki.  
  
 **Obejrzyj krótki klip wideo:** ![Konfigurowanie funkcji zainstalowane](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [Praca ze ścieżkami: przekonwertować kształt na ścieżkę](https://www.youtube.com/watch?v=Io5bC0-nH6Q#t=147).  
  
##  <a name="Combine"></a>Łączenie ścieżek  
 Ścieżki i kształty można łączyć w pojedynczą ścieżkę.  
  
 ![](../designers/media/2df17a5d-a338-4ef4-96c5-dae51cc1ca8a.png "2df17a5d-a338-4ef4-96c5-dae51cc1ca8a")  
  
|||||  
|-|-|-|-|  
|![](../designers/media/b1_1.png "B1_1")|Dwa kształty przed łączenie|![](../designers/media/b1_4.png "B1_4")|INTERSECT|  
|![](../designers/media/b1_2.png "B1_2")|Łączenia|![](../designers/media/b1_5.png "B1_5")|Wyklucz nachodzenie|  
|![](../designers/media/b1_3.png "B1_3")|Podziel|![](../designers/media/b1_6.png "B1_6")|Odejmowanie|  
  
 **Obejrzyj krótki klip wideo:** ![Konfigurowanie funkcji zainstalowane](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [Praca ze ścieżkami: łączenia ścieżek](https://www.youtube.com/watch?v=Io5bC0-nH6Q#t=195).  
  
##  <a name="Compound"></a>Ścieżek złożonych  
 Po utworzeniu złożony ścieżki przecinających się część ścieżki jest odejmowany od wyniku, a ścieżka przejmuje visual właściwości znajdujących się najniżej ścieżki.  
  
 Możesz można podzielić złożony ścieżki po jego utworzeniu.  
  
 ![](../designers/media/2157a8aa-d9a7-4de4-8de5-b10d28f08a84.png "2157a8aa-d9a7-4de4-8de5-b10d28f08a84")  
  
 **Obejrzyj krótki klip wideo:** ![Konfigurowanie funkcji zainstalowane](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [Praca ze ścieżkami: Tworzenie złożonego ścieżki](https://www.youtube.com/watch?v=Io5bC0-nH6Q).  
  
##  <a name="Clipping"></a>Tworzenie ścieżki przycinania  
 Ścieżka wycinka jest ścieżkę lub kształt, który jest stosowany do innego obiektu ukrycie części maskowanego obiektu, które wykraczają poza ścieżki przycinania.  
  
 ![](../designers/media/22471e98-a841-4f39-a3ef-36090cf5a625.png "22471e98-a841-4f39-a3ef-36090cf5a625")  
  
 **Obejrzyj krótki klip wideo:** ![Konfigurowanie funkcji zainstalowane](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [Praca ze ścieżkami: Tworzenie ścieżki przycinania](https://www.youtube.com/watch?v=Io5bC0-nH6Q#t=232).  
  
## <a name="see-also"></a>Zobacz też  
 [Tworzenie interfejsu użytkownika przy użyciu programu Blend for Visual Studio](../designers/creating-a-ui-by-using-blend-for-visual-studio.md)