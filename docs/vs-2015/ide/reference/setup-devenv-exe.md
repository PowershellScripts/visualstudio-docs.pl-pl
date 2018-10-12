---
title: -Setup (devenv.exe) | Dokumentacja firmy Microsoft
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
- setup Devenv switch
- /setup Devenv switch
- Devenv, /setup switch
ms.assetid: 87608b7f-a156-400c-80f5-fc823f843e61
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f57de02f0d46a14574ef3f34d47f2f5e4018096b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49230624"
---
# <a name="setup-devenvexe"></a>/Setup (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Wymusza [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] do scalenia metadanych zasobów, które opisują, menu, paski narzędzi i grup poleceń, ze wszystkich dostępnych pakietów VSPackage.  
  
## <a name="syntax"></a>Składnia  
  
```  
devenv /setup  
```  
  
## <a name="remarks"></a>Uwagi  
 Ten przełącznik nie przyjmuje żadnych argumentów. `devenv /setup` Polecenia jest zazwyczaj podawana jako ostatni krok w procesie instalacji programu. Korzystanie z `/setup` przełącznika nie można uruchomić [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
 Należy uruchomić `devenv` jako administrator, aby można było używać [/Setup (devenv.exe)](../../ide/reference/setup-devenv-exe.md) i [/installvstemplates (devenv.exe)](../../ide/reference/installvstemplates-devenv-exe.md) przełączników.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie przedstawiono ostatni krok w instalacji wersji [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] zawierającej pakietów VSPackage.  
  
```  
devenv /setup  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)



