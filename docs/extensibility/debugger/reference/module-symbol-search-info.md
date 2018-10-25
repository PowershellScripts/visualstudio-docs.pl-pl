---
title: MODULE_SYMBOL_SEARCH_INFO | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- MODULE_SYMBOL_SEARCH_INFO
helpviewer_keywords:
- MODULE_SYMBOL_SEARCH_INFO structure
ms.assetid: 432aff03-08a5-4c5a-b2d5-e212090fc70a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9deadc13f8cbe3678282bb2d9ac619959ecd26b3
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49875921"
---
# <a name="modulesymbolsearchinfo"></a>MODULE_SYMBOL_SEARCH_INFO
Zawiera informacje o stanie dotyczące ścieżki wyszukiwania symboli, które zostały przeszukiwane.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct _tagSYMBOL_SEARCH_INFO  
{  
   SYMBOL_SEARCH_INFO_FIELDS dwValidFields;  
   BSTR                      bstrVerboseSearchInfo;  
} MODULE_SYMBOL_SEARCH_INFO;  
```  
  
```csharp  
public struct MODULE_SYMBOL_SEARCH_INFO {  
   public uint   dwValidFields;  
   public string bstrVerboseSearchInfo;  
}  
```  
  
#### <a name="parameters"></a>Parametry  
 `dwValidFields`  
 Kombinacja flag z [SYMBOL_SEARCH_INFO_FIELDS](../../../extensibility/debugger/reference/symbol-search-info-fields.md) wyliczenie opisujące rodzaju informacje o wyszukiwaniu opisane w tej strukturze.  
  
 `bstrVerboseSearchInfo`  
 Ścieżka wyszukiwania i wyników połączonych w jeden ciąg.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest zwracany z wywołania [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md) metody.  
  
 Jeśli `bstrVerboseSearchInfo` pole nie jest puste, a następnie zawiera listę ścieżek przeszukiwane i wyniki tego wyszukiwania. Lista jest formatowana ze ścieżką, w którym następuje wielokropek ("..."), a następnie wynik. W przypadku więcej niż jedną parę wynik ścieżki każdej pary jest oddzielony przez parę "\r\n" (powrót karetki return/wysuw wiersza). Wzorzec wygląda następująco:  
  
 \<Ścieżka >... \<wyniku > \r\n\<ścieżka >... \<wyniku > \r\n\<ścieżka >... \<wyniku >  
  
 Należy pamiętać, że ostatni wpis nie ma sekwencji \r\n.  
  
 Poniżej przedstawiono możliwe `bstrVerboseSearchInfo` ciąg, który została wysłana na standardowe wyjście.  
  
 `c:\symbols\user32.pdb... File not found.`  
  
 `c:\winnt\symbols\user32.pdb... Version does not match.`  
  
 `\\symbols\symbols\user32.dll\0a8sd0ad8ad\user32.pdb... Symbols loaded.`  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md)