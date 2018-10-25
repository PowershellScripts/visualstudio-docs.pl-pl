---
title: IDebugField::Equal | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugField::Equal
helpviewer_keywords:
- IDebugField::Equal method
ms.assetid: 75369fe6-ddd3-497d-80d1-2488e6100e9f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1ae30cd36d2a3f51b697afa3cb5f4615a5f322da
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49830785"
---
# <a name="idebugfieldequal"></a>IDebugField::Equal
Ta metoda porównuje tego pola z określonym polem pod kątem równości.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Equal(   
   IDebugField* pField  
);  
```  
  
```csharp  
int Equal(  
   IDebugField pField  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pField`  
 [in] Pole do porównania z niej.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli pola są takie same, zwraca `S_OK`. Jeśli pola są różne, zwraca `S_FALSE.` w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)