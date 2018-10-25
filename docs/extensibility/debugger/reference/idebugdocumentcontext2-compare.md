---
title: IDebugDocumentContext2::Compare | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugDocumentContext2::Compare
helpviewer_keywords:
- IDebugDocumentContext2::Compare
ms.assetid: 2327b1ba-52d0-42fb-a01e-63cb4b332d2f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: af349d8568d50e2059ab33ad54b14f499c7b6afd
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49913465"
---
# <a name="idebugdocumentcontext2compare"></a>IDebugDocumentContext2::Compare
Porównuje ten kontekst dokumentu do danej tablicy kontekstów dokumentu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Compare(   
   DOCCONTEXT_COMPARE       compare,  
   IDebugDocumentContext2** rgpDocContextSet,  
   DWORD                    dwDocContextSetLen,  
   DWORD*                   pdwDocContext  
);  
```  
  
```csharp  
int Compare(   
   enum_ DOCCONTEXT_COMPARE compare,  
   IDebugDocumentContext2[] rgpDocContextSet,  
   uint                     dwDocContextSetLen,  
   out uint                 pdwDocContext  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `compare`  
 [in] Wartość z zakresu od [DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md) wyliczenie, który określa typ porównania.  
  
 `rgpDocContextSet`  
 [in] Tablica [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) obiekty reprezentujące kontekstów dokumentu, którą jest porównywany.  
  
 `dwDocContextSetLen`  
 [in] Długość tablicy kontekstów dokumentu do porównania.  
  
 `pdwDocContext`  
 [out] Zwraca indeks do `rgpDocContextSet` tablicy pierwszy kontekst dokumentu, który spełnia porównanie.  
  
## <a name="return-value"></a>Wartość zwracana  
 Zwraca `S_OK` Jeśli znaleziono dopasowanie. Zwraca `S_FALSE` Jeżeli nie znaleziono dopasowania. W przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) obiekty, które są przekazywane w tablicy musi być implementowana przez tego samego aparatu debugowania, który implementuje `IDebugDocumentContext2` obiektu wywołanego w przeciwnym razie wynik porównania jest nieprawidłowy.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md)