---
title: -ResetSettings (devenv.exe) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Devenv, /ResetSettings switch
- ResetSettings switch
- /ResetSettings Devenv switch
ms.assetid: 1d41021c-6f58-4bd5-b122-d1c995812192
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 276205ae2aab3c38ceb3d4f1419e0bac13ae626c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49273497"
---
# <a name="resetsettings-devenvexe"></a>/ResetSettings (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Przywraca [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] ustawienia domyślne i automatycznie uruchamia [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE. Opcjonalnie resetuje ustawienia do określonego pliku .vssettings.  
  
 Ustawienia domyślne są określane przez profil który został wybrany, gdy [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] najpierw została uruchomiona.  
  
## <a name="syntax"></a>Składnia  
  
```  
Devenv /ResetSettings SettingsFile  
```  
  
## <a name="arguments"></a>Argumenty  
 `SettingsFile`  
 Pełna ścieżka i nazwa pliku .vssettings do zastosowania do [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
 Aby przywrócić profil ogólne ustawienia projektowe, użyj `General`.  
  
## <a name="remarks"></a>Uwagi  
 Jeśli nie `SettingsFile` jest określona, zostanie wyświetlony monit wybór domyślnej kolekcji ustawień przy następnym uruchomieniu [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
## <a name="example"></a>Przykład  
 Następujący wiersz polecenia powoduje zastosowanie ustawień przechowywanych w pliku `MySettings.vssettings`.  
  
```  
Devenv.exe /ResetSettings "C:\My Files\MySettings.vssettings"  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Dostosowywanie ustawień środowiska deweloperskiego w programie Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)



