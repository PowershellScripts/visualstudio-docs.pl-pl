---
title: "Porady: Określanie lokalizacji plików symboli z wiersza polecenia | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 8aa067bb-e8bf-4081-aff0-cfbcf65934a0
caps.latest.revision: "11"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d4d0e04c439f5e677cbbbdcfcf560ec976c6257b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-specify-symbol-file-locations-from-the-command-line"></a>Porady: określanie lokalizacji plików symboli z wiersza polecenia
Aby wyświetlić informacje dotyczące symboli, takich jak funkcja nazwy i numery wierszy, narzędzie wiersza polecenia VSPerfReport wymaga dostępu do plików symboli (.pdb) PROFILOWANEGO składników i plików systemu Windows. Pliki symboli są tworzone, gdy składnik jest kompilowany. Aby uzyskać więcej informacji, zobacz [VSPerfReport](../profiling/vsperfreport.md). VSPerfReport automatycznie wyszukuje następujących lokalizacji plików symboli:  
  
-   Ścieżek określonych w **/SymbolPath** opcji lub **_NT_SYMBOL_PATH** zmiennej środowiskowej.  
  
-   Gdy składnik został skompilowany dokładne ścieżka lokalna.  
  
-   Katalog zawierający plik danych profilowania (Vsp lub vsps).  
  
 Firma Microsoft udostępnia .pdb, pliki dla wielu jego produktów w trybie online na serwerze symboli. Jeśli komputer, którego używasz do raportowania jest połączony z Internetem, VSPerfReport łączy się z serwera symboli online automatycznie wyszukiwanie informacji o symbolach i zapisać pliki w lokalnym magazynie.  
  
 Można określić lokalizacji plików symboli i magazynu serwera symboli firmy Microsoft, w następujący sposób:  
  
-   Ustaw **_NT_SYMBOL_PATH** zmiennej środowiskowej.  
  
-   Dodaj **/SymbolPath** opcji wiersza polecenia VSPerfReport.  
  
 Można również użyć obu tych metod.  
  
> [!NOTE]
>  Jeśli [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] jest zainstalowany na komputerze lokalnym, lokalizację dla plików symboli Windows prawdopodobnie określono już. Aby uzyskać więcej informacji, zobacz [porady: odwołanie do systemu Windows — informacje o symbolach](../profiling/how-to-reference-windows-symbol-information.md). Nadal muszą skonfigurować VSPerfReport, aby użyć lokalizacji i serwera, zgodnie z opisem w dalszej części tego tematu.  
  
## <a name="specifying-windows-symbol-files"></a>Określanie plików symboli z systemem Windows  
  
#### <a name="to-configure-the-use-of-the-windows-symbol-server"></a>Umożliwia skonfigurowanie użycia systemu Windows Server — symbol  
  
1.  Jeśli to konieczne, Utwórz katalog do przechowywania plików symboli lokalnie.  
  
2.  Użyj następującej składni, aby ustawić **_NT_SYMBOL_PATH** zmiennej środowiskowej lub opcji /SymbolPath VSPerfReport:  
  
     **SRV\***  *LocalStore*  **\*http://msdl.microsoft.com/downloads/symbols**  
  
     gdzie *LocalStore* jest ścieżką katalogu lokalnego, który został utworzony.  
  
## <a name="specifying-component-symbol-files"></a>Określanie plików symboli składnika  
 Profilowanie narzędzia wyszukuje pliki the.pdb składników, które mają być profil w ich oryginalnych lokalizacji, które są przechowywane w składnikach lub w folderze, który zawiera plik danych profilowania. Można określić innych lokalizacji do wyszukiwania przez dodanie jedną lub więcej ścieżek do **_NT_SYMBOL_PATH** lub **/SymbolPath** opcji. Ścieżki średnikami.  
  
## <a name="example"></a>Przykład  
 Następujące zestawy wiersza polecenia **_NT_SYMBOL_PATH** zmienna środowiskowa systemu Windows server symboli i katalogu lokalnego do **C:\Symbols**.  
  
 **Ustaw _NT_SYMBOL_PATH = srv\*C:\symbols\*http://msdl.microsoft.com/downloads/symbols**  
  
 Następujące polecenie w wierszu polecenia VSPerfReport dodaje C:\Projects\Symbols katalog do ścieżki wyszukiwania za pomocą **/SymbolPath** opcji.  
  
 **VSPerfReport***moja_aplikacja* **.exe /SymbolPath:C:\Projects\Symbols /summary:all** 