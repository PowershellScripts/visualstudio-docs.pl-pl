---
title: '&lt;Opis&gt; — Element (wdrażanie ClickOnce) | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#description
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <description> element [ClickOnce deployment manifest]
ms.assetid: 18f6919e-a3ab-4942-a57d-167fabfac44e
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 8ddba6356ab051dbad27e55eefd53a517b47a21a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49224773"
---
# <a name="ltdescriptiongt-element-clickonce-deployment"></a>&lt;Opis&gt; — Element (wdrażanie ClickOnce)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Określa informacje o aplikacji, które pozwala utworzyć obecności powłoki i **apletu Dodaj lub usuń programy** w Panelu sterowania.  
  
## <a name="syntax"></a>Składnia  
  
```  
  
      <description   
   publisher   
   product  
   suiteName  
   supportUrl  
/>  
```  
  
## <a name="elements-and-attributes"></a>Atrybuty i elementy  
 `description` Element jest wymagany i znajduje się w `urn:schemas-microsoft-com:asm.v1` przestrzeni nazw. Go nie zawiera żadnych elementów podrzędnych i ma następujące atrybuty.  
  
|Atrybut|Opis|  
|---------------|-----------------|  
|`publisher`|Wymagane. Określa nazwę firmy, używane do umieszczenia ikony w Windows **Start** menu i **apletu Dodaj lub usuń programy** w Panelu sterowania, gdy wdrożenie jest skonfigurowane do instalacji.|  
|`product`|Wymagane. Identyfikuje Pełna nazwa produktu. Używane jako tytuł na ikonę zainstalowane w Windows **Start** menu.|  
|`suiteName`|Opcjonalna. Identyfikuje podfolder w `publisher` folderu w Windows **Start** menu.|  
|`supportUrl`|Opcjonalna. Określa adres URL pomocy technicznej, która jest wyświetlana w **apletu Dodaj lub usuń programy** w Panelu sterowania. Skrót do tego adresu URL tworzona jest również obsługę aplikacji w Windows **Start** menu, gdy wdrożenie jest skonfigurowane do instalacji.|  
  
## <a name="remarks"></a>Uwagi  
 Opis elementu jest wymagany we wszystkich konfiguracjach wdrażania.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie kodu pokazano `description` element [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] manifest wdrożenia. Ten przykład kodu jest częścią większego przykładu przewidzianego dla [Manifest wdrażania ClickOnce](../deployment/clickonce-deployment-manifest.md) tematu.  
  
```  
<description   
  asmv2:publisher="My Company Name"  
  asmv2:product="My Application"  
  xmlns="urn:schemas-microsoft-com:asm.v1" />  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Manifest wdrożenia ClickOnce](../deployment/clickonce-deployment-manifest.md)



