---
title: "Porady: Tworzenie dziedziczenia pomiędzy typami (Projektant klas) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.classdesigner.inheritanceline
helpviewer_keywords:
- inheritance, relationship defining
- relationships, defining inheritance
ms.assetid: 3786a21c-8022-4bf5-9d13-740fd354e93c
caps.latest.revision: "30"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 72cb7612df9c0a80df131ee122df100dc6eeedbe
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-create-inheritance-between-types-class-designer"></a>Porady: Tworzenie dziedziczenia pomiędzy typami (Projektant klas)
Aby utworzyć relację dziedziczenia między dwoma typami na diagramie klas, za pomocą projektanta klas, połączenie typu podstawowego z jego pochodny typ lub typy. Może mieć relację dziedziczenia między dwiema klasami, między klasą a interfejsem lub między dwa interfejsy.  
  
### <a name="to-create-an-inheritance-between-types"></a>Aby utworzyć dziedziczenia pomiędzy typami  
  
1.  Z projektu w Eksploratorze rozwiązań Otwórz plik diagramu (.cd) klasy.  
  
     Jeśli nie masz diagramu klas, należy go utworzyć. Zobacz [porady: Dodawanie diagramów klasy do projektu (Projektant klas)](../ide/how-to-add-class-diagrams-to-projects-class-designer.md).  
  
2.  W **przybornika**w obszarze **Projektant klas**, kliknij przycisk **dziedziczenia**.  
  
3.  Na diagramie klas Rysowanie linii dziedziczenia pomiędzy typami, które mają, zaczynając od:  
  
    -   Klasa pochodna do klasy podstawowej  
  
    -   Klasa implementująca jak zaimplementowany interfejs  
  
    -   Rozszerzanie interfejs do rozszerzonego interfejsu  
  
4.  Opcjonalnie Jeśli typ pochodny od typu ogólnego, kliknij przycisk linii dziedziczenia. W **właściwości** ustaw **argumentów typu** właściwości pasuje do typu, który ma obowiązywać dla typu ogólnego.  
  
    > [!NOTE]
    >  Jeśli nadrzędnej klasy abstrakcyjnej zawiera co najmniej jeden abstrakcyjny element członkowski, wszystkie abstrakcyjne elementy członkowskie są zaimplementowane jako dziedziczące klasy nieabstrakcyjnej.  
    >   
    >  Mimo że można Wizualizuj istniejące typy ogólne, nie można utworzyć nowych typów ogólnych. Nie można zmienić również parametry typu dla istniejących typów ogólnych.  
  
## <a name="see-also"></a>Zobacz też  
 [Dziedziczenie](/dotnet/csharp/programming-guide/classes-and-structs/inheritance)   
 [Podstawowe informacje o dziedziczeniu](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)   
 [Porady: wyświetlanie dziedziczenia pomiędzy typami (Projektant klas)](../ide/how-to-view-inheritance-between-types-class-designer.md)   
 [Klasy Visual C++ w Projektancie klas](../ide/visual-cpp-classes-in-class-designer.md)