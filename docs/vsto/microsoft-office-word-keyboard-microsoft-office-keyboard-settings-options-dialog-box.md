---
title: "Microsoft Office Word klawiatury, ustawienia klawiatury Microsoft Office, opcje ― Okno dialogowe | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- VS.ToolsOptionsPages.Microsoft_Office_Tools.Microsoft_Office_Word.Keyboard
- VS.ToolsOptionsPages.Microsoft_Office_Keyboard_Settings.Microsoft_Office_Word_Keyboard
- VST.WordOptions.KeyboardMappingScheme
dev_langs:
- VB
- CSharp
helpviewer_keywords: keyboard shortcuts, Office development in Visual Studio
ms.assetid: d98edaab-846a-4baa-b190-702b1134754c
caps.latest.revision: "18"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: bbce725246356086ac64b1810b80b91839caea3c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="microsoft-office-word-keyboard-microsoft-office-keyboard-settings-options-dialog-box"></a>Klawiatura Microsoft Office Word, ustawienia klawiatury Microsoft Office — Okno dialogowe
  Program Microsoft Word pakietu Office i programu Visual Studio zarówno obsługi klawiszy skrótów. Inne polecenia w programie Word i w programie Visual Studio może zastąpić tej samej kombinacji klawiszy skrótów. Gdy program Word jest otwarty w projektach na poziomie dokumentu w programie Visual Studio, tylko jedną aplikację naraz odbiera poleceń klawiszy skrótów. Domyślnie program Visual Studio odbiera wszystkie polecenia klawiszy skrótu, ale można wprowadzić ich odbierania, gdy dokument ma fokus, wybierając Word **schemat klawiatury dynamiczne**.  
  
 Jeśli używasz klawisz skrótu, który nie jest przypisany do polecenia w aplikacji, która obecnie obsługuje klawiszy skrótów klawisz skrótu są przekazywane do innych aplikacji.  
  
 Należy wybrać opcję będą obowiązywać dla projektów programu Word dopóki nie zostanie zmieniony. Zaznaczenie nie ma wpływu na projektów programu Microsoft Office Excel; należy zmiany dla programu Excel, korzystając z opcji Microsoft Office Excel klawiatury.  
  
## <a name="uielement-list"></a>Lista elementów UI  
 **Schemat klawiatury w usłudze Visual Studio**  
 Visual Studio odbiera wszystkich poleceń klawiszy skrótów, nawet jeśli dokument programu Word ma fokus. Na przykład jeśli naciśniesz klawisz funkcji F5, podczas gdy dokument ma fokus, Visual Studio rozpoczyna debugowanie rozwiązania.  
  
 **Schemat klawiatury dynamiczne**  
 Visual Studio odbiera poleceń klawiszy skrótów tylko wtedy, gdy fokus. Po aktywowaniu dokument programu Word, wyraz odbiera wszystkich poleceń klawiszy skrótów. Na przykład, jeśli naciśniesz klawisz funkcji F5, gdy fokus jest dokument programu Word, wyraz otwiera **Znajdź i Zamień** okno dialogowe z **przejdź do** kartę zaznaczone. Jeśli podczas, gdy fokus jest Visual Studio naciśnij klawisz F5, Visual Studio rozpoczyna debugowanie rozwiązania.  
  
## <a name="see-also"></a>Zobacz też  
 [Microsoft Office Excel klawiatury, ustawienia klawiatury Microsoft Office, opcje — Okno dialogowe](../vsto/microsoft-office-excel-keyboard-microsoft-office-keyboard-settings-options-dialog-box.md)  
  
  