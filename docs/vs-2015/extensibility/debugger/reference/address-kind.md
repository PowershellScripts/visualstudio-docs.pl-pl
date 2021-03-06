---
title: ADDRESS_KIND | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- ADDRESS_KIND
helpviewer_keywords:
- ADDRESS_KIND enumeration
ms.assetid: 3a12fbec-7088-4cf9-8f6f-ad8ddec6009a
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: dad092e8a0de1a69ded2f09e6c64de653edc8493
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/16/2018
ms.locfileid: "51734750"
---
# <a name="addresskind"></a>ADDRESS_KIND
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Określa typy adresów.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_ADDRESS_KIND {  
   ADDRESS_KIND_NATIVE                  = 0x0001,  
   ADDRESS_KIND_UNMANAGED_THIS_RELATIVE = 0x0002,  
   ADDRESS_KIND_UNMANAGED_PHYSICAL      = 0x0005,  
   ADDRESS_KIND_METADATA_METHOD         = 0x0010,  
   ADDRESS_KIND_METADATA_FIELD          = 0x0011,  
   ADDRESS_KIND_METADATA_LOCAL          = 0x0012,  
   ADDRESS_KIND_METADATA_PARAM          = 0x0013,  
   ADDRESS_KIND_METADATA_ARRAYELEM      = 0x0014,  
   ADDRESS_KIND_METADATA_RETVAL         = 0x0015,  
};  
typedef DWORD ADDRESS_KIND;  
```  
  
```csharp  
public enum enum_ADDRESS_KIND {  
   ADDRESS_KIND_NATIVE                  = 0x0001,  
   ADDRESS_KIND_UNMANAGED_THIS_RELATIVE = 0x0002,  
   ADDRESS_KIND_UNMANAGED_PHYSICAL      = 0x0005,  
   ADDRESS_KIND_METADATA_METHOD         = 0x0010,  
   ADDRESS_KIND_METADATA_FIELD          = 0x0011,  
   ADDRESS_KIND_METADATA_LOCAL          = 0x0012,  
   ADDRESS_KIND_METADATA_PARAM          = 0x0013,  
   ADDRESS_KIND_METADATA_ARRAYELEM      = 0x0014,  
   ADDRESS_KIND_METADATA_RETVAL         = 0x0015,  
};  
```  
  
## <a name="terms"></a>Warunki  
 ADDRESS_KIND_NATIVE  
 Adresu natywnego, reprezentowane przez [NATIVE_ADDRESS](../../../extensibility/debugger/reference/native-address.md) struktury.  
  
 ADDRESS_KIND_UNMANAGED_THIS_RELATIVE  
 Adres niezarządzanych względem `this` (`Me` w języku Visual Basic) wskaźnik i są reprezentowane przez [UNMANAGED_ADDRESS_THIS_RELATIVE](../../../extensibility/debugger/reference/unmanaged-address-this-relative.md) struktury.  
  
 ADDRESS_KIND_UNMANAGED_PHYSICAL  
 Niezarządzane adres fizyczny, reprezentowane przez [UNMANAGED_ADDRESS_PHYSICAL](../../../extensibility/debugger/reference/unmanaged-address-physical.md) struktury.  
  
 ADDRESS_KIND_METHOD  
 Metoda klasy, reprezentowane przez [METADATA_ADDRESS_METHOD](../../../extensibility/debugger/reference/metadata-address-method.md) struktury.  
  
 ADDRESS_KIND_FIELD  
 To pole klasy reprezentowane przez [METADATA_ADDRESS_FIELD](../../../extensibility/debugger/reference/metadata-address-field.md) struktury.  
  
 ADDRESS_KIND_LOCAL  
 Adres jest zmienną lokalną i jest reprezentowany przez [METADATA_ADDRESS_LOCAL](../../../extensibility/debugger/reference/metadata-address-local.md) struktury.  
  
 ADDRESS_KIND_PARAM  
 Parametr metody lub funkcji, reprezentowane przez [METADATA_ADDRESS_PARAM](../../../extensibility/debugger/reference/metadata-address-param.md) struktury.  
  
 ADDRESS_KIND_ARRAYELEM  
 Do elementu tablicy, reprezentowane przez [METADATA_ADDRESS_ARRAYELEM](../../../extensibility/debugger/reference/metadata-address-arrayelem.md) struktury.  
  
 ADDRESS_KIND_RETVAL  
 Wartość zwracana, reprezentowane przez [METADATA_ADDRESS_RETVAL](../../../extensibility/debugger/reference/metadata-address-retval.md) struktury.  
  
## <a name="remarks"></a>Uwagi  
 [Getaddress —](../../../extensibility/debugger/reference/idebugaddress-getaddress.md) metoda zwraca [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) strukturę, która zawiera sumę możliwe struktury [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) struktury. `dwKind` Pole `DEBUG_ADDRESS_UNION` struktury przechowują `ADDRESS_KIND` wartości, a w tym artykule opisano sposób interpretowania pól złożenia.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Getaddress —](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)   
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)   
 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)

