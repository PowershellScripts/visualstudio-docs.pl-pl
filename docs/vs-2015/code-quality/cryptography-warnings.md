---
title: Ostrzeżenia dotyczące kryptografii | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: d96723ea-a293-488d-b9db-adb437e50cdd
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 4d795d9c6b6cefcf15c19867cc954ab898215a36
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49201503"
---
# <a name="cryptography-warnings"></a>Ostrzeżenia dotyczące kryptografii
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ostrzeżenia dotyczące kryptografii obsługują bezpieczniejsze biblioteki i aplikacje przy użyciu poprawnego użycia kryptografii. Ostrzeżenia te pomagają zapobiec usterkom w zabezpieczeniach w programie. Przyczynę wyłączenia któregokolwiek z tych ostrzeżeń należy wyraźnie oznaczyć w kodzie i poinformować o tym osobę odpowiedzialną za bezpieczeństwo w projekcie.  
  
|Reguła|Opis|  
|----------|-----------------|  
|[CA5350: Nie używaj słabych algorytmów kryptograficznych](../code-quality/ca5350-do-not-use-weak-cryptographic-algorithms.md)|Słabe szyfrowanie, algorytmy i funkcje wyznaczania wartości skrótu są używane obecnie do szeregu przyczyn, ale nie powinny być używane, aby zagwarantować poufność ani spójność danych, które chronią.        Ta zasada wyzwala, gdy znajdzie TripleDES, SHA1 lub RIPEMD160 algorytmów w kodzie.|  
|[CA5351: Nie używaj uszkodzonych algorytmów kryptograficznych](../code-quality/ca5351-do-not-use-broken-cryptographic-algorithms.md)|Uszkodzony kryptograficznych algorytmy nie są uznawane za bezpieczne i ich użycie powinno być zdecydowanie odradzane. Ta zasada wyzwala, gdy znajdzie algorytmu wyznaczania wartości skrótu MD5 lub DES lub RC2 algorytmów szyfrowania w kodzie.|



