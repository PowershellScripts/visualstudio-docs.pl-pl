---
title: Moduł wyliczający kod stanu katalogu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- directory status code enumerator
- source control plug-ins, directory status enumeration
ms.assetid: 616026b5-f529-40ef-90c1-1836e116d797
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 178d208b944cd52c641d60be7e0004c359896680
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49264078"
---
# <a name="directory-status-code-enumerator"></a>Moduł wyliczający kod stanu katalogu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`SccDirStatus` Modułu wyliczającego zawiera nazwanych stałych, określające stan katalogu w systemie kontroli źródła. To wyliczenie jest używane przez [SccDirQueryInfo](../extensibility/sccdirqueryinfo-function.md). To została wprowadzona w wersji 1.2 API wtyczki kontroli źródła.  
  
## <a name="syntax"></a>Składnia  
  
```  
enum SccDirStatus {  
   SCC_DIRSTATUS_INVALID       = -1L,  
   SCC_DIRSTATUS_NOTCONTROLLED = 0x0000L,  
   SCC_DIRSTATUS_CONTROLLED    = 0x0001L,  
   SCC_DIRSTATUS_EMPTYPROJ     = 0x0002L  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 SCC_DIRSTATUS_INVALID  
 Nie można uzyskać stanu; nie należy polegać na niej.  
  
 SCC_DIRSTATUS_NOTCONTROLLED  
 Katalog nie jest pod kontrolą źródła.  
  
 SCC_DIRSTATUS_CONTROLLED  
 Katalog jest pod kontrolą źródła.  
  
 SCC_DIRSTATUS_EMPTYPROJ  
 Projekt odpowiadający ten katalog jest pusty.  
  
## <a name="see-also"></a>Zobacz też  
 [Wtyczek kontroli kodu źródłowego](../extensibility/source-control-plug-ins.md)   
 [SccDirQueryInfo](../extensibility/sccdirqueryinfo-function.md)

