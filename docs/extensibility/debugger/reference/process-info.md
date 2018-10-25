---
title: PROCESS_INFO | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- PROCESS_INFO
helpviewer_keywords:
- PROCESS_INFO structure
ms.assetid: 260c33cc-a05e-4645-84b6-536d0b3b0537
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 2a8f07cfb99ac42704d3829c30dbf5adbb16e9d0
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49864624"
---
# <a name="processinfo"></a>PROCESS_INFO
Zawiera informacje na temat procesu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct tagPROCESS_INFO {   
   PROCESS_INFO_FIELDS Fields;  
   BSTR                bstrFileName;  
   BSTR                bstrBaseName;  
   BSTR                bstrTitle;  
   AD_PROCESS_ID       ProcessId;  
   DWORD               dwSessionId;  
   BSTR                bstrAttachedSessionName;  
   FILETIME            CreationTime;  
   PROCESS_INFO_FLAGS  Flags;  
} PROCESS_INFO;  
```  
  
```csharp  
public struct PROCESS_INFO {   
   public uint          Fields;  
   public string        bstrFileName;  
   public string        bstrBaseName;  
   public string        bstrTitle;  
   public AD_PROCESS_ID ProcessId;  
   public uint          dwSessionId;  
   public string        bstrAttachedSessionName;  
   public FILETIME      CreationTime;  
   public uint          Flags;  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 Pola  
 Kombinacja flag z [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md) wyliczenie określające, które pola są wypełnione.  
  
 bstrFileName  
 Pełna nazwa ścieżki procesu. Równoważne z wywoływaniem [getname —](../../../extensibility/debugger/reference/idebugprocess2-getname.md) metody z parametrem `GN_FILENAME`.  
  
 bstrBaseName  
 Nazwa pliku i rozszerzenie procesu. Równoważne z wywoływaniem `IDebugProcess2::Getname` metody z parametrem `GN_BASENAME`.  
  
 bstrTitle  
 Tytuł proces, jeśli taka istnieje. Równoważne z wywoływaniem `IDebugProcess2::Getname` metody z parametrem `GN_TITLE`.  
  
 Identyfikator procesu  
 [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) strukturę, która identyfikuje proces. Równoważne z wywoływaniem [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md) metody.  
  
 dwSessionId  
 Identyfikator ten proces jest uruchomiony w sesji debugowania.  
  
 bstrAttachedSessionName  
 Nazwa sesji dołączone. Równoważne z wywoływaniem [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md) metody.  
  
 CreationTime  
 Godzina utworzenia procesu.  
  
 Flagi  
 Kombinacja flag z [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md) wyliczenie określające właściwości procesu.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest przekazywany do [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) metody, gdzie jest wypełnione.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md)   
 [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md)   
 [Getname —](../../../extensibility/debugger/reference/idebugprocess2-getname.md)   
 [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)   
 [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md)