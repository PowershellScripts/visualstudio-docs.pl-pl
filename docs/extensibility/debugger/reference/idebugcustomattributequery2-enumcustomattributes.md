---
title: IDebugCustomAttributeQuery2::EnumCustomAttributes | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugCustomAttributeQuery2::EnumCustomAttributes
helpviewer_keywords: IDebugCustomAttributeQuery2::EnumCustomAttributes
ms.assetid: 94bfce74-aa3d-45f0-8e04-5715faf85217
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 47b643c8f08de60bb873f3daf69ee93e0816d31f
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugcustomattributequery2enumcustomattributes"></a>IDebugCustomAttributeQuery2::EnumCustomAttributes
Pobiera moduł wyliczający dla wszystkich atrybutów niestandardowych dołączony do tego pola.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT EnumCustomAttributes(   
   IEnumDebugCustomAttributes** ppEnum  
);  
```  
  
```csharp  
int EnumCustomAttributes(  
   out IEnumDebugCustomAttributes ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnum`  
 [out] Zwraca [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md) obiekt reprezentujący listę atrybutów niestandardowych; w przeciwnym razie zwraca wartość null, jeśli nie ma żadnych atrybutów niestandardowych.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca S_OK lub wartości S_FALSE, jeśli nie ma żadnych atrybutów niestandardowych dla tego pola. W przeciwnym razie zwraca błąd o kodzie;  
  
## <a name="remarks"></a>Uwagi  
 Pole może mieć wiele atrybutów niestandardowych.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugCustomAttributeQuery2](../../../extensibility/debugger/reference/idebugcustomattributequery2.md)   
 [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)