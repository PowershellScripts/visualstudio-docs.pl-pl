---
title: 'Porady: Tworzenie skojarzeń między typami (Projektant klas) | Dokumentacja firmy Microsoft'
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
- vs.classdesigner.associationline
helpviewer_keywords:
- types [Visual Studio], associations
- association lines, defining (Class Designer)
- defining association lines (Class Designer)
- associations, types
- association lines
ms.assetid: adccb9c8-2f8a-4086-9fa9-f70f99fb6e00
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: ad870c9b470e96a120e334c79ed5b36e44cca41a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49247887"
---
# <a name="how-to-create-associations-between-types-class-designer"></a>Porady: Tworzenie skojarzeń między typami (Projektant klas)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Linie skojarzenia w Konstruktorze klasy pokazują relacje klas na diagramie. Linia skojarzenia reprezentuje klasę, która jest typem właściwości lub polem innej klasy w projekcie. Linii skojarzeń zwykle używa się do ilustrowania najważniejszych relacji między klasami w projekcie.  
  
 Podczas gdy można wyświetlić wszystkie pola i właściwości jako skojarzenia, więcej sensu ma wyświetlanie tylko ważnych elementów członkowskich jako skojarzeń, w zależności od tego, co zamierzasz podkreślić na diagramie. (Można wyświetlić mniej ważne elementy członkowskie jako zwykłe elementy członkowskie lub je całkowicie ukryć.)  
  
> [!NOTE]
>  Projektant klasy obsługuje tylko jednokierunkowe skojarzenia.  
  
### <a name="to-define-an-association-line-in-the-class-diagram"></a>Aby zdefiniować linię skojarzenia na Diagramie klasy  
  
1.  W przyborniku, w obszarze Projektant klasy, wybierz **skojarzenie**.  
  
2.  Narysuj linię między dwoma kształtami, które chcesz połączyć przez skojarzenie.  
  
     Nowa właściwość jest tworzona w pierwszej klasie. Ta właściwość służy jako linia skojarzenia, (a nie jako właściwość w ramach przedziału w kształcie) z domyślną nazwą. Jej typ to kształt, na który wskazuje linia skojarzenia.  
  
### <a name="to-change-the-name-of-an-association"></a>Aby zmienić nazwę skojarzenia  
  
-   Na powierzchni diagramu kliknij etykietę linii skojarzenia i ją wyedytuj.  
  
 \- lub —  
  
1.  Kliknij kształt, który zawiera właściwość, która jest wyświetlana jako skojarzenie.  
  
     Kształt uzyskuje fokus, a jego składowe są prezentowane w oknie Szczegóły klasy i w oknie Właściwości.  
  
2.  W oknie Szczegóły klasy lub w oknie Właściwości, wyedytuj pole nazwy dla tej właściwości, a następnie naciśnij klawisz Enter.  
  
     Nazwa jest aktualizowana w **szczegóły klasy** okna w linii skojarzenia, w oknie dialogowym właściwości, a w kodzie.  
  
## <a name="see-also"></a>Zobacz też  
 [Instrukcje: Zmiana między notacją składowych i notacją skojarzeń (Projektant klas)](../ide/how-to-change-between-member-notation-and-association-notation-class-designer.md)



