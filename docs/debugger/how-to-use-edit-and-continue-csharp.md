---
title: 'Porady: używanie funkcji Edytuj i Kontynuuj (C#) | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 10/04/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [C#], about Edit and Continue
ms.assetid: 40e136d8-a08c-43bd-b313-fb821c55eb3c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 41e97f488344e3d34ce326a3d35880d94da4ad9a
ms.sourcegitcommit: c5e72875206b8c5737c29d5b1ec7b86eec747303
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/17/2018
ms.locfileid: "49382808"
---
# <a name="how-to-use-edit-and-continue-c"></a>Porady: korzystanie z opcji edytuj i kontynuuj (C#)
Z funkcją Edytuj i Kontynuuj możesz wprowadzić i Zastosuj zmiany do kodu w trybie przerwania podczas debugowania, bez konieczności zatrzymywania i uruchamiania sesji debugowania.  

Edytuj i Kontynuuj dla języka C# odbywa się automatycznie po wprowadzeniu zmian w kodzie w trybie przerwania, następnie Kontynuuj debugowanie przy użyciu **Kontynuuj**, **kroku**, lub **Ustaw następną instrukcję**, lub Oceń funkcję w oknie debugera.  

Aby uzyskać więcej informacji, zobacz [Edytuj i Kontynuuj (Visual C#)](../debugger/edit-and-continue-visual-csharp.md).

>[!NOTE]
>Edytuj i Kontynuuj nie jest obsługiwane dla zoptymalizowane pod kątem, mieszany, lub kodu integracji środowiska uruchomieniowego (języka wspólnego CLR) wspólnego języka programu SQL Server. Aby uzyskać informacji na temat innych nieobsługiwanych scenariuszy, zobacz [obsługiwane zmiany kodu (C# i Visual Basic)](../debugger/supported-code-changes-csharp.md). Jeśli zostanie podjęta próba Edytuj i Kontynuuj przy użyciu jednego z tych scenariuszy, pojawi się komunikat informujący, że Edytuj i Kontynuuj nie jest obsługiwany.  
  
**Aby włączyć lub wyłączyć Edytuj i Kontynuuj:**  
   
1. Jeśli pracujesz w sesji debugowania, Zatrzymaj debugowanie (**debugowania** > **Zatrzymaj debugowanie** lub **Shift**+**F5**) .
   
1. W **narzędzia** > **opcje** (lub **debugowania** > **opcje**) > **debugowania**  >  **Ogólne**, zaznacz lub wyczyść **Włącz edytowanie i kontynuowanie** pole wyboru.  
  
Ustawienie zostanie uwzględnione po ponownym uruchomieniu lub uruchom ponownie sesję debugowania.  

**Aby użyć polecenia Edytuj i Kontynuuj:**  
   
1. Podczas debugowania w trybie przerwy wprowadź zmiany do kodu źródłowego.  
   
1. Z **debugowania** menu, kliknij przycisk **Kontynuuj**, **kroku**, lub **Ustaw następną instrukcję**, lub oceń funkcję w oknie debugera.  
   
   Debugowanie nadal stanowi nowy kod skompilowany. 

Niektóre rodzaje zmian w kodzie nie są obsługiwane przez Edytuj i Kontynuuj. Aby uzyskać więcej informacji, zobacz [obsługiwane zmiany kodu (C# i Visual Basic)](../debugger/supported-code-changes-csharp.md).   
