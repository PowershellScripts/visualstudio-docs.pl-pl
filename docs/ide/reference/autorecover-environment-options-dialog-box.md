---
title: AutoRecover, środowisko, opcje — Okno dialogowe
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.DialogAutoRestore
- VS.ToolsOptionsPages.Environment.AutoRecover
- VS.ToolsOptionsPages.Environment.Auto_Save_and_Restore
helpviewer_keywords:
- files, recovering
- AutoRecover page
- saving files, automatically
- files, saving automatically
ms.assetid: 397e5e44-4bbe-4289-94d1-642b466c9111
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ed5ad6259ede32304cfe15ef4e79c6b3e56dbd9d
ms.sourcegitcommit: 1abb9cf4c3ccb90e3481ea8079272c98aad12875
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/26/2018
ms.locfileid: "50143310"
---
# <a name="autorecover-environment-options-dialog-box"></a>Okno dialogowe AutoRecover, środowisko, opcje

Użyj tej strony w **opcje** okno dialogowe, aby określić, czy do automatycznego wykonywania kopii zapasowej plików, czy nie. Ta strona umożliwia również określić, czy przywrócić zmodyfikowane pliki, jeśli nieoczekiwane zamknięcie programu Visual Studio.

Dostęp do tego okna dialogowego wybierając **narzędzia** menu, wybierając **opcje**, a następnie wybierając **środowiska** > **Autoodzyskiwania**. Jeśli ta strona nie jest wyświetlana na liście, wybierz **Pokaż wszystkie ustawienia** w **opcje** okno dialogowe.

> [!NOTE]
> Okna dialogowe i polecenia menu mogą się różnić od tych opisanych w Pomocy, w zależności od ustawień aktywnych lub wydania. Aby zmienić swoje ustawienia, wybierz opcję **Import i eksport ustawień** na **narzędzia** menu. Aby uzyskać więcej informacji, zobacz [personalizowanie środowiska IDE programu Visual Studio](../../ide/personalizing-the-visual-studio-ide.md).

**Zapisuj informacje Autoodzyskiwania co minut [n]**

Użyj tej opcji, aby dostosować, jak często automatycznie zapisaniu pliku w edytorze. Wcześniej zapisanych plików, kopia pliku jest zapisywana w *%USERPROFILE%\Documents\Visual Studio \<wersji > pliki \Backup\\<projectname>*. Jeśli plik jest nowy, a nie zapisano go, plik jest automatycznie zapisany przy użyciu nazwy losowo wygenerowany plik.

**Zachowaj informacje automatycznego odzyskiwania dni [n]**

Użyj tej opcji, aby określić, jak długo Visual Studio przechowuje pliki utworzone dla Autoodzyskiwania.

## <a name="see-also"></a>Zobacz także

- [Opcje, okno dialogowe](../../ide/reference/options-dialog-box-visual-studio.md)