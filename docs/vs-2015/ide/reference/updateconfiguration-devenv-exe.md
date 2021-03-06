---
title: -Updateconfiguration (devenv.exe) | Dokumentacja firmy Microsoft
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
- /updateconfiguration Devenv switch
- Devenv, /updateconfiguration switch
- updateconfiguration Devenv switch
ms.assetid: 9a1084cc-8b68-4ccc-aaea-f95939164338
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: ed69bf8c54d3b428907b4dbe0636f2966254de75
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49253639"
---
# <a name="updateconfiguration-devenvexe"></a>/ Updateconfiguration (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Powiadamia [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] do scalenia [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] żadnych zmian w pamięci podręcznej pakietów w systemie i wyboru MEF.  
  
## <a name="syntax"></a>Składnia  
  
```  
devenv /updateconfiguration  
```  
  
## <a name="remarks"></a>Uwagi  
 [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] uruchamia to polecenie automatycznie po zainstalowaniu pakietu VSIX. Należy uruchomić `devenv.exe /updateconfiguration` po poprawianie plików tak, aby [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] aktualizuje pamięć podręczna MEF. Dzięki temu można ocenić, czy rozwiązanie problemu jest odpowiednia.  
  
## <a name="example"></a>Przykład  
 Poniższe przyczyny wiersza polecenia [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] do scalenia [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] żadnych zmian w pamięci podręcznej pakietów w systemie i wyboru MEF.  
  
```  
Devenv.exe /updateconfiguration  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Dostosowywanie ustawień środowiska deweloperskiego w programie Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)



