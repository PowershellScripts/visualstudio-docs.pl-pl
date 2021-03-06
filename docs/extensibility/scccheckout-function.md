---
title: Funkcja SccCheckout | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- SccCheckout
helpviewer_keywords:
- SccCheckout function
ms.assetid: 06e9ecd7-fc09-40c1-9dd1-2b56c622c80b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1ba80df71dce70ad4a6a0953d37f8f87bd487e12
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49908525"
---
# <a name="scccheckout-function"></a>Funkcja SccCheckout
Biorąc pod uwagę listę w pełni kwalifikowanej nazwy, ta funkcja wyewidencjonowuje je na dysku lokalnym. Komentarza ma zastosowanie do wszystkich plików, które są wyewidencjonowane. Argument komentarz może być `null` ciągu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccCheckout (  
   LPVOID    pvContext,  
   HWND      hWnd,  
   LONG      nFiles,  
   LPCSTR*   lpFileNames,  
   LPCSTR    lpComment,  
   LONG      fOptions,  
   LPCMDOPTS pvOptions  
);  
```  
  
### <a name="parameters"></a>Parametry  
 pvContext  
 [in] Struktura kontekście wtyczki kontroli źródła.  
  
 hWnd  
 [in] Uchwyt okna środowiska IDE, które wtyczka do kontroli źródła można użyć jako element nadrzędny dla wszystkie okna dialogowe, które zawiera.  
  
 Niepowodzeń  
 [in] Liczba plików wybranych do wyewidencjonowania.  
  
 lpFileNames  
 [in] Tablica nazw w pełni kwalifikowaną ścieżką lokalną plików do wyewidencjonowania.  
  
 lpComment  
 [in] Komentarz, które mają być stosowane do każdego z wybranych plików, które są wyewidencjonowane.  
  
 fOptions  
 [in] Polecenie flagi (zobacz [flagi bitowe używane przez określone polecenia](../extensibility/bitflags-used-by-specific-commands.md)).  
  
 pvOptions  
 [in] Opcje plug-określonych kontroli źródła.  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczki kontroli źródła tej funkcji powinien zwrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_OK|Wyewidencjonowanie zostało pomyślnie zakończone.|  
|SCC_E_FILENOTCONTROLLED|Wybrany plik nie jest pod kontrolą kodu źródłowego.|  
|SCC_E_ACCESSFAILURE|Wystąpił problem podczas uzyskiwania dostępu do systemu kontroli źródła, prawdopodobnie z powodu problemów z siecią lub rywalizacji o zasoby. Ponowienie próby jest zalecane.|  
|SCC_E_NOTAUTHORIZED|Użytkownik nie może wykonać tej operacji.|  
|SCC_E_NONSPECIFICERROR|Wystąpił nieokreślony błąd. Plik nie został wyewidencjonowany.|  
|SCC_E_ALREADYCHECKEDOUT|Użytkownik ma już ten plik wyewidencjonowany.|  
|SCC_E_FILEISLOCKED|Plik jest zablokowany zabronienia tworzenie nowych wersji.|  
|SCC_E_FILEOUTEXCLUSIVE|Inny użytkownik ma wykonać wyewidencjonowania na wyłączność tego pliku.|  
|SCC_I_OPERATIONCANCELED|Operacja została anulowana przed ukończeniem.|  
  
## <a name="see-also"></a>Zobacz także  
 [Funkcje interfejsu API wtyczki kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)   
 [Flagi bitowe używane przez określone polecenia](../extensibility/bitflags-used-by-specific-commands.md)