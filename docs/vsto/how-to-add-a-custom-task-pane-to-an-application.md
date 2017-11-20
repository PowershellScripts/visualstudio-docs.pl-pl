---
title: "Porady: Dodawanie niestandardowego okienka zadań do aplikacji | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- task panes [Office development in Visual Studio], adding to application
- custom task panes [Office development in Visual Studio], adding to application
ms.assetid: 67b4ed5b-d77e-4630-b851-34bb25bdc9b3
caps.latest.revision: "28"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 1a39267da04be68793a2236250e5ed10efb01afd
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-add-a-custom-task-pane-to-an-application"></a>Porady: dodawanie niestandardowego okienka zadań do aplikacji
  Możesz dodać niestandardowego okienka zadań do aplikacji wymienionych powyżej przy użyciu dodatku VSTO. Aby uzyskać więcej informacji, zobacz [niestandardowego okienka zadań](../vsto/custom-task-panes.md).  
  
 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]  
  
> [!NOTE]  
>  Na komputerze w poniższych instrukcjach mogą być wyświetlane inne nazwy i lokalizacje niektórych elementów interfejsu użytkownika programu Visual Studio. Te elementy są określane przez numer wersji Visual Studio oraz twoje ustawienia. Aby uzyskać więcej informacji, zobacz [personalizowanie środowiska IDE programu Visual Studio](../ide/personalizing-the-visual-studio-ide.md).  
  
## <a name="adding-a-custom-task-pane-to-an-application"></a>Dodawanie niestandardowego okienka zadań do aplikacji  
  
#### <a name="to-add-a-custom-task-pane-to-an-application"></a>Aby dodać niestandardowego okienka zadań do aplikacji  
  
1.  Otwórz lub Utwórz projekt dodatku VSTO dla jednej z aplikacji wymienionych powyżej. Aby uzyskać więcej informacji, zobacz [porady: tworzenie projektów Office w Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md).  
  
2.  Na **projektu** menu, kliknij przycisk **Dodaj kontrolkę użytkownika**.  
  
3.  W **Dodaj nowy element** okno dialogowe Zmień nazwę nowego formantu użytkownika do **MyUserControl**, a następnie kliknij przycisk **Dodaj**.  
  
     Kontrola użytkownika zostanie otwarty w projektancie.  
  
4.  Dodaj formanty formularzy systemu Windows co najmniej jeden z **przybornika** do kontrolki użytkownika.  
  
5.  Otwórz **ThisAddIn.cs** lub **ThisAddIn.vb** pliku kodu.  
  
6.  Dodaj następujący kod do `ThisAddIn` klasy. Ten kod deklaruje wystąpienia `MyUserControl` i <xref:Microsoft.Office.Tools.CustomTaskPane> jako elementy członkowskie `ThisAddIn` klasy.  
  
     [!code-vb[Trin_TaskPaneBasic#1](../vsto/codesnippet/VisualBasic/Trin_TaskPaneBasic/ThisAddIn.vb#1)]
     [!code-csharp[Trin_TaskPaneBasic#1](../vsto/codesnippet/CSharp/Trin_TaskPaneBasic/ThisAddIn.cs#1)]  
  
7.  Dodaj następujący kod do `ThisAddIn_Startup` obsługi zdarzeń. Ten kod tworzy nową <xref:Microsoft.Office.Tools.CustomTaskPane> przez dodanie `MyUserControl` do obiektu `CustomTaskPanes` kolekcji. Kod są również wyświetlane w okienku zadań.  
  
     [!code-vb[Trin_TaskPaneBasic#2](../vsto/codesnippet/VisualBasic/Trin_TaskPaneBasic/ThisAddIn.vb#2)]
     [!code-csharp[Trin_TaskPaneBasic#2](../vsto/codesnippet/CSharp/Trin_TaskPaneBasic/ThisAddIn.cs#2)]  
  
    > [!NOTE]  
    >  Ten kod kojarzy niestandardowego okienka zadań z aktywnego okna aplikacji. Dla pewnych aplikacji możesz modyfikować ten kod, aby zapewnić z innymi dokumenty lub elementy w aplikacji okienka zadań. Aby uzyskać więcej informacji, zobacz [niestandardowego okienka zadań](../vsto/custom-task-panes.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Dostosowywanie interfejsu użytkownika pakietu Office](../vsto/office-ui-customization.md)   
 [Niestandardowe okienka zadań](../vsto/custom-task-panes.md)   
 [Wskazówki: Automatyzacja aplikacji z niestandardowego okienka zadań](../vsto/walkthrough-automating-an-application-from-a-custom-task-pane.md)  
  
  