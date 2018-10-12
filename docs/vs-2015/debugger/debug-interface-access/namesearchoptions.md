---
title: Namesearchoptions — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- NameSearchOptions enumeration
ms.assetid: 67dfbede-2678-47df-b664-5c49841d0b9b
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6b3e29ece07ffb385da0c54a3f8f4d31afc60be7
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49199236"
---
# <a name="namesearchoptions"></a>NameSearchOptions
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Określa opcje wyszukiwania dla nazwy symboli i plików.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
enum NameSearchOptions {   
   nsNone,  
   nsfCaseSensitive     = 0x1,  
   nsfCaseInsensitive   = 0x2,  
   nsfFNameExt          = 0x4,  
   nsfRegularExpression = 0x8,  
   nsfUndecoratedName   = 0x10,  
  
// For backward compatibility:  
   nsCaseSensitive           = nsfCaseSensitive,  
   nsCaseInsensitive         = nsfCaseInsensitive,  
   nsFNameExt                = nsfCaseInsensitive | nsfFNameExt,  
   nsRegularExpression       = nsfRegularExpression | nsfCaseSensitive,  
   nsCaseInRegularExpression = nsfRegularExpression | nsfCaseInsensitive  
};  
```  
  
## <a name="elements"></a>Elementy  
 `nsNone`  
 Nie określono opcji.  
  
 `nsfCaseSensitive`  
 Stosuje musi odpowiadać nazwie uwzględniana wielkość liter.  
  
 `nsfCaseInsensitive`  
 Stosuje dopasowanie bez uwzględniania wielkości liter nazwy.  
  
 `nsfFNameExt`  
 Traktuje nazw jako ścieżki, a następnie stosuje musi odpowiadać nazwie nazwa_pliku.Ext.  
  
 `nsfRegularExpression`  
 Stosuje dopasowanie liter nazwy przy użyciu gwiazdki (*) i znaki zapytania (?) jako symboli wieloznacznych.  
  
 `nsfUndecoratedName`  
 Dotyczy tylko symbole, które mają zarówno niedekorowanego i nazw ozdobionych.  
  
## <a name="remarks"></a>Uwagi  
 Wartości z tego wyliczenia są przekazywane do następujących metod:  
  
-   [IDiaSession::findChildren](../../debugger/debug-interface-access/idiasession-findchildren.md)  
  
-   [IDiaSession::findFile](../../debugger/debug-interface-access/idiasession-findfile.md)  
  
-   [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: dia2.h  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia i struktury](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasession::findchildren —](../../debugger/debug-interface-access/idiasession-findchildren.md)   
 [Idiasession::FindFile —](../../debugger/debug-interface-access/idiasession-findfile.md)   
 [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)



