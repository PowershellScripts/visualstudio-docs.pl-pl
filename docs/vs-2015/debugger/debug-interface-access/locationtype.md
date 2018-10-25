---
title: Locationtype — | Dokumentacja firmy Microsoft
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
- LocationType enumeration
ms.assetid: d3e1eedc-bfd3-4c91-881b-d69565138d0f
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3d1c9ff2dce8918d5bcc75c8504e5af133ea5e43
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49836161"
---
# <a name="locationtype"></a>LocationType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Wskazuje rodzaj informacji o lokalizacji zawarte w symbolu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
enum LocationType {   
   LocIsNull,  
   LocIsStatic,  
   LocIsTLS,  
   LocIsRegRel,  
   LocIsThisRel,  
   LocIsEnregistered,  
   LocIsBitField,  
   LocIsSlot,  
   LocIsIlRel,  
   LocInMetaData,  
   LocIsConstant,  
   LocTypeMax  
};  
```  
  
## <a name="elements"></a>Elementy  
 `LocIsNull`  
 Informacje o lokalizacji jest niedostępny.  
  
 `LocIsStatic`  
 Lokalizacja jest statyczne.  
  
 `LocIsTLS`  
 Lokalizacja znajduje się w pamięci lokalnej wątku.  
  
 `LocIsRegRel`  
 Lokalizacja jest powiązane z wątkiem rejestru.  
  
 `LocIsThisRel`  
 Lokalizacja jest `this`— względna.  
  
 `LocIsEnregistered`  
 Lokalizacja znajduje się w rejestrze.  
  
 `LocIsBitField`  
 Lokalizacja jest polem bitowym.  
  
 `LocIsSlot`  
 Lokalizacja jest miejsce Microsoft Intermediate Language (MSIL).  
  
 `LocIsIlRel`  
 Lokalizacja jest powiązane z wątkiem MSIL.  
  
 `LocInMetaData`  
 Lokalizacja znajduje się w metadanych.  
  
 `LocIsConstant`  
 Lokalizacja jest wartością stałą.  
  
 `LocTypeMax`  
 Liczba typów lokalizacji, w tym wyliczeniu.  
  
## <a name="remarks"></a>Uwagi  
 Właściwości dostępne dla [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) interfejsu są zależne od lokalizacji symbolu w pliku obrazu. Aby uzyskać więcej informacji, zobacz [lokalizacje symboli](../../debugger/debug-interface-access/symbol-locations.md).  
  
 Wartości w tym wyliczeniu są zwracane przez wywołanie [idiasymbol::get_locationtype —](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: cvconst.h  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia i struktury](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)   
 [Idiasymbol::get_locationtype —](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md)   
 [Lokalizacje symboli](../../debugger/debug-interface-access/symbol-locations.md)



