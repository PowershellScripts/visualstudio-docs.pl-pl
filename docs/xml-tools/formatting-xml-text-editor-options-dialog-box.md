---
title: Formatowanie, XML, Edytor tekstu, okno dialogowe Opcje | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: bb539b3a-027c-4b2f-906e-403e0e22ba8d
caps.latest.revision: "2"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: c6b6a0cbfc0a82bbc827b0a994426ef7e87ced91
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="formatting-xml-text-editor-options-dialog-box"></a>Formatowanie, XML, Edytor tekstu, opcje — Okno dialogowe
To okno dialogowe służy do określenia ustawienia formatowania edytora XML. Dostęp można uzyskać **opcje** okno dialogowe z **narzędzia** menu.  
  
> [!NOTE]
>  Te ustawienia są dostępne po wybraniu **Edytor tekstu** folderu, **XML** folder, a następnie **formatowanie** opcję **opcje** okno dialogowe.  
  
## <a name="attributes"></a>Atrybuty  
 **Zachowaj ręczne formatowanie atrybutów**  
 Atrybuty nie są ponownie sformatowany. Domyślnie włączone.  
  
> [!NOTE]
>  W przypadku atrybutów w wielu wierszach, Edytor wcięcie każdego wiersza atrybutów, aby dopasować wcięcie elementu nadrzędnego.  
  
 **Dopasuj atrybutów na ich własnych wiersza**  
 Wyrównuje druga i kolejna atrybutów w pionie, tak aby dopasować wcięcia pierwszego atrybutu. Przykładem czy wyrównanie atrybutów jest następujący tekst XML.  
  
```  
<item id = "123-A"  
      name = "hammer"  
      price = "9.95">  
</item>  
```  
  
## <a name="auto-reformat"></a>Automatycznego ponownego formatowania  
 **Po wklejeniu ze Schowka**  
 Formatuje tekstu XML wklejonych ze Schowka.  
  
 **Po zakończeniu tagu końcowego**  
 Formatuje element po zakończeniu tagu końcowego.  
  
## <a name="mixed-content"></a>Zawartość mieszaną  
 **Zachowaj zawartość mieszaną domyślnie**  
 Określa, czy edytor formatuje zawartość mieszana. Domyślnie próbuje ponownie Formatuj zawartość mieszaną, z wyjątkiem przypadków, gdy zawartość znajduje się w edytorze `xml:space="preserve"` zakresu.  
  
 Jeśli element zawiera tekst i znacznik, zawartość są traktowane jako mieszanie zawartości. Oto przykład elementu z zawartością mieszaną.  
  
```  
<dir>c:\data\AlphaProject\  
  <file readOnly="false">test1.txt</file>  
  <file readOnly="false">test2.txt</file>  
</dir>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Właściwości dokumentu XML, okno właściwości](../xml-tools/xml-document-properties-properties-window.md)   
 [Składniki edytora XML](../xml-tools/xml-editor-components.md)