---
title: "Lista źródeł — polecenie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: Debug.ListSource
helpviewer_keywords:
- Debug.ListSource command
- list source command
- ListSource command
ms.assetid: e45f08d2-f4a3-49c3-9452-aa60508e2f74
caps.latest.revision: "6"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 2f94f7bea2f4742fa975948d838e0cb01ce5e11e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="list-source-command"></a>Lista źródeł — Polecenie
Wyświetla określony wiersze kodu źródłowego.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.ListSource [/Count:number] [/Current] [/File:filename]  
[/Line:number] [/ShowLineNumbers:yes|no]  
```  
  
## <a name="switches"></a>Przełączniki  
 / Liczba:`number`  
 Opcjonalny. Określa liczbę wierszy do wyświetlenia.  
  
 / Bieżącym  
 Opcjonalny. Pokazuje bieżącego wiersza.  
  
 / Plik:`filename`  
 Opcjonalny. Ścieżka pliku do wyświetlenia. Jeśli nazwa pliku nie zostanie określony, polecenie wyświetla kod źródłowy dla wiersza bieżącej instrukcji.  
  
 / Wiersz:`number`  
 Opcjonalny. Pokazuje liczbę określonego wiersza.  
  
 / ShowLineNumbers:`yes|no`  
 Opcjonalny. Określa, czy do wyświetlania numerów wierszy.  
  
## <a name="remarks"></a>Uwagi  
  
## <a name="example"></a>Przykład  
 W tym przykładzie przedstawiono kodu źródłowego z wiersza 4 pliku Form1.vb, numery wierszy są widoczne.  
  
```  
Debug.ListSource /File:"C:\Visual Studio Projects\Form1.vb" /Line:4 /ShowLineNumbers:yes  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)