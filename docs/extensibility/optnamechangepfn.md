---
title: OPTNAMECHANGEPFN | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- OPTNAMECHANGEPFN
helpviewer_keywords:
- OPTNAMECHANGEPFN callback function
ms.assetid: 147303f3-c7f1-438a-81b7-db891ea3d076
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 12b8f6eb441eb9ca65cbdf2215363af48c65bfa4
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49912997"
---
# <a name="optnamechangepfn"></a>OPTNAMECHANGEPFN
Jest to określone w wywołaniu do funkcji wywołania zwrotnego [SccSetOption](../extensibility/sccsetoption-function.md) (przy użyciu opcji `SCC_OPT_NAMECHANGEPFN`) i jest używany do komunikowania się nazwa zmiany wprowadzone przez kontroli źródła wtyczki powrót środowiska IDE.  
  
## <a name="signature"></a>Podpis  
  
```cpp  
typedef void (*OPTNAMECHANGEPFN)(  
   LPVOID pvCallerData,  
   LPCSTR pszOldName,  
   LPCSTR pszNewName  
);  
```  
  
## <a name="parameters"></a>Parametry  
 pvCallerData  
 [in] Wartość użytkownika określonego w poprzednie wywołanie [SccSetOption](../extensibility/sccsetoption-function.md) (przy użyciu opcji `SCC_OPT_USERDATA`).  
  
 pszOldName  
 [in] Oryginalna nazwa pliku.  
  
 pszNewName  
 [in] Nazwa pliku została zmieniona na.  
  
## <a name="return-value"></a>Wartość zwracana  
 Brak.  
  
## <a name="remarks"></a>Uwagi  
 Po zmianie nazwy pliku podczas operacji kontroli źródła, wtyczka do kontroli źródła może generować powiadomienia o zmianie nazwy przez to wywołanie zwrotne środowiska IDE programu.  
  
 Jeśli środowisko IDE nie obsługuje tego wywołania zwrotnego, nie będzie wywoływać [SccSetOption](../extensibility/sccsetoption-function.md) go określić. Jeśli wtyczka nie obsługuje tego wywołania zwrotnego, to zostanie zwrócona `SCC_E_OPNOTSUPPORTED` z `SccSetOption` działają w przypadku IDE podejmuje próbę ustawienia wywołania zwrotnego.  
  
## <a name="see-also"></a>Zobacz także  
 [Funkcje wywołania zwrotnego implementowane przez środowisko IDE](../extensibility/callback-functions-implemented-by-the-ide.md)   
 [SccSetOption](../extensibility/sccsetoption-function.md)