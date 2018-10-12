---
title: '&lt;Podpis&gt; — Element (wdrażanie ClickOnce) | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <Signature> element [ClickOnce deployment manifest]
ms.assetid: c99b07ad-e8ba-43f2-b0d6-3745e7a7c8b3
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: fe93a951fdde4a1aa4ad6d2c300551988e42c82b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49266958"
---
# <a name="ltsignaturegt-element-clickonce-deployment"></a>&lt;Podpis&gt; — Element (wdrażanie ClickOnce)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Zawiera informacje potrzebne do cyfrowego podpisywania to manifest wdrożenia.  
  
## <a name="syntax"></a>Składnia  
  
```  
  
      <Signature>   
   XML signature information   
</Signature>  
```  
  
## <a name="remarks"></a>Uwagi  
 Podpisywania manifestu wdrożenia za pomocą podpisu koperty jest opcjonalne, ale zalecane. Aby uzyskać więcej informacji na temat podpisywania XML plików Zobacz World Wide Web Consortium zalecenia, "Podpis XML składni i przetwarzanie" opisane w [ http://www.w3.org/TR/xmldsig-core/ ](http://www.w3.org/TR/xmldsig-core/).  
  
 Jeśli chcesz zarejestrować manifeście skróty należy określić dla wszystkich plików. Nie można podpisać manifest z plikami, które nie mają formę skrótu, ponieważ użytkownicy nie może sprawdzić zawartości bez haszowania plików.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie kodu pokazano `Signature` elementu w manifeście wdrożenia, używane w [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] wdrożenia.  
  
```  
<Signature xmlns="http://www.w3.org/2000/09/xmldsig#">  
  <SignedInfo>  
    <CanonicalizationMethod Algorithm=  
           "http://www.w3.org/TR/2001/REC-xml-c14n-20010315" />  
    <SignatureMethod Algorithm=  
           "http://www.w3.org/2000/09/xmldsig#rsa-sha1" />  
    <Reference URI="">  
      <Transforms>  
        <Transform Algorithm=  
           "http://www.w3.org/2000/09/xmldsig#enveloped-signature" />  
      </Transforms>  
      <DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />  
      <DigestValue>d2z5AE...</DigestValue>  
    </Reference>  
  </SignedInfo>  
  <SignatureValue>  
4PHj6SaopoLp...  
  </SignatureValue>  
  <KeyInfo>  
    <X509Data>  
      <X509Certificate>  
MIIHnTCCBoWgAwIBAgIKJY9+nwAHAAB...  
      </X509Certificate>  
    </X509Data>  
  </KeyInfo>  
</Signature>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Manifest wdrożenia ClickOnce](../deployment/clickonce-deployment-manifest.md)



