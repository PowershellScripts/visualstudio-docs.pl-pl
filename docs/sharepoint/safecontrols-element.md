---
title: "SafeControls — Element | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords: SafeControls element
ms.assetid: f5ffdbbe-cf85-4e5a-9d39-3cd4462f2a0e
caps.latest.revision: "11"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f1588c7f20b0187557a1bfc993ba57657cbc52cd
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="safecontrols-element"></a>SafeControls — Element
  Reprezentuje kolekcję ASPX kontrolek i składników Web Part, które są wyznaczone jako bezpieczne dla każdego użytkownika uzyskiwać dostęp do dowolnej strony ASPX w witrynie programu SharePoint.  
  
## <a name="syntax"></a>Składnia  
  
```  
<SafeControls>  
  <SafeControl.../>  
</SafeControls>  
```  
  
## <a name="attributes-and-elements"></a>Atrybuty i elementy  
 W poniższych sekcjach opisano atrybuty, elementy podrzędne i elementy nadrzędne.  
  
### <a name="attributes"></a>Atrybuty  
 Brak.  
  
### <a name="child-elements"></a>Elementy podrzędne  
  
|Element|Opis|  
|-------------|-----------------|  
|[SafeControl —](../sharepoint/safecontrol-element.md)|Element opcjonalny.<br /><br /> Reprezentuje kontrolki ASPX lub składnik Web Part jest oznaczony jako bezpieczny dla każdego użytkownika uzyskiwać dostęp do dowolnej strony ASPX w witrynie programu SharePoint.|  
  
### <a name="parent-elements"></a>Elementy nadrzędne  
  
|Element|Opis|  
|-------------|-----------------|  
|[ProjectItem](../sharepoint/projectitem-element.md)|Reprezentuje element projektu programu SharePoint. Jest to wymaganego głównego elementu pliku .spdata —.|  
  
## <a name="remarks"></a>Uwagi  
 Aby uzyskać więcej informacji na temat bezpiecznych formantów, zobacz [dostarczanie pakowania i informacje o wdrożeniu w elementach projektu](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).  
  
## <a name="element-information"></a>Informacje o elementach  
  
|||  
|-|-|  
|**Namespace**|http://schemas.microsoft.com/VisualStudio/2010/SharePointTools/SharePointProjectItemModel|  
|**Nazwa schematu**|Schemat elementu projektu SharePoint|  
|**Sprawdzanie poprawności pliku**|ProjectItemModelSchema.xsd|  
|**Może być pusta.**|Nie|  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do schematu elementu projektu SharePoint](../sharepoint/sharepoint-project-item-schema-reference.md)   
 [Opakowanie i informacje o wdrożeniu w elementach projektu](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)  
  
  