---
title: -Tryb awaryjny (devenv.exe) | Dokumentacja firmy Microsoft
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
- /SafeMode Devenv switch
- Devenv, /SafeMode switch
- SafeMode switch
ms.assetid: b191f6a5-8f12-47ec-bcc7-b68149a22aa8
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b785a3e43726522f6e6cc6ce99dec4bf3815c81d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49230083"
---
# <a name="safemode-devenvexe"></a>/SafeMode (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Uruchamia [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] w trybie awaryjnym, ładowanie tylko środowisko domyślne i usługi.  
  
## <a name="syntax"></a>Składnia  
  
```  
devenv /SafeMode   
```  
  
## <a name="remarks"></a>Uwagi  
 Ten przełącznik uniemożliwia załadowanie, kiedy wszystkich innych pakietów VSPackage [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] rozpoczyna się, co pozwala na zapewnienie stabilne wykonywania.  
  
## <a name="description"></a>Opis  
 Poniższy przykład rozpoczyna się [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] w trybie awaryjnym.  
  
## <a name="code"></a>Kod  
  
```  
Devenv.exe /SafeMode  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)



