---
title: Moduł wyliczający kod stanu pliku | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- named constants, SccStatus enumerator
- source control plug-ins, file status enumeration
- SccStatus enumerator
- file status code enumerator
ms.assetid: 5c37876b-c83c-4ca1-837b-57cd465a879a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 884c7ab1b5d4fe1461fd1ae00fbc670f0bc7b6f2
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49921018"
---
# <a name="file-status-code-enumerator"></a>Moduł wyliczający kod stanu pliku
`SccStatus` Modułu wyliczającego zawiera nazwanych stałych, określające stan pliku w systemie kontroli źródła. To wyliczenie jest używane przez [SccQueryInfo](../extensibility/sccqueryinfo-function.md) i `POPLISTFUNC` funkcji wywołania zwrotnego (zobacz [POPLISTFUNC](../extensibility/poplistfunc.md) Aby uzyskać szczegółowe informacje).  
  
## <a name="syntax"></a>Składnia  
  
```  
enum SccStatus {  
   SCC_STATUS_INVALID          = -1L,  
   SCC_STATUS_NOTCONTROLLED    = 0x0000L,  
   SCC_STATUS_CONTROLLED       = 0x0001L,  
   SCC_STATUS_CHECKEDOUT       = 0x0002L,  
   SCC_STATUS_OUTOTHER         = 0x0004L,  
   SCC_STATUS_OUTEXCLUSIVE     = 0x0008L,  
   SCC_STATUS_OUTMULTIPLE      = 0x0010L,  
   SCC_STATUS_OUTOFDATE        = 0x0020L,  
   SCC_STATUS_DELETED          = 0x0040L,  
   SCC_STATUS_LOCKED           = 0x0080L,  
   SCC_STATUS_MERGED           = 0x0100L,  
   SCC_STATUS_SHARED           = 0x0200L,  
   SCC_STATUS_PINNED           = 0x0400L,  
   SCC_STATUS_MODIFIED         = 0x0800L,  
   SCC_STATUS_OUTBYUSER        = 0x1000L  
   SCC_STATUS_NOMERGE          = 0x2000L  
   SCC_STATUS_RESERVED_1       = 0x4000L  
   SCC_STATUS_RESERVED_2       = 0x8000L  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 SCC_STATUS_INVALID  
 Nie można uzyskać stanu; nie należy polegać na niej.  
  
 SCC_STATUS_NOTCONTROLLED  
 Plik nie jest pod kontrolą źródła.  
  
 SCC_STATUS_CONTROLLED  
 Plik jest pod kontrolą źródła.  
  
 SCC_STATUS_CHECKEDOUT  
 Wyewidencjonowany przez bieżącego użytkownika na dysku lokalnym.  
  
 SCC_STATUS_OUTOTHER  
 Plik jest wyewidencjonowany przez innego użytkownika.  
  
 SCC_STATUS_OUTEXCLUSIVE  
 Plik jest wyewidencjonowany.  
  
 SCC_STATUS_OUTMULTIPLE  
 Plik jest wyewidencjonowany przez więcej niż jednego użytkownika.  
  
 SCC_STATUS_OUTOFDATE  
 Plik nie jest najnowsza.  
  
 SCC_STATUS_DELETED  
 Plik został usunięty z projektu.  
  
 SCC_STATUS_LOCKED  
 Plik jest zablokowany; nie dozwolone więcej wersji.  
  
 SCC_STATUS_MERGED  
 Plik został połączony, ale nie zostały jeszcze rozwiązane/weryfikacji.  
  
 SCC_STATUS_SHARED  
 Plik jest udostępniony między projektami.  
  
 SCC_STATUS_PINNED  
 Plik jest udostępniony do jawnego wersji.  
  
 SCC_STATUS_MODIFIED  
 Plik został zmodyfikowany/uszkodzony/naruszone.  
  
 SCC_STATUS_OUTBYUSER  
 Plik jest wyewidencjonowany przez bieżącego użytkownika.  
  
 SCC_STATUS_NOMERGE  
 Plik nigdy nie mogą zostać scalone z i nie muszą zostać zapisane przed GET.  
  
 SCC_STATUS_RESERVED_1  
 Zarezerwowane do użytku wewnętrznego.  
  
 SCC_STATUS_RESERVED_2  
 Zarezerwowane do użytku wewnętrznego.  
  
## <a name="see-also"></a>Zobacz także  
 [Wtyczek kontroli kodu źródłowego](../extensibility/source-control-plug-ins.md)   
 [SccQueryInfo](../extensibility/sccqueryinfo-function.md)   
 [POPLISTFUNC](../extensibility/poplistfunc.md)