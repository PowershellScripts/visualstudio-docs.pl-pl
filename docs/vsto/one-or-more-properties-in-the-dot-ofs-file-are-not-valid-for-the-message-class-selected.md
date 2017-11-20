---
title: "Co najmniej jednej właściwości w pliku .ofs nie są prawidłowe dla klasy wybranego komunikatu | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: VSTO.NewFormRegionWizard.OFSPropertyError
dev_langs:
- VB
- CSharp
ms.assetid: ca9e2ec1-df96-45ca-9611-cec47edfe1e4
caps.latest.revision: "8"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: ddaad272326c4cd77e0e54bd7216974181c77a72
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="one-or-more-properties-in-the-ofs-file-are-not-valid-for-the-message-class-selected"></a>Jedna właściwość lub więcej w pliku .ofs jest nieprawidłowa dla klasy wybranego komunikatu
  Ten błąd pojawia się po zaimportowaniu regionów formularzy zaprojektowanych w programie Outlook, ale co najmniej jedno pole na region formularza nie są zgodne z klas wiadomości, które wybiera się na ostatniej stronie **nowego regionu formularza** kreatora.  
  
 Na przykład możesz wybrać pozycję **zadań (IPM. Zadanie)** na ostatniej stronie **nowego regionu formularza** kreatora. Jeśli regionu formularza zawiera **adres firmy** pola, zostanie wyświetlony ten błąd, ponieważ zadanie nie ma adres firmy. W związku z tym **adres firmy** pola nie jest zgodny z IPM. Klasy wiadomości zadań.  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Na ostatniej stronie **nowego regionu formularza** kreatora wybierz klasy wiadomości, która jest zgodna z pola regionu formularza.  
  
-   W narzędziu Projektant dla formularzy w programie Outlook, usuń pola, które nie są zgodne z klas wiadomości, które mają być wybierz na ostatniej stronie **nowego regionu formularza** kreatora.  
  
## <a name="see-also"></a>Zobacz też  
 [Wskazówki: Importowanie regionów formularzy zaprojektowanych w programie Outlook](../vsto/walkthrough-importing-a-form-region-that-is-designed-in-outlook.md)  
  
  