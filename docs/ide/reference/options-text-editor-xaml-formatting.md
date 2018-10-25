---
title: Opcje, edytor tekstu, XAML, formatowanie
ms.date: 01/17/2017
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.XAML.Formatting.General
- VS.ToolsOptionsPages.Text_Editor.XAML.Miscellaneous
- VS.ToolsOptionsPages.Text_Editor.XAML.Formatting.Spacing
helpviewer_keywords:
- element spacing, XAML view settings
- attribute spacing, XAML view settings
- XAML view settings, auto-formatting events
- auto-formatting events, XAML view settings
- XAML view settings, tag wrapping
- XAML view settings, auto insert
- quotation mark style, XAML view settings
- XAML formatting, WPF Designer
- XAML view settings, Toolbox
- XAML view settings, element spacing
- default view, XAML view settings
- auto insert, XAML view settings
- XAML view settings, default view
- XAML view settings, quotation mark style
- tag wrapping, XAML view settings
- WPF Designer, XAML formatting
- XAML view settings, attribute spacing
ms.assetid: ad3820b1-0d94-4807-a74c-c3467ed973a2
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- uwp
ms.openlocfilehash: 272fb5368b73e483bb7d2f44c475d5e4e7bfdfcc
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49933576"
---
# <a name="options-text-editor-xaml-formatting"></a>Opcje, edytor tekstu, XAML, formatowanie
Użyj **formatowanie** stronę właściwości, aby określić, jak sformatowane elementów i atrybutów w dokumencie XAML. Aby otworzyć **opcje** okno dialogowe, kliknij przycisk **narzędzia** menu, a następnie kliknij przycisk **opcje**. Aby uzyskać dostęp do **formatowanie** właściwości rozwiń **edytora tekstów**, **XAML**, **formatowanie** węzła.

> [!NOTE]
> Okna dialogowe i polecenia menu mogą się różnić od tych opisanych w Pomocy, w zależności od ustawień aktywnych lub wydania. Aby zmienić swoje ustawienia, wybierz opcję **Import i eksport ustawień** na **narzędzia** menu. Aby uzyskać więcej informacji, zobacz [personalizowanie środowiska IDE programu Visual Studio](../../ide/personalizing-the-visual-studio-ide.md).


## <a name="auto-formatting-events"></a>Automatyczne formatowanie zdarzeń
 Automatyczne formatowanie może wystąpić, gdy dowolne z następujących zdarzeń wykryte.

-   Uzupełnianie tagu końcowego lub prostego.

-   Uzupełnianie tagu początkowego.

-   Wklejanie ze Schowka.

-   Formatowanie klawiaturowych.

Można określić, zdarzenia, które powodują automatyczne formatowanie.

|||
|-|-|
|**Po zakończeniu tagu końcowego lub prostego**|Automatyczne formatowanie występuje po zakończeniu wpisywania tagu końcowego lub prostego tagu. Prostych tagów nie ma atrybutów, na przykład `<Button />`.|
|**Po zakończeniu tagu początkowego**|Automatyczne formatowanie występuje po zakończeniu wpisywania tagu początkowego.|
|**Przy wklejaniu ze Schowka**|Automatyczne formatowanie występuje podczas wklejania XAML ze Schowka w widoku XAML.|

## <a name="quotation-mark-style"></a>Styl cudzysłowu
 To ustawienie wskazuje, czy wartości atrybutów są ujęte w pojedyncze lub podwójne znaki cudzysłowu. Użyj tego ustawienia, element formatujący automatycznie i automatycznego uzupełniania IntelliSense.

 Po ustawieniu tej opcji tylko atrybuty później dodane przy użyciu narzędzia Projektant lub ręcznie w widoku XAML dotyczy problem.

|||
|-|-|
|**Podwójny cudzysłów (")**|Wartości atrybutów są ujęte w cudzysłów.<br /><br /> `<Button Name="button1">Hello</Button>`|
|**Pojedynczy cudzysłów (')**|Wartości atrybutów są ujęte w apostrofy.<br /><br /> `<Button Name='button1'>Hello</Button>`|

## <a name="tag-wrapping"></a>Zawijanie tagów
 Można określić długość wiersza zawijanie tagów. Po włączeniu zawijanie tagów XAML, wszystkie dodane przy użyciu narzędzia Projektant zostanie zawinięta odpowiednio.

|||
|-|-|
|**Zawijaj tagi przekraczające określoną długość**|Określa, czy wiersze są opakowane w określonej przez długość wiersza **długość**.|
|**Długość**|Liczba znaków, które mogą zawierać wiersz. Jeśli to konieczne, niektóre linie XAML może przekraczać długości określonej linii.|

## <a name="attribute-spacing"></a>Odstępy między atrybutami
 To ustawienie służy do kontrolowania, jak atrybuty są rozmieszczone w dokumencie XAML

|||
|-|-|
|**Zachowaj tabulacji i spacje między atrybutami**|Nowe wiersze i spacje między atrybutami nie dotyczy automatyczne formatowanie.<br /><br /> `<Button Height="23"   Name="button1"`<br /><br /> `Width="75">Hello</Button>`|
|**Wstaw odstęp między atrybutami**|Atrybuty zajmują jeden wiersz z jednego miejsca oddzielenie sąsiadujących atrybutów. Ustawienia zawijania tag są stosowane.<br /><br /> `<Button Height="23" Name="button1" Width="75">Hello</Button>`|
|**Umieść każdy atrybut w osobnym wierszu**|Każdy atrybut zajmuje swój własny wiersz. Jest to przydatne, jeśli podano wiele atrybutów.<br /><br /> `<Button`<br /><br /> `Height="23"`<br /><br /> `Name="button1"`<br /><br /> `Width="75">Hello</Button>`|
|**Pozycja pierwszego atrybutu w tym samym wierszu co tag początkowy**|Po zaznaczeniu tej opcji, w tym samym wierszu co tag początkowy element pojawi się pierwszy atrybut.<br /><br /> `<Button Height="23"`<br /><br /> `Name="button1"`<br /><br /> `Width="75">Hello</Button>`|

## <a name="element-spacing"></a>Odstępy między elementami
 Użyj tego ustawienia, aby kontrolować sposób rozmieszczenia elementów w dokumencie XAML


| | |
| - | - |
| **Zachowaj nowe wiersze w zawartości** | Puste wiersze w zawartości elementu nie są usuwane.<br /><br /> `<Grid>`<br /><br /> ``<br /><br /> ``<br /><br /> `<Button Name="button1">Hello</Button>`<br /><br /> ``<br /><br /> `</Grid>\` |
| **Zwiń wiele puste wiersze w zawartości w jeden wiersz** | Puste wiersze w zawartości elementu są zwinięte do pojedynczego wiersza.<br /><br /> `<Grid>`<br /><br /> ``<br /><br /> `<Button Name="button1">Hello</Button>`<br /><br /> ``<br /><br /> `</Grid>` |
| **Usuń puste wiersze w zawartości** | Wszystkie puste wiersze w zawartości elementu są usuwane.<br /><br /> `<Grid>`<br /><br /> `<Button Name="button1">Hello</Button>`<br /><br /> `</Grid>` |

## <a name="miscellaneous-section-auto-insert"></a>Różne części, automatyczne wstawianie
 To ustawienie służy do kontrolowania, kiedy tagów i cudzysłowy są generowane automatycznie.

|||
|-|-|
|**Taga zamykającego**|Określa, czy tag zamykający elementu jest generowana automatycznie, gdy zamkniesz otwierający tag o rozmiarze większym niż znak większości (>).|
|**Cudzysłowy atrybutu**|Określa, czy otaczającej cudzysłowy są generowane w przypadku wybrania wartości atrybutu z listy rozwijanej uzupełniania instrukcji.|
|**Zamykające nawiasy klamrowe dla wyrażeń MarkupExtension**|Określa, czy jako rozszerzenie znacznika zamykającego nawiasu klamrowego (}) jest generowany automatycznie po wpisaniu otwierający nawias klamrowy znak ({}).|
|**Przecinków do oddzielenia parametry wyrażeń MarkupExtension**|Określa, czy przecinkami są generowane, gdy więcej niż jeden parametr jest typu rozszerzenia znaczników.|

## <a name="see-also"></a>Zobacz także

- [XAML w WPF](/dotnet/framework/wpf/advanced/xaml-in-wpf)
