---
title: SEEK_START | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- SEEK_START
helpviewer_keywords:
- SEEK_START enumeration
ms.assetid: 55bd8901-626e-428b-a263-23b14417f4c6
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a10d749022757860c6f7cc620091c2ac10623976
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49905225"
---
# <a name="seekstart"></a>SEEK_START
Określa położenie, z którym ma zostać rozpoczęte wyszukiwanie w strumieniu dezasemblacji.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_SEEK_START {   
   SEEK_START_BEGIN       = 0x0001,  
   SEEK_START_END         = 0x0002,  
   SEEK_START_CURRENT     = 0x0003,  
   SEEK_START_CODECONTEXT = 0x0004,  
   SEEK_START_CODELOCID   = 0x0005  
};  
typedef DWORD SEEK_START;  
```  
  
```csharp  
public enum enum_SEEK_START {   
   SEEK_START_BEGIN       = 0x0001,  
   SEEK_START_END         = 0x0002,  
   SEEK_START_CURRENT     = 0x0003,  
   SEEK_START_CODECONTEXT = 0x0004,  
   SEEK_START_CODELOCID   = 0x0005  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 SEEK_START_BEGIN  
 Rozpoczyna się wyszukiwanie od początku bieżącego dokumentu.  
  
 SEEK_START_END  
 Rozpoczyna się wyszukiwanie na koniec bieżącego dokumentu.  
  
 SEEK_START_CURRENT  
 Rozpoczyna się wyszukiwanie w bieżącym położeniu bieżącego dokumentu.  
  
 SEEK_START_CODECONTEXT  
 Rozpoczyna się wyszukiwanie w kontekście danego kodu bieżącego dokumentu.  
  
 SEEK_START_CODELOCID  
 Rozpoczyna się wyszukiwanie na identyfikator lokalizacji danego kodu. Identyfikatory lokalizacji kodu są pobierane przez wywołanie metody [GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md).  
  
## <a name="remarks"></a>Uwagi  
 Przekazywany jako argument do [Seek](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Wyszukiwanie](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)   
 [GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md)