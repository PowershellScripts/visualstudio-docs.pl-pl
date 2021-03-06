---
title: Formatowanie, XML, Edytor tekstu, okno dialogowe Opcje | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: bb539b3a-027c-4b2f-906e-403e0e22ba8d
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5c8379393dd5327359789f8621cf67ed55e89209
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49256675"
---
# <a name="formatting-xml-text-editor-options-dialog-box"></a>Formatowanie, XML, Edytor tekstu, Opcje, okno dialogowe
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
To okno dialogowe umożliwia określenie ustawień formatowania edytora XML. Możesz uzyskać dostęp **opcje** okno dialogowe z **narzędzia** menu.  
  
> [!NOTE]
>  Te ustawienia są dostępne po wybraniu **edytora tekstów** folderze **XML** folder, a następnie **formatowanie** opcję **opcje** okno dialogowe.  
  
## <a name="attributes"></a>Atrybuty  
 **Zachowaj ręczne formatowanie atrybutów**  
 Atrybuty nie są ponownie sformatowany. Domyślnie włączone.  
  
> [!NOTE]
>  W przypadku atrybutów w wielu wierszach, Edytor wcięcie każdego wiersza atrybutów, aby dopasować wcięcie elementu nadrzędnego.  
  
 **Wyrównaj atrybuty na własnej linii**  
 Wyrównuje drugim i kolejnych atrybutów w pionie, aby dopasować wcięcie pierwszego atrybutu. Następujący tekst XML jest przykładem sposobu atrybuty byłaby wyrównana.  
  
```  
<item id = "123-A"  
      name = "hammer"  
      price = "9.95">  
</item>  
```  
  
## <a name="auto-reformat"></a>Automatycznie Formatuj ponownie  
 **Przy wklejaniu ze Schowka**  
 Formatuje tekst XML wklejonych ze Schowka.  
  
 **Po zakończeniu tagu końcowego**  
 Formatuje element, po zakończeniu tagu końcowego.  
  
## <a name="mixed-content"></a>Zawartość mieszana  
 **Zachowaj zawartość mieszana domyślnie**  
 Określa, czy edytor formatuje zawartość mieszana. Domyślnie, próbuje ponownie Formatuj zawartość mieszaną, z wyjątkiem sytuacji, gdy zawartość znajduje się w edytorze `xml:space="preserve"` zakresu.  
  
 Jeśli element zawiera tekst i znacznik, uznaje się zawartość mieszaną zawartość i być. Oto przykład elementu z zawartością mieszane.  
  
```  
<dir>c:\data\AlphaProject\  
  <file readOnly="false">test1.txt</file>  
  <file readOnly="false">test2.txt</file>  
</dir>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Właściwości dokumentu XML, okno właściwości](../xml-tools/xml-document-properties-properties-window.md)   
 [Składniki edytora XML](../xml-tools/xml-editor-components.md)



