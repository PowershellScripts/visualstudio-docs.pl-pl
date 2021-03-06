---
title: Dodaj XML schematu zestaw wyszukiwania wynik węzły do obszaru roboczego
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: ff33b3cc-4db9-4b4e-9378-b45ed5999b18
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 04e74057bd059c82010678b7de571ff180e7fbfe
ms.sourcegitcommit: 58052c29fc61c9a1ca55a64a63a7fdcde34668a4
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34751913"
---
# <a name="how-to-add-schema-set-search-result-nodes-to-the-workspace"></a>Porady: Dodawanie węzłów wynik wyszukiwania zestawu schematu do obszaru roboczego

W tym temacie wyjaśniono, jak dodać węzłów, które są wyróżnione **Eksploratora schematu XML** wyniku wyszukiwanie słów kluczowych w obszarze roboczym.

> [!NOTE]
> Tylko węzły globalnego mogą być dodawane do [obszaru roboczego](../xml-tools/xml-schema-designer-workspace.md).


 W tym przykładzie użyto przykładowej [schematu zamówienia zakupu](../xml-tools/sample-xsd-file-purchase-order-schema.md).

## <a name="to-add-schema-set-result-nodes"></a>Aby dodać węzły wynik zestawu schematu

1.  Postępuj zgodnie z instrukcjami [porady: tworzenie i edytowanie pliku schematu XSD](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).

2.  W polu tekstowym wyszukiwania wpisz "purchaseOrder" [XML Explorer](../xml-tools/xml-schema-explorer.md) narzędzi i kliknij przycisk wyszukiwania.

     ![Wyszukiwanie słów kluczowych Eksploratora schematu XML](../xml-tools/media/schemaexplorersearch.gif)

     Wyniki wyszukiwania są wyróżnione **Eksploratora schematu XML** i oznaczone przez znaczniki na pionowy pasek przewijania.

3.  Wyniki wyszukiwania można dodać do obszaru roboczego, klikając **Dodaj wyróżnione węzły do obszaru roboczego** przycisk w okienku podsumowania wyników.

     ![Wynik wyszukiwania Eksploratora schematu XML](../xml-tools/media/schemaexplorersearchresult.gif)

     `purchaseOrder` Węzła i `PurchaseOrderType` węźle są wyświetlane obok siebie na powierzchni projektu [widok wykresu](../xml-tools/graph-view.md). Ponieważ dwa węzły są powiązane ( `purchaseOrder` element jest `PurchaseOrderType` typu), Strzałka jest rysowany między nimi.