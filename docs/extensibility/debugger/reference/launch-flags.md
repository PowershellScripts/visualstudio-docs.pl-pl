---
title: LAUNCH_FLAGS | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: LAUNCH_FLAGS
helpviewer_keywords: LAUNCH_FLAGS enumeration
ms.assetid: f51aab02-d257-4302-bb79-b7d8ba9ac4e5
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 69942eef506f5c95f2d7d1b37b4fb439fcbca5f2
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="launchflags"></a>LAUNCH_FLAGS
Określa flagi uruchamiania debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_LAUNCH_FLAGS {   
   LAUNCH_DEBUG      = 0x0000,  
   LAUNCH_NODEBUG    = 0x0001,  
   LAUNCH_ENABLE_ENC = 0x0002,  
   LAUNCH_MERGE_ENV  = 0x0004  
};  
typedef DWORD LAUNCH_FLAGS;  
```  
  
```csharp  
public enum enum_LAUNCH_FLAGS {   
   LAUNCH_DEBUG      = 0x0000,  
   LAUNCH_NODEBUG    = 0x0001,  
   LAUNCH_ENABLE_ENC = 0x0002,  
   LAUNCH_MERGE_ENV  = 0x0004  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 LAUNCH_DEBUG  
 Uruchamia proces do debugowania.  
  
 LAUNCH_NODEBUG  
 Uruchamia proces bez jego debugowania.  
  
 LAUNCH_ENABLE_ENC  
 PRZESTARZAŁE, NIE NALEŻY UŻYWAĆ.  
  
 LAUNCH_MERGE_ENV  
 Uruchamia proces i scala środowisko uruchamiania hosta.  
  
## <a name="remarks"></a>Uwagi  
 Te wartości są przekazywane jako argument [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md) metody.  
  
 Te flagi mogą być łączone z bitowego `OR`.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)