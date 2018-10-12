---
title: -Command (devenv.exe) | Dokumentacja firmy Microsoft
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
- Devenv, /command switch
- /command Devenv switch
ms.assetid: 13c20cd6-f09d-400a-8b7b-ecc266a32cef
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5f95d8758da77f1b720f0a1b6ca74f7ac753d805
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49254389"
---
# <a name="command-devenvexe"></a>/Command (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Wykonuje określone polecenie po uruchomieniu [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] zintegrowanego środowiska programistycznego (IDE).  
  
## <a name="syntax"></a>Składnia  
  
```  
devenv /command CommandName  
```  
  
## <a name="arguments"></a>Argumenty  
 `CommandName`  
 Wymagane. Pełna nazwa [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] polecenia lub jego alias, ujęte w podwójny cudzysłów. Aby uzyskać więcej informacji o syntaksie aliasów i poleceń, zobacz [polecenia programu Visual Studio](../../ide/reference/visual-studio-commands.md).  
  
## <a name="remarks"></a>Uwagi  
 Po zakończeniu uruchamiania, IDE wykonuje polecenie nazwane. Jeśli używasz tego przełącznika, IDE nie wyświetla [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] strony początkowej podczas uruchamiania.  
  
 Jeśli dodatek udostępnia polecenia, można użyć tego przełącznika, aby uruchomić dodatek z wiersza polecenia. Aby uzyskać więcej informacji, zobacz [instrukcje: kontrolki Add-Ins za pomocą Menedżera dodatków](http://msdn.microsoft.com/library/4f60444a-cb48-4cdb-8df4-941f6419aeeb).  
  
## <a name="example"></a>Przykład  
 W tym przykładzie uruchamia [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] i automatycznie uruchamia makro otwierania ulubionych plików.  
  
```  
devenv /command "Macros.MyMacros.Module1.OpenFavoriteFiles"  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



