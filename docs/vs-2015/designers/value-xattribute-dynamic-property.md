---
title: Wartość (właściwość dynamiczna XAttribute) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
api_name:
- XAttribute.Value
api_type:
- Assembly
ms.assetid: 019733d2-e050-4120-b537-831cd3fc008e
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: bd9ea1fa163980a39bcd9981b9e1d757d72fcb6a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49229154"
---
# <a name="value-xattribute-dynamic-property"></a>Wartość (właściwość dynamiczna XAttribute)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Pobiera lub ustawia wartość atrybutu XML.  
  
## <a name="syntax"></a>Składnia  
  
```  
attrib.Value   
```  
  
## <a name="property-valuereturn-value"></a>Wartość właściwości/Zwracana wartość  
 Element <xref:System.String> zawierający wartość tego atrybutu.  
  
## <a name="exceptions"></a>Wyjątki  
  
|Typ wyjątku|Warunek|  
|--------------------|---------------|  
|<xref:System.ArgumentNullException>|Podczas ustawiania, `value` jest `null`.|  
  
## <a name="remarks"></a>Uwagi  
 Ta właściwość jest równoważna <xref:System.Xml.Linq.XAttribute.Value%2A> właściwość <xref:System.Xml.Linq.XAttribute?displayProperty=fullName> klasy, ale ta właściwość dynamiczna obsługuje również powiadomienia o zmianach.  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.Xml.Linq.XAttribute.Value%2A?displayProperty=fullName>   
 [Właściwości dynamiczne klasy XAttribute](../designers/xattribute-class-dynamic-properties.md)   
 [Atrybut](../designers/attribute-xelement-dynamic-property.md)



