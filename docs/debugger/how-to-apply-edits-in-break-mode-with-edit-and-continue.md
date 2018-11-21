---
title: 'Porady: stosowanie edycji w trybie przerwania za pomocą edycji i kontynuowania | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.variables.failededit
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [Visual Basic], applying edits in break mode
- break mode, applying code changes
- Edit and Continue, applying edits in break mode
- editing, break mode
- coding, editing in break mode
- code, editing in break mode
ms.assetid: 1eef7498-6a1f-4fba-8146-510adc6375c9
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f45b2a64e7602d038a12f436019a8f99e352aa26
ms.sourcegitcommit: a7de99f36e9ead7ea9e9bac23c88d05ddfc38b00
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/20/2018
ms.locfileid: "52257078"
---
# <a name="how-to-apply-edits-in-break-mode-with-edit-and-continue-visual-basic"></a>Porady: stosowanie edycji w trybie przerwania za pomocą Edytuj i Kontynuuj (Visual Basic)
Edytuj i Kontynuuj umożliwia edytowanie kodu w trybie przerwania, a następnie kontynuuj bez zatrzymywania i ponownego uruchamiania wykonywania.  
  
Ograniczenia dotyczące używania Edytuj i Kontynuuj podczas debugowania, zobacz [obsługiwane zmiany kodu (C# i Visual Basic](../debugger/supported-code-changes-csharp.md)]
  
### <a name="to-edit-code-in-break-mode"></a>Do edycji kodu w trybie przerwania  
  
1.  Tryb przerwania, wykonując jedną z następujących czynności:  
  
    -   Ustaw punkt przerwania w kodzie, a następnie wybierz **Rozpocznij debugowanie** z **debugowania** menu i zaczekaj, aż ją w dotarciu do punktu przerwania.  
  
         —lub—  
  
    -   Rozpocznij debugowanie, a następnie wybierz **Przerwij wszystko** z **debugowania** menu.  
  
         —lub—  
  
    -   Gdy wystąpi wyjątek, wybierz pozycję **Włącz edytowanie** na **Asystenta wyjątków**.  
  
2.  Wprowadź wszelkie zmiany kodu żądaną i objęty pomocą techniczną.  
  
     Aby uzyskać więcej informacji, zobacz [obsługiwane zmiany kodu (C# i Visual Basic](../debugger/supported-code-changes-csharp.md).  
  
    > [!NOTE]
    >  Jeśli spróbujesz kodu, zmiany, które nie jest dozwolona przez Edytuj i Kontynuuj, zmiany będą podkreślone purpurowa linia falista i zadania pojawi się na liście zadań. Nie można kontynuować wykonywania kodu, chyba że można cofnąć zmiany kodu niedozwolony.  
  
3.  Na **debugowania** menu, kliknij przycisk **Kontynuuj** można wznowić wykonywania.  
  
     Kod wykonuje teraz stosowane edycji włączone do projektu.  
  
## <a name="see-also"></a>Zobacz też  
 [Obsługiwane zmiany kodu (C# i Visual Basic](../debugger/supported-code-changes-csharp.md)   
 [Edytuj i kontynuuj (Visual Basic)](../debugger/edit-and-continue-visual-basic.md)