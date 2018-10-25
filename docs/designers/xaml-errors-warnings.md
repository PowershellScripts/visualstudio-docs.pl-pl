---
title: XAML błędy i ostrzeżenia
ms.date: 03/06/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: 34eac8a0-7ec5-4c40-b97a-0126ed367931
author: karann-msft
ms.author: karann
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 09251f13cafa320e2736e9c61135283bb9e9739d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49844188"
---
# <a name="xaml-errors-and-warnings"></a>Błędy i ostrzeżenia XAML

Podczas tworzenia zawartości XAML, program Visual Studio analizuje kod podczas wpisywania. Fala pojawi się w wierszu kodu, gdy zostanie wykryty błąd. Kursor wężyk daje więcej informacji na temat błędu lub ostrzeżenia. Niektóre błędy i ostrzeżenia żarówki szybka akcja zostanie wyświetlony, przy użyciu **Ctrl**+**.** skrót klawiaturowy Wyświetla opcje, aby rozwiązać ten problem.

## <a name="error-types"></a>Typy błędów

W tle wielu narzędzi do analizowania XAML równolegle. Błędy XAML są podzielone na jeden z trzech następujących typów, oparte na narzędziu, że wykryto błąd:

|**Błąd wykryte przez**|**Błąd formatu kodu**|
| - |-----------------|
|Usługa języka XAML (Edytor XAML)|XLSxxxx|
|XAML Designer|XDGxxxx|
|XAML Edytuj i Kontynuuj|XECxxxx|

> [!Note]
> Nie wszystkie błędy i ostrzeżenia mają odpowiedni kod. Takie błędy są zazwyczaj błędy projektanta XAML.


## <a name="suppress-xaml-designer-errors"></a>Pomiń błędy projektanta XAML

Otwórz **opcje** okna dialogowego wybierając **Narzędzia > Opcje**, a następnie wybierz pozycję **Edytor tekstu > XAML > różne**.

Usuń zaznaczenie pola wyboru **Pokaż błędy wykryte przez projektanta XAML** pole wyboru.

![Pomiń błędy projektanta XAML](../designers/media/suppress_xaml_designer_errors.png)


