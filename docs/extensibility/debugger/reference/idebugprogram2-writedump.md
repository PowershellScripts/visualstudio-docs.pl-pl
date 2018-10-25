---
title: IDebugProgram2::WriteDump | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::WriteDump
helpviewer_keywords:
- IDebugProgram2::WriteDump
ms.assetid: 375afb8c-882d-44db-bfa7-e2c9eb555122
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3d2953b3f30a0d485b58afc04e8ce42158a7537e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49905275"
---
# <a name="idebugprogram2writedump"></a>IDebugProgram2::WriteDump
Zapisuje plik zrzutu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT WriteDump(   
   DUMPTYPE  DumpType,  
   LPCOLESTR pszDumpUrl  
);  
```  
  
```csharp  
int WriteDump(   
   enum_DUMPTYPE  DumpType,  
   string         pszDumpUrl  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `DumpType`  
 [in] Wartość z zakresu od [DUMPTYPE](../../../extensibility/debugger/reference/dumptype.md) wyliczenie, które określa typ zrzutu, na przykład, w skrócie lub long.  
  
 `pszDumpUrl`  
 [in] Adres URL zrzutu do zapisu. Zazwyczaj jest to w formie `file://c:\path\filename.ext`, ale może być dowolny prawidłowy adres URL.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Zrzut program zwykle obejmuje bieżącej ramki stosu, sam stos, Lista wątków, uruchomiony w programie i prawdopodobnie wszystkie pamięci, który jest właścicielem program.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)