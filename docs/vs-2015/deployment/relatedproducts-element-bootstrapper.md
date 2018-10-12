---
title: '&lt;RelatedProducts&gt; — Element (program inicjujący) | Dokumentacja firmy Microsoft'
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
- MSBuild.GenerateBootstrapper.MissingDependency
- MSBuild.GenerateBootstrapper.DuplicateItems
- MSBuild.GenerateBootstrapper.IncludedProductIncluded
- MSBuild.GenerateBootstrapper.DependencyNotFound
- MSBuild.GenerateBootstrapper.PackageFileNotFound
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- <RelatedProducts> element [bootstrapper]
ms.assetid: bf152712-4c1e-48bd-9b7f-311cf0fdb832
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: c78aa559bf64b110909134426c676f302ca5fe04
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49296299"
---
# <a name="ltrelatedproductsgt-element-bootstrapper"></a>&lt;RelatedProducts&gt; — Element (program inicjujący)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`RelatedProducts` Element definiuje innych produktów, które zależą od lub znajdują się w bieżącym produkcie.  
  
## <a name="syntax"></a>Składnia  
  
```  
<RelatedProducts>  
    <DependsOnProduct  
        Code  
    />  
    <EitherProducts>  
        <DependsOnProduct  
            Code  
        />  
    </EitherProducts>  
    <IncludesProduct  
        Code  
    />  
</RelatedProducts>  
```  
  
## <a name="elements-and-attributes"></a>Atrybuty i elementy  
 `RelatedProducts` Element jest elementem podrzędnym `Product` elementu. Go nie ma żadnych atrybutów.  
  
## <a name="dependsonproduct"></a>DependsOnProduct  
 `DependsOnProduct` Element oznacza, że bieżącego produktu zależy od wskazanego produktu i że wskazanego produktu powinien zostać zainstalowany przed bieżącym. Jest elementem podrzędnym `RelatedProducts` elementu. A `RelatedProducts` element może mieć co najmniej jeden `DependsOnProduct` elementów.  
  
 `DependsOnProduct` ma następujący atrybut.  
  
|Atrybut|Opis|  
|---------------|-----------------|  
|`Code`|Nazwa kodu produktu uwzględniona, określony przez `ProductCode` atrybutu `Product` elementu. Aby uzyskać więcej informacji, zobacz [ \<produktu > Element](../deployment/product-element-bootstrapper.md).|  
  
## <a name="eitherproducts"></a>EitherProducts  
 `EitherProducts` Element definiuje zero lub więcej `DependsOnProduct` elementów, a nie ma żadnych atrybutów. Co najmniej jeden `DependsOnProduct` w tym zestawie musi zostać zainstalowany przed bieżącego produktu. A `RelatedProducts` element może mieć zero lub więcej `EitherProducts` elementów.  
  
## <a name="includesproduct"></a>IncludesProduct  
 `IncludesProduct` Element oznacza znajduje się w bieżącej instalacji produktu i nie wymagają oddzielnej instalacji. Jest elementem podrzędnym `RelatedProducts` elementu. A `RelatedProducts` element może mieć co najmniej jeden `IncludesProduct` elementów.  
  
 `IncludesProduct` ma następujący atrybut.  
  
|Atrybut|Opis|  
|---------------|-----------------|  
|`Code`|Nazwa kodu produktu uwzględniona, określony przez `ProductCode` atrybutu `Product` elementu. Aby uzyskać więcej informacji, zobacz [ \<produktu > Element](../deployment/product-element-bootstrapper.md).|  
  
## <a name="example"></a>Przykład  
 Poniższy przykład kodu Określa, że Microsoft Installer został zainstalowany z [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)]i w związku z tym nie wymagają oddzielnej instalacji.  
  
```  
<RelatedProducts>  
    <IncludesProduct Code="Microsoft.Windows.Installer.2.0" />  
</RelatedProducts>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [\<Produktu > Element](../deployment/product-element-bootstrapper.md)



