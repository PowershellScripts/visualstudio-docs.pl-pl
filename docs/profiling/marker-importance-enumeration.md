---
title: "marker_importance — wyliczenie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: cvmarkersobj/Concurrency::diagnostic::marker_importance
helpviewer_keywords: Concurrency::diagnostic::marker_importance enumeration
ms.assetid: d5524ea0-0227-4d8e-9122-332291042df5
caps.latest.revision: "3"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d09138f90b94d3b37c4a20fbe53f311fa29a36e9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="markerimportance-enumeration"></a>marker_importance — Wyliczenie
Reprezentuje poziom ważności znaczników wizualizatora współbieżności.  
  
## <a name="syntax"></a>Składnia  
  
```  
enum marker_importance;  
```  
  
## <a name="members"></a>Elementy członkowskie  
  
### <a name="values"></a>Wartości  
  
|Nazwa|Opis|  
|----------|-----------------|  
|`critical_importance`|Określa, czy znacznika ma kluczowe znaczenie.|  
|`high_importance`|Określa, czy znacznika ma wysokiej ważności.|  
|`low_importance`|Określa, czy znacznika ma niskiej ważności.|  
|`normal_importance`|Określa, czy znacznika ma znaczenie normalnego.|  
  
## <a name="requirements"></a>Wymagania  
 **Nagłówek:** cvmarkersobj.h  
  
 **Namespace:** CONCURRENCY::Diagnostic —  
  
## <a name="see-also"></a>Zobacz też  
 [Namespace diagnostycznych](../profiling/diagnostic-namespace.md)