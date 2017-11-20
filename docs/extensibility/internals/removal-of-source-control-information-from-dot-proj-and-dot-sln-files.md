---
title: "Usunięcie informacji o kontroli źródła z. Proj i. Pliki SLN | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: source control plug-ins, .sln and .proj files
ms.assetid: 7b06883f-35de-41e2-9a9e-d3edba236f17
caps.latest.revision: "14"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 73ea933a7e9efc08347ea107b089101f1e5d5459
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="removal-of-source-control-information-from-proj-and-sln-files"></a>Usunięcie informacji o kontroli źródła z. Proj i. Pliki SLN
W wersji 1.2 API dodatku typu Plug-in kontroli źródła SCC informacje są przechowywane w MSSCCPRJ. Plik SCC. Zaletą MSSCCPRJ. Plik SCC jest, że informacje SCC jest nie źródła - kontrolowane, tak jak w .proj i .sln plików.  
  
## <a name="version-12-changes"></a>Zmiany w wersji 1.2  
 W źródła formantu dodatków plug-in oparte na API dodatku typu Plug-in kontroli źródła w wersji 1.1 informacje o kontroli źródła są przechowywane w projektu (.proj) i pliki rozwiązania (sln). Lokalizacja bazy danych informacji dotyczących kontroli źródła jest określona przez AuxPath i określonej lokalizacji w bazie danych jest określona przez nazwa_projektu.nazwa_modułu.nazwa_procedury. To zachowanie może spowodować problemy po gałęzi, rozwidlenia lub operacje kopiowania, ponieważ nazwa_projektu.nazwa_modułu.nazwa_procedury zazwyczaj będzie nieprawidłowe po każdej z tych operacji.  
  
 W interfejsie API dodatku typu Plug-in kontroli źródła w wersji 1.1, IDE używane ~ SAK pliki, aby wykryć, czy dodatek typu plug-in obsługiwane MSSCCPRJ. Metoda SCC przechowywania informacji o kontroli źródła. API dodatku typu Plug-in kontroli źródła w wersji 1.2 udostępnia nową funkcję wykrywania obsługę MSSCCPRJ. Plik SCC bez użycia ~ SAK pliku. Aby uzyskać więcej informacji, zobacz [eliminacja ~ pliki SAK](../../extensibility/internals/elimination-of-tilde-sak-files.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Nowości w źródła formantu wtyczka interfejsu API wersji 1.2](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)