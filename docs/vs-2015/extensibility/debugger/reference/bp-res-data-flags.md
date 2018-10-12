---
title: BP_RES_DATA_FLAGS | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- BP_RES_DATA_FLAGS
helpviewer_keywords:
- BP_RES_DATA_FLAGS enumeration
ms.assetid: d97611e2-def6-45a9-ad7d-eedf2ad4c82b
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 189b1b8c4e597af6e1bd0a63824e53059a27c125
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49201633"
---
# <a name="bpresdataflags"></a>BP_RES_DATA_FLAGS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Określa, czy punkt przerwania danych jest emulowane lub wdrożonych w sprzętu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
enum enum_BP_RES_DATA_FLAGS {   
   BP_RES_DATA_EMULATED = 0x0001  
};  
typedef DWORD BP_RES_DATA_FLAGS;  
```  
  
```csharp  
public enum enum_BP_RES_DATA_FLAGS {   
   BP_RES_DATA_EMULATED = 0x0001  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 BP_RES_DATA_EMULATED  
 Określa, że punkt przerwania danych jest emulowane.  
  
## <a name="remarks"></a>Uwagi  
 Używany do `dwFlags` członkiem [BP_RESOLUTION_DATA](../../../extensibility/debugger/reference/bp-resolution-data.md) struktury.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_RESOLUTION_DATA](../../../extensibility/debugger/reference/bp-resolution-data.md)

