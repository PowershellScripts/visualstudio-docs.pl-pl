---
title: Funkcja SccRename | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: SccRename
helpviewer_keywords: SccRename function
ms.assetid: b467ade6-a1db-4c0b-b60f-7850ec4f79eb
caps.latest.revision: "12"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2936c2ea4425ad6eaccc2d23853f4174e1c9c2a2
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="sccrename-function"></a>Funkcja SccRename
Ta funkcja zmienia nazwę pliku w systemie kontroli źródła.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccRename(  
   LPVOID pvContext,  
   HWND   hWnd,  
   LPCSTR lpFileName,  
   LPCSTR lpNewName  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pvContext  
 [in] Struktura kontekstu wtyczkę kontroli źródła.  
  
 Właściwość hWnd  
 [in] Dojście do okna IDE, które wtyczka do kontroli źródła można używać jako elementu nadrzędnego wszystkie okna dialogowe, które zawiera.  
  
 lpFileName  
 [in] W pełni kwalifikowanej nazwy pliku zmianą nazwy pliku.  
  
 lpNewName  
 [in] Nowa nazwa FQDN. Jeśli ścieżka do katalogu jest inny, plik został przeniesiony w z podkatalogu co do innego.  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczkę kontroli źródła tej funkcji może przywrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_OK|Pomyślnie ukończono operację zmiany nazwy.|  
|SCC_E_PROJNOTOPEN|Projekt nie jest otwarty pod kontrolą źródła.|  
|SCC_E_FILENOTCONTROLLED|Plik nie jest pod kontrolą źródła.|  
|SCC_E_ACCESSFAILURE|Wystąpił problem podczas uzyskiwania dostępu do systemu kontroli źródła, prawdopodobnie z powodu problemów z siecią lub rywalizacji.|  
|SCC_E_NOTAUTHORIZED|Użytkownik nie ma uprawnień do ukończenia tej operacji.|  
|SCC_E_COULDNOTCREATEPROJECT|Nie można utworzyć projektu jako część procesu zmiany nazwy.|  
|SCC_E_OPNOTPERFORMED|Operacja nie została wykonana.|  
|SCC_E_NONSPECIFICERROR|Wystąpił błąd nieokreślonej lub ogólne.|  
  
## <a name="remarks"></a>Uwagi  
 Ta funkcja może służyć do zmiany nazwy pliku lub przenieść go z jednej lokalizacji do innej w systemie kontroli źródła. Wtyczka do kontroli źródła nie powinny podejmować próby dostępu do pliku na dysku. Odpowiada IDE Zmień nazwę pliku lokalnego.  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje API wtyczkę kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)