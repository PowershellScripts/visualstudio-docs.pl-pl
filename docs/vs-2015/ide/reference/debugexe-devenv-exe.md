---
title: -DebugExe (devenv.exe) | Dokumentacja firmy Microsoft
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
- Devenv, /DebugExe switch
- DebugExe switch
- /DebugExe [devenv.exe]
ms.assetid: cd700006-1648-418f-924b-4b1e5c1412ab
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 56ff98aa40e122b5067bd17d72334daf93164fe2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49262655"
---
# <a name="debugexe-devenvexe"></a>/DebugExe (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Otwiera określony plik wykonywalny do zdebugowania.  
  
## <a name="syntax"></a>Składnia  
  
```  
Devenv /debugexe ExecutableFile  
```  
  
## <a name="arguments"></a>Argumenty  
 `ExecutableFile`  
 Wymagane. Ścieżka i nazwa pliku .exe.  
  
 Jeśli plik .exe nie zostanie znaleziony lub nie istnieje, jest wyświetlana nie ostrzeżenia lub błędu i [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] uruchamia się normalnie.  
  
## <a name="remarks"></a>Uwagi  
 Wszystkie ciągi zgodnie z `ExecutableFile` parametru są przekazywane do tego pliku jako argumenty.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie otwierany plik `MyApplication.exe` do debugowania.  
  
```  
Devenv.exe /debugexe MyApplication.exe  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)



