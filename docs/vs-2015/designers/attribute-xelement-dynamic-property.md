---
title: Atrybut (właściwość dynamiczna XElement) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8440fc7d-b3b4-4726-8ec8-492e6af79642
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b6be72f0b40382ca8c7e9986c2d5a56e03344221
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49194847"
---
# <a name="attribute-xelement-dynamic-property"></a>Atrybut (właściwość dynamiczna XElement)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Pobiera indeksatora używane do pobierania wystąpienia atrybutu, który odpowiada określony rozwiniętej nazwy.  
  
## <a name="syntax"></a>Składnia  
  
```  
elem.Attribute[{namespaceName}attribName]  
```  
  
## <a name="property-valuereturn-value"></a>Wartość właściwości/Zwracana wartość  
 Indeksator typu `XAttribute Item(String expandedName)`. Ten indeksator rozwiniętą nazwę określonego atrybutu przyjmuje i zwraca odpowiedni <xref:System.Xml.Linq.XAttribute>, lub `null` Jeśli istnieje atrybut o określonej nazwie.  
  
## <a name="remarks"></a>Uwagi  
 Ta właściwość jest równoważna <xref:System.Xml.Linq.XElement.Attribute%2A> metody <xref:System.Xml.Linq.XElement?displayProperty=fullName> klasy.  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.Xml.Linq.XElement.Attribute%2A?displayProperty=fullName>   
 [Właściwości dynamiczne klasy XElement](../designers/xelement-class-dynamic-properties.md)   
 [Wartość](../designers/value-xattribute-dynamic-property.md)



