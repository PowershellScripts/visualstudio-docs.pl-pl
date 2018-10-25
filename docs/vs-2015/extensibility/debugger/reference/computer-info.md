---
title: COMPUTER_INFO | Dokumentacja firmy Microsoft
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
- COMPUTER_INFO structure
ms.assetid: 943085b2-f165-462d-9a4e-2086f0cdfff4
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f96d42936f62b7724629127a638d2ea534d3b6f4
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49883045"
---
# <a name="computerinfo"></a>COMPUTER_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

W tym artykule opisano komputera, na którym uruchomiony jest debugera.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
typedef struct tagCOMPUTER_INFO  
{  
    WORD wProcessorArchitecture;  
    WORD wSuiteMask;  
    DWORD dwOperatingSystemVersion;  
} COMPUTER_INFO;  
```  
  
```csharp  
public struct COMPUTER_INFO  
{  
    public ushort wProcessorArchitecture;  
    public ushort wSuiteMask;  
    public uint dwOperatingSystemVersion;  
}  
```  
  
## <a name="terms"></a>Warunki  
 wProcessorArchitecture  
 Określa z architekturą procesora.  
  
 wSuiteMask  
 Określa maskę pakietu.  
  
 dwOperatingSystemVersion  
 Numer wersji systemu operacyjnego.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest zwracany przez [GetComputerInfo](../../../extensibility/debugger/reference/idebugwindowscomputerport2-getcomputerinfo.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetComputerInfo](../../../extensibility/debugger/reference/idebugwindowscomputerport2-getcomputerinfo.md)

