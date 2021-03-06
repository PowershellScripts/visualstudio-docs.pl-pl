---
title: Operator kontekstu debugera (C++) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.operators
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- expressions [C++], native debugger
- evaluation
- format specifiers, expressions
- context operator, in expressions
- debugging [C++], expressions
- native expression evaluator
ms.assetid: 73cc9afe-f4a4-474e-bb89-5a33fb5e570c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- cplusplus
ms.openlocfilehash: e520b40e5a2f4bf6bb7c3a7b6c2ab50930773578
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49862401"
---
# <a name="context-operator-in-the-visual-studio-debugger-c"></a>Operator kontekstu w debugerze programu Visual Studio (C++)
Operator kontekstu w języku C++ umożliwia kwalifikują się do lokalizacji punktu przerwania, nazwa zmiennej lub wyrażenia. Operator kontekstu jest przydatne w przypadku określenia nazwy w zewnętrznym zakresie, w przeciwnym razie ukryte przez nazwę lokalnego.  
  
##  <a name="BKMK_Using_context_operators_to_specify_a_symbol"></a> Składnia  
 Istnieją dwa sposoby określania kontekstu:  
  
1.  {, [*modułu*]} *wyrażenia*  
  
     Nawiasy klamrowe mogą zawierać dwóch przecinkami, a moduł (pliku wykonywalnego lub biblioteki DLL) nazwa lub pełną ścieżkę.  
  
     Na przykład, aby ustawić punkt przerwania w `SomeFunction` funkcja EXAMPLE.dll:  
  
    ```C++  
    {,,EXAMPLE.dll}SomeFunction  
    ```  
  
2.  *Moduł*! *wyrażenie*  
  
    ```C++  
    EXAMPLE.dll!SomeFunction  
    ```  
  
- *Moduł* jest nazwą modułu. Pełna ścieżka służy do rozróżniania między modułami o takiej samej nazwie.  
  
   Jeśli *modułu* ścieżka zawiera przecinek, osadzona spacja lub nawiasu klamrowego, należy użyć ścieżki w cudzysłowie, aby analizator kontekstu poprawnie rozpoznać ciągu. Znaki pojedynczego cudzysłowu są traktowane jako część nazwy pliku Windows, więc należy użyć podwójnego cudzysłowu. Na przykład  
  
  ```C++  
  {,,"a long, long, library name.dll"} g_Var  
  ```  
  
- *wyrażenie* jest dowolne prawidłowe wyrażenie C++, który jest rozpoznawany jako prawidłowego elementu docelowego, takie jak nazwy funkcji, nazwa zmiennej lub adres wskaźnika w *modułu*.  
  
  Gdy Ewaluator wyrażeń napotka symboli w wyrażeniu, wyszukiwanie symboli w następującej kolejności:  
  
1.  Zakresie leksykalnym na zewnątrz, począwszy od bieżącego bloku serię instrukcji ujęta w nawiasy klamrowe i na zewnątrz kontynuowanie otaczającym bloku. Bieżący blok jest kod, zawierający bieżącą lokalizację adres wskaźnika instrukcji.  
  
2.  Zakres funkcji. Bieżąca funkcja.  
  
3.  Zakres klasy, jeśli bieżąca lokalizacja znajduje się wewnątrz funkcji składowej C++. Zakres klasy zawiera wszystkie klasy podstawowej. Ewaluator wyrażeń przy użyciu reguł dominacji normalny.  
  
4.  Symbole globalne w bieżącego modułu.  
  
5.  Symbole publiczne w bieżącym programie.