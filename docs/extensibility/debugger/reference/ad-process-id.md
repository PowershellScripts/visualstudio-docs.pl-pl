---
title: AD_PROCESS_ID | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- AD_PROCESS_ID
helpviewer_keywords:
- AD_PROCESS_ID union
ms.assetid: 4cb40d12-2e92-4f09-83f4-689928bd65b3
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9634d16a89670b92e616e4bd6b878f41166aea2b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49833879"
---
# <a name="adprocessid"></a>AD_PROCESS_ID
Określa identyfikator procesu, który może mieć identyfikator systemu lub identyfikator GUID.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct _AD_PROCESS_ID {  
   AD_PROCESS_ID_TYPE ProcessIdType;  
   union {  
      DWORD dwProcessId;   
      GUID  guidProcessId;   
      DWORD dwUnused;   
   } ProcessId;  
} AD_PROCESS_ID;  
```  
  
```csharp  
public struct AD_PROCESS_ID {  
   AD_PROCESS_ID_TYPE ProcessIdType;  
   DWORD              dwProcessId;   
   GUID               guidProcessId;   
   DWORD              dwUnused;   
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 `ProcessIdType`  
 Wartość z zakresu od [AD_PROCESS_ID_TYPE](../../../extensibility/debugger/reference/ad-process-id-type.md) wyliczenie opisujące jak interpretować `ProcessId` Unii (lub dla kodu zarządzanego, które do członków struktury).  
  
 dwProcessId  
 Identyfikator procesu jako wartość z systemu.  
  
 guidProcessId  
 Identyfikator procesu jako identyfikatora GUID.  
  
 dwUnused  
 Dopełnienie.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest przekazywany do następujących metod:  
  
- [GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md)  
  
- [WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md)  
  
- [GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md)  
  
- [GetProcess](../../../extensibility/debugger/reference/idebugport2-getprocess.md)  
  
  I zostanie zwrócony z następujących metod:  
  
- [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)  
  
- [GetHostId](../../../extensibility/debugger/reference/idebugprogramhost2-gethostid.md)  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [Getprocess —](../../../extensibility/debugger/reference/idebugport2-getprocess.md)   
 [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)   
 [AD_PROCESS_ID_TYPE](../../../extensibility/debugger/reference/ad-process-id-type.md)   
 [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)   
 [GetHostId](../../../extensibility/debugger/reference/idebugprogramhost2-gethostid.md)   
 [GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md)   
 [WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md)   
 [GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md)