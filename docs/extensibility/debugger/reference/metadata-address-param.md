---
title: METADATA_ADDRESS_PARAM | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: METADATA_ADDRESS_PARAM
helpviewer_keywords: METADATA_ADDRESS_PARAM structure
ms.assetid: 90904f19-0e71-4cb3-a56e-6a2e92f66dfc
caps.latest.revision: "6"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 472eee2ee8cd657457e2c31331fbdedc2db075ae
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="metadataaddressparam"></a>METADATA_ADDRESS_PARAM
Ta struktura reprezentuje parametr metody lub funkcji.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct _tagMETADATA_ADDRESS_PARAM {  
   _mdToken tokMethod;  
   _mdToken tokParam;  
   DWORD    dwIndex;  
} METADATA_ADDRESS_PARAM;  
```  
  
```csharp  
public struct METADATA_ADDRESS_PARAM {  
   public int  tokMethod;  
   public int  tokParam;  
   public uint dwIndex;  
}  
```  
  
## <a name="terms"></a>Warunki  
 tokMethod  
 Identyfikator metody parametr jest częścią.  
  
 tokParam  
 Identyfikator parametru.  
  
 dwIndex  
 Indeks parametru na liście parametrów.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest częścią Unii w [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) struktury, kiedy `dwKind` pole `DEBUG_ADDRESS_UNION` ustawiono struktury `ADDRESS_KIND_PARAM` (wartość z zakresu od [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md) Wyliczenie).  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktury i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)   
 [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)