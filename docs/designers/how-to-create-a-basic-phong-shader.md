---
title: 'Porady: Tworzenie podstawowego cieniowania Phong | Dokumentacja firmy Microsoft'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-designers
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c7c69da8-142b-4d3b-9be9-4be0d5970b25
caps.latest.revision: "13"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 29def0d3aef8a097f5b956bd43df7d8b53abebb9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-create-a-basic-phong-shader"></a>Porady: tworzenie podstawowego modułu cieniowanie Phong
Ten dokument przedstawia sposób umożliwiają utworzenie cieniowania oświetlenia, implementujący klasycznego modelu oświetlenia Phong Designer programu do cieniowania i języka programu do cieniowania wykres skierowane (DGSL).  
  
 W tym dokumencie przedstawiono następujące działania:  
  
-   Dodawanie węzłów do programu do cieniowania wykresu.  
  
-   Rozłączanie węzłów  
  
-   Łączenie węzłów  
  
## <a name="the-phong-lighting-model"></a>Model oświetlenia Phong  
 Model oświetlenia Phong rozszerza Lambert oświetlenia modelu do uwzględnienia odblasków wyróżnianiem, która symuluje odbicia właściwości powierzchni. Odblasków składników zapewnia dodatkowego oświetlenia z tym samym kierunkową źródła światła, które są używane w modelu oświetlenia Lambert, ale jej udziału ostateczny kolor jest przetwarzany inaczej. Wyróżnianie odblasków ma wpływ na co powierzchni sceny inaczej, na podstawie relacji między kierunku widoku, kierunek źródła światła i orientację powierzchni. Jest to produkt koloru odblasków, odblasków zasilania i orientację powierzchnią i kolor, intensywność i kierunek światła źródeł. Powierzchnie odzwierciedlające źródła światła bezpośrednio w przeglądarce odbierania maksymalny udział odblasków uprawnia do powierzchni odzwierciedlające źródła światła od obserwatora nie udziału. Zgodnie z modelem oświetlenia Phong są łączone do określenia kolorów i intensywność wyróżnianie odblasków dla każdego punktu w obiekcie jeden lub więcej składników odblasków, a następnie są dodawane do wyniku modelu oświetlenia Lambert wygenerowało ostateczny kolor piksela .  
  
 Aby uzyskać więcej informacji na temat modelu oświetlenia Lambert, zobacz [porady: Tworzenie podstawowego cieniowania Lambert](../designers/how-to-create-a-basic-lambert-shader.md).  
  
 Przed rozpoczęciem upewnij się, że **właściwości** okna i **przybornika** są wyświetlane.  
  
#### <a name="to-create-a-phong-shader"></a>Aby utworzyć cieniowania Phong  
  
1.  Utwórz Lambert programu do cieniowania, zgodnie z opisem w [porady: Tworzenie podstawowego cieniowania Lambert](../designers/how-to-create-a-basic-lambert-shader.md).  
  
2.  Odłącz **Lambert** węzła z **ostateczny kolor** węzła. Wybierz **RGB** terminali z **Lambert** węzeł, a następnie wybierz pozycję **przerwanie łączy**. Dzięki temu miejsce na węźle, który jest dodawany w następnym kroku.  
  
3.  Dodaj **Dodaj** węzła do wykresu. W **przybornika**w obszarze **matematyczne**, wybierz pozycję **Dodaj** i przenieść ją na powierzchnię projektu.  
  
4.  Dodaj **Specular** węzła do wykresu. W **przybornika**w obszarze **narzędzie**, wybierz pozycję **Specular** i przenieść ją na powierzchnię projektu.  
  
5.  Dodaj udział odblasków. Przenieś **dane wyjściowe** terminali z **Specular** węzeł **X** terminali z **Dodaj** węzeł, a następnie przenieść **danych wyjściowych**  terminali z **Lambert** węzeł **Y** terminali z **Dodaj** węzła. Te połączenia łączyć wkładów całkowita kolor rozpraszania i odblasków dla piksela.  
  
6.  Wartość obliczana koloru nawiązać połączenia z ostateczny kolor. Przenieś **dane wyjściowe** terminali z **Dodaj** węzeł **RGB** terminali z **ostateczny kolor** węzła.  
  
 Na poniższej ilustracji przedstawiono ukończone programu do cieniowania wykres i Podgląd programu do cieniowania zastosowano do modelu teapot.  
  
> [!NOTE]
>  Aby lepiej zaprezentować efekt cieniowania na tej ilustracji, kolor pomarańczowy został określony przy użyciu **MaterialDiffuse** został określony parametr programu do cieniowania i zakończenia wyszukiwania metaliczne przy użyciu **MaterialSpecular** i **MaterialSpecularPower** parametrów. Informacje o istotnych parametrach, zobacz sekcję Podgląd programów do cieniowania w [Designer programu do cieniowania](../designers/shader-designer.md).  
  
 ![Wykres programu do cieniowania i podgląd jego wpływu](../designers/media/digit-lighting-graph.png "cyfrę-oświetlenia-wykresu")  
  
 Niektórych kształtów udostępniać lepsze podglądy niektórych programów do cieniowania. Aby uzyskać więcej informacji na temat wersji preview programów do cieniowania w projektancie programu do cieniowania, zobacz sekcję Podgląd programów do cieniowania w [Designer programu do cieniowania](../designers/shader-designer.md)  
  
 Na poniższej ilustracji przedstawiono programu do cieniowania, które jest opisane w tym dokumencie dotyczą 3-w modelu. **MaterialSpecular** właściwość ma wartość (1,00, 0,50, 0,20, 0,00), a jego **MaterialSpecularPower** właściwość jest ustawiona na 16.  
  
> [!NOTE]
>  **MaterialSpecular** właściwość określa jawnego Zakończ powierzchni materiału. Powierzchni połysku wysokiej, takich jak szkła lub plastiku zwykle odblasków kolor, który jest jasne odcień biały. Powierzchnia metali zwykle odblasków kolor, który znajduje się w pobliżu jego kolor rozpraszania. Powierzchnia Zakończ Satyna zwykle odblasków kolor, który jest ciemny odcień szarości.  
>   
>  **MaterialSpecularPower** właściwość określa, jak intensywny są światła odblasków. Wysoka uprawnień odblasków symulować bardziej matowe, zlokalizowany więcej wyróżnia. Bardzo małe odblasków uprawnień symulować intensywny, polegających na usuwaniu najważniejsze funkcje, które mogą oversaturate i Ukryj kolor całej powierzchni.  
  
 ![Zastosowano do modelu oświetlenia Phong](../designers/media/digit-lighting-model.png "cyfrę oświetlenia modelu")  
  
 Aby uzyskać więcej informacji dotyczących sposobu stosowania programu do cieniowania 3-w modelu, zobacz [porady: dotyczą programu do cieniowania 3-w modelu](../designers/how-to-apply-a-shader-to-a-3-d-model.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: dotyczą programu do cieniowania 3-w modelu](../designers/how-to-apply-a-shader-to-a-3-d-model.md)   
 [Porady: eksportowanie programu do cieniowania](../designers/how-to-export-a-shader.md)   
 [Porady: tworzenie cieniowania Lambert podstawowe](../designers/how-to-create-a-basic-lambert-shader.md)   
 [Projektant programu do cieniowania](../designers/shader-designer.md)   
 [Węzły projektanta programu do cieniowania](../designers/shader-designer-nodes.md)