---
title: 'Porady: tworzenie cieniowania tekstury podstawowej | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 5af113fb-6415-4be0-8b23-10fddb10e80a
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 18bb4f1ad4dfc3428e8dc30958013438de22e13a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49898541"
---
# <a name="how-to-create-a-basic-texture-shader"></a>Porady: tworzenie cieniowania tekstury podstawowej
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W tym dokumencie przedstawiono sposób umożliwia tworzenie cieniowania tekstury jednego języka programu do cieniowania wykres kierowany (DGSL) i Projektant programu do cieniowania. Ten program do cieniowania Ustawia kolor końcowy bezpośrednio RGB i wartości alfa, które są próbkowane z tekstury.  
  
 Ten dokument przedstawia te działania:  
  
-   Usuwanie węzłów z wykresu programu do cieniowania  
  
-   Dodawanie węzłów do wykresu  
  
-   Ustawianie parametrów programu do cieniowania  
  
-   Ustawienie parametru widoczności  
  
-   Łączenie z węzłami  
  
## <a name="creating-a-basic-texture-shader"></a>Tworzenie cieniowania tekstury podstawowej  
 Podstawowa, jednego tekstury modułu cieniującego można zaimplementować, pisząc wartości kolorów i alfa próbki tekstury bezpośrednio na kolor końcowych danych wyjściowych.  
  
 Przed rozpoczęciem upewnij się, że **właściwości** okna i **przybornika** są wyświetlane.  
  
#### <a name="to-create-a-basic-texture-shader"></a>Aby utworzyć cieniowania tekstury podstawowej  
  
1. Tworzenie modułu cieniującego DGSL chcesz pracować. Aby uzyskać informacje dotyczące sposobu dodawania modułu cieniującego DGSL do projektu, zobacz sekcję pierwsze kroki w [Shader Designer](../designers/shader-designer.md).  
  
2. Usuń **koloru punktu** węzła. W **wybierz** tryb, wybierz **koloru punktu** węzła, a następnie na pasku menu wybierz **Edytuj**, **Usuń**. To sprawia, że miejsce na węzeł, który zostanie dodany do następnego kroku.  
  
3. Dodaj **próbki tekstury** węzła do wykresu. W **przybornika**w obszarze **tekstury**, wybierz opcję **próbki tekstury** i przenieś go do powierzchni projektowej.  
  
4. Dodaj **koordynować tekstury** węzła do wykresu. W **przybornika**w obszarze **tekstury**, wybierz opcję **koordynować tekstury** i przenieś go do powierzchni projektowej.  
  
5. Wybierz teksturę do zastosowania. W **wybierz** tryb, wybierz **próbki tekstury** węzła, a następnie w polu **właściwości** okna, określ teksturę, która ma być za pomocą **nazwy pliku**  właściwości.  
  
6. Udostępnienie tekstury publicznie. Wybierz **próbki tekstury** węzła, a następnie w polu **właściwości** oknie **dostępu** właściwości **publicznych**. Teraz można ustawić tekstury z innego narzędzia, takie jak **edytora modelu**.  
  
7. Połącz się próbki tekstury z współrzędnych tekstury. W **wybierz** tryb, Przenieś **dane wyjściowe** terminali z **koordynować tekstury** węzeł, aby **UV** terminali z **tekstury Przykładowe** węzła. To połączenie pobiera próbki tekstury na określonych współrzędnych.  
  
8. Połącz się ostateczny kolor z próbki tekstury. Przenieś **RGB** terminali z **próbki tekstury** węzeł **RGB** terminali z **ostateczny kolor** węzeł, a następnie przenieść **Alfa** terminali z **próbki tekstury** węzeł **alfa** terminali z **ostateczny kolor** węzła.  
  
   Poniższej ilustracji ukończone programu do cieniowania programu graph i wersję zapoznawczą programu do cieniowania stosowane do modułu.  
  
> [!NOTE]
>  Na tej ilustracji płaszczyznę jest używany jako kształt (wersja zapoznawcza), a określono tekstury lepiej wykazać efekt programu do cieniowania.  
  
 ![Wykres modułu cieniującego i podgląd efektów jej](../designers/media/digit-texture-effect.png "cyfrę tekstury efektu")  
  
 Niektórych kształtów udostępniać lepsze wersje zapoznawcze niektórych programów do cieniowania. Aby uzyskać więcej informacji na temat programów do cieniowania w projektancie programu do cieniowania w wersji zapoznawczej, zobacz [Shader Designer](../designers/shader-designer.md)  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: stosowanie cieniowania do modelu 3-D](../designers/how-to-apply-a-shader-to-a-3-d-model.md)   
 [Edytor obrazów](../designers/image-editor.md)   
 [Projektant programu do cieniowania](../designers/shader-designer.md)   
 [Węzły projektanta cieniowania](../designers/shader-designer-nodes.md)



