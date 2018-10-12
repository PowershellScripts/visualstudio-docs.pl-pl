---
title: T4 Output — dyrektywa | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 03a14993-47ad-4f2e-8032-57db28d5842a
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 2e2d30c5d1dee578da14608a4e272fea09184a76
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49198526"
---
# <a name="t4-output-directive"></a>Dyrektywa T4 Output
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] szablonów tekstowych `output` dyrektywa jest używany do definiowania rozszerzenia nazwy pliku i kodowanie pliku przekształcone.  
  
 Na przykład jeśli Twoja [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] projekt zawiera plik szablonu o nazwie **MyTemplate.tt** zawierającą następujące dyrektywy:  
  
 `<#@output extension=".cs"#>`  
  
 następnie [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] wygeneruje plik o nazwie **MyTemplate.cs**  
  
 `output` Dyrektywy nie jest wymagany w szablon tekstowy (wstępnie przetworzony) czasu wykonywania. Zamiast tego aplikacja uzyskuje wygenerowany ciąg przez wywołanie metody `TextTransform()`. Aby uzyskać więcej informacji, zobacz [Generowanie tekstu czasu wykonywania przy użyciu szablonów tekstowych T4](../modeling/run-time-text-generation-with-t4-text-templates.md).  
  
## <a name="using-the-output-directive"></a>Za pomocą dane wyjściowe — dyrektywa  
  
```  
<#@ output extension=".fileNameExtension" [encoding="encoding"] #>  
```  
  
 Powinna istnieć nie więcej niż jednego `output` dyrektywy w każdym szablonie tekstu.  
  
## <a name="extension-attribute"></a>Atrybut rozszerzenia  
 Określa rozszerzenie nazwy pliku wyjściowego pliku wygenerowanego tekstu.  
  
 Wartość domyślna to **.cs**  
  
 Przykłady:  
 `<#@ output extension=".txt" #>`  
  
 `<#@ output extension=".htm" #>`  
  
 `<#@ output extension=".cs" #>`  
  
 `<#@ output extension=".vb" #>`  
  
 Dopuszczalne wartości:  
 Wszelkie nieprawidłowe rozszerzenie nazwy pliku.  
  
## <a name="encoding-attribute"></a>Atrybut kodowania  
 Określa kodowanie do użycia podczas generowania pliku wyjściowego. Na przykład:  
  
 `<#@ output encoding="utf-8"#>`  
  
 Wartość domyślna to kodowanie używane przez plik szablonu tekstu.  
  
 Dopuszczalne wartości:  
 `us-ascii`  
  
 `utf-16BE`  
  
 `utf-16`  
  
 `utf-8`  
  
 `utf-7`  
  
 `utf-32`  
  
 `0` (Ustawienie domyślne systemu)  
  
 Ogólnie rzecz biorąc, można użyć ciągu nazwasieciweb lub numer strony kodowej dowolnego kodowania zwrócony przez <xref:System.Text.Encoding.GetEncodings%2A?displayProperty=fullName>.



