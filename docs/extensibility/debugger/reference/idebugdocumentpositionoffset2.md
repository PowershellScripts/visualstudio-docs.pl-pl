---
title: IDebugDocumentPositionOffset2 | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: IDebugDocumentPositionOffset2 interface
ms.assetid: f1b05db3-50d8-453f-a72f-e68b239236a4
caps.latest.revision: "7"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 81c934add7248b7d63854b259957d58aae298401
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugdocumentpositionoffset2"></a>IDebugDocumentPositionOffset2
Reprezentuje pozycji w pliku źródłowym jako przesunięcie znaków.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDebugDocumentPositionOffset2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uwagi dotyczące implementacji  
 Zaimplementowane IDE i używane przez aparaty debugowania.  
  
## <a name="methods"></a>Metody  
 W poniższej tabeli przedstawiono metody `IDebugDocumentPositionOffset2`.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[GetRange](../../../extensibility/debugger/reference/idebugdocumentpositionoffset2-getrange.md)|Pobiera zakres dla bieżącego położenia dokumentu.|  
  
## <a name="remarks"></a>Uwagi  
 To polecenie zwróci te same informacje co [GetRange](../../../extensibility/debugger/reference/idebugdocumentposition2-getrange.md) jednak `char` powoduje przesunięcie od początku dokumentu. Wyświetla dokument, tak, czy istnieje on na dysku, to znaczy Jednowymiarowa tablica znaków, zamiast informacji wiersza i kolumny, która zwykle jest zwracana.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugDocumentPosition2](../../../extensibility/debugger/reference/idebugdocumentposition2.md)