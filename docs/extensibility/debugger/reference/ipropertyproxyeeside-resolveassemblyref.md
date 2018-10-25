---
title: IPropertyProxyEESide::ResolveAssemblyRef | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IPropertyProxyEESide::ResolveAssemblyRef
helpviewer_keywords:
- IPropertyProxyEESide::ResolveAssemblyRef
ms.assetid: 662ca0a6-dad0-4c00-a718-bb3bbc5bd9da
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c7711d185e92b0cc8a29070aa78a4acff835df33
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49846944"
---
# <a name="ipropertyproxyeesideresolveassemblyref"></a>IPropertyProxyEESide::ResolveAssemblyRef
Określa lokalizację odwołanie do określonego zestawu zarządzanego.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT ResolveAssemblyRef(  
   BSTR*                  assemName,  
   IEEDataStorage**       assemBytes,  
   IEEDataStorage**       assemPdb,  
   BSTR*                  assemLocation,  
   ASSEMBLYLOCRESOLUTION* alr  
);  
```  
  
```csharp  
int ResolveAssemblyRef(  
   ref string                     assemName,  
   out IEEDataStorage             assemBytes,  
   out IEEDataStorage             assemPdb,  
   out string                     assemLocation,  
   out enum_ASSEMBLYLOCRESOLUTION alr  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `assemName`  
 [in] Nazwa zestawu, aby rozwiązać.  
  
 `assemBytes`  
 [out] Zwraca [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) obiekt zawierający bajtów zestawu skojarzonej z odwołaniem.  
  
 `assemPdb`  
 [out] Zwraca `IEEDataStorage` obiekt, który zawiera symbol są przechowywane dane skojarzone z tym odwołaniem.  
  
 `assemLocation`  
 [out] Zwraca ścieżkę lokalizacji tego odwołania.  
  
 `alr`  
 [out] Zwraca wartość z zakresu od [ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md) Wyliczenie wskazujące lokalizację to odwołanie do zestawu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda nie jest zwykle implementowany przez ewaluatora wyrażeń niestandardowych.  
  
## <a name="see-also"></a>Zobacz też  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md)