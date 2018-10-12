---
title: Import i eksport ustawień polecenie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- Tools.ImportandExportSettings
helpviewer_keywords:
- Tools.ImportandExportSettings
- Import and Export Settings command
ms.assetid: 94a06468-a44d-403d-a931-77bbc9d06e56
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 2556b814059a80f2b93d0220de27cdbd8c051ea9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49305568"
---
# <a name="import-and-export-settings-command"></a>Import i eksport ustawień — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Importuje, eksportuje lub resetuje [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] ustawienia.  
  
## <a name="syntax"></a>Składnia  
  
```  
Tools.ImportandExportSettings [/export:filename | /import:filename | /reset]  
```  
  
## <a name="switches"></a>Przełączniki  
 / export:`filename`  
 Opcjonalna. Eksportuje bieżące ustawienia do określonego pliku.  
  
 Import:`filename`  
 Opcjonalna. Importuje ustawienia w określonym pliku.  
  
 / Reset  
 Opcjonalna. Przywraca bieżące ustawienia.  
  
## <a name="remarks"></a>Uwagi  
 Uruchomienie tego polecenia, na których nie zmienia otwiera **Import i eksport ustawień** kreatora. Aby uzyskać więcej informacji, zobacz [porady: ustawienia udziału między komputerami lub wersjami programu Visual Studio](http://msdn.microsoft.com/en-us/1131fb10-35c1-42da-9cd8-91aa3235b882).  
  
## <a name="example"></a>Przykład  
 Następujące polecenie eksportuje bieżące ustawienia do pliku `MyFile.vssettings`.  
  
```  
Tools.ImportandExportSettings /export:"c:\Files\MyFile.vssettings"  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Dostosowywanie ustawień środowiska deweloperskiego w programie Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)



