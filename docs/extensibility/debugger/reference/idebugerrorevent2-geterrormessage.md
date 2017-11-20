---
title: IDebugErrorEvent2::GetErrorMessage | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugErrorEvent2::GetErrorMessage
helpviewer_keywords: IDebugErrorEvent2::GetErrorMessage
ms.assetid: 9e3b0d74-a2dd-4eaa-bd95-21b2f9c79409
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0b8a4e4c2ca938d8c600d3fd9ef0e615aa847fd9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugerrorevent2geterrormessage"></a>IDebugErrorEvent2::GetErrorMessage
Zwraca informacje umożliwiające temu konstrukcji komunikatu o błędzie zrozumiałą dla użytkownika.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetErrorMessage(  
   MESSAGETYPE* pMessageType,  
   BSTR*        pbstrErrorFormat,  
   HRESULT*     hrErrorReason,  
   DWORD*       pdwType,  
   BSTR*        pbstrHelpFileName,  
   DWORD*       pdwHelpId  
);  
```  
  
```csharp  
int GetErrorMessage(  
   out enum_MESSAGETYPE   pMessageType,  
   out string             pbstrErrorFormat,  
   out int                phrErrorReason,  
   out uint               pdwType,  
   out string             pbstrHelpFileName,  
   out uint               pdwHelpId  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pMessageType`  
 [out] Zwraca wartość z zakresu od [MESSAGETYPE](../../../extensibility/debugger/reference/messagetype.md) wyliczenie opisujące typ komunikatu.  
  
 `pbstrErrorFormat`  
 [out] Format komunikatu końcowego dla użytkownika (patrz "Uwagi", aby uzyskać szczegółowe informacje).  
  
 `hrErrorReason`  
 [out] Kod błędu: komunikat dotyczy.  
  
 `pdwType`  
 [out] Ważność błędu (Użyj stałe MB_XXX dla `MessageBox`, na przykład `MB_EXCLAMATION` lub `MB_WARNING`).  
  
 `pbstrHelpFileName`  
 [out] Ścieżka do pliku pomocy (zestaw ma wartość null, jeśli plik pomocy nie istnieje).  
  
 `pdwHelpId`  
 [out] Identyfikator tematu pomocy do wyświetlenia (wartość 0, jeśli ma tematu pomocy).  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Komunikat o błędzie powinien być sformatowany wzdłuż linii `"What I was doing.  %1"`. `"%1"` Będą następnie zastąpione przez obiekt wywołujący komunikat pochodzi z kodu błędu (który jest zwracany w `hrErrorReason`). `pMessageType` Parametr określa, że obiekt wywołujący wyświetlania ostatni komunikat o błędzie.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md)   
 [MESSAGETYPE](../../../extensibility/debugger/reference/messagetype.md)