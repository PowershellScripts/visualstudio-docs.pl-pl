---
title: PROCESS_INFO_FLAGS | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- PROCESS_INFO_FLAGS
helpviewer_keywords:
- PROCESS_INFO_FLAGS enumeration
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 04bc34de6e7ecbc438cfc63ed08c684cf4224366
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49917027"
---
# <a name="processinfoflags"></a>PROCESS_INFO_FLAGS

W tym artykule opisano lub określa właściwości procesu.

## <a name="syntax"></a>Składnia

```cpp
enum enum_PROCESS_INFO_FLAGS { 
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,
   PIFLAG_PROCESS_STOPPED   = 0x00000004,
   PIFLAG_PROCESS_RUNNING   = 0x00000008,
};
typedef DWORD PROCESS_INFO_FLAGS;
```

```csharp
enum enum_PROCESS_INFO_FLAGS { 
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,
   PIFLAG_PROCESS_STOPPED   = 0x00000004,
   PIFLAG_PROCESS_RUNNING   = 0x00000008,
};
```

## <a name="members"></a>Elementy członkowskie

PIFLAG_SYSTEM_PROCESS  
Wskazuje, że proces jest proces systemowy.

PIFLAG_DEBUGGER_ATTACHED  
Wskazuje, że proces jest debugowany przez debuger. Może być [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] debugera, lub może być kilka innych debugera, na przykład WinDbg.

PIFLAG_PROCESS_STOPPED  
Wskazuje, że proces zostanie zatrzymany. Prawidłowe tylko wtedy, gdy `PIFLAG_DEBUGGER_ATTACHED` jest także określona. Dostępne w programie Visual Studio 2005 i nowszych wersjach.

PIFLAG_PROCESS_RUNNING  
Wskazuje, że proces jest uruchomiony. Prawidłowe tylko wtedy, gdy `PIFLAG_DEBUGGER_ATTACHED` jest także określona. Dostępne w programie Visual Studio 2005 i nowszych wersjach.

## <a name="remarks"></a>Uwagi

Używany do `Flags` członkiem [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) struktury.

Te flagi mogą być łączone przy użyciu bitowego operatora `OR`.

## <a name="requirements"></a>Wymagania

Nagłówek: msdbg.h

Namespace: Microsoft.VisualStudio.Debugger.Interop

Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Zobacz też

[Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)