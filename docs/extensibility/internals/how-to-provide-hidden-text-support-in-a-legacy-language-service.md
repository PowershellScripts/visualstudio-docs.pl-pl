---
title: "Porady: zapewniają obsługę tekstu ukrytego w usłudze języka starszych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- hidden text, supporting
- editors [Visual Studio SDK], hidden text
- language services, implementing hidden text regions
ms.assetid: 1c1dce9f-bbe2-4fc3-a736-5f78a237f4cc
caps.latest.revision: "21"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f7aab5978d2fc5f7bee82b097ed61a9603d7e198
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-provide-hidden-text-support-in-a-legacy-language-service"></a>Porady: zapewniają obsługę tekstu ukrytego w starsza wersja usługi języka
Można utworzyć regiony tekstu ukrytego oprócz konspektu regionów. Regiony tekstu ukrytego mogą być kontrolowane przez klienta lub kontrolowanych przez Edytor i są używane do ukrywania całkowicie obszaru tekstu. Edytor wyświetla ukryte regionu jako poziome linie. Na przykład jest widok tylko skrypt w edytorze HTML.  
  
## <a name="procedure"></a>Procedura  
  
#### <a name="to-implement-a-hidden-text-region"></a>Aby zaimplementować region tekstu ukrytego  
  
1.  Wywołanie `QueryService` dla <xref:Microsoft.VisualStudio.TextManager.Interop.SVsTextManager>.  
  
     Zwraca wskaźnik do <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager>.  
  
2.  Wywołanie <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.GetHiddenTextSession%2A>, przekazując wskaźnika buforu danego tekstu. Określa, czy sesja ukryty tekst, który jest już istnieje dla buforu.  
  
3.  Jeśli już istnieje, a następnie trzeba utworzyć jedną i wskaźnika do istniejącej <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> obiekt jest zwracany. This, wskaźnik umożliwia wyliczyć i utworzyć regiony tekstu ukrytego. W przeciwnym razie wywołać <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.CreateHiddenTextSession%2A> do utworzenia sesji ukrytego tekstu dla buforu.  
  
     Wskaźnik do <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> obiekt jest zwracany.  
  
    > [!NOTE]
    >  Podczas wywoływania `CreateHiddenTextSession`, można określić klienta tekstu ukrytego (czyli <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextClient>). Klient tekstu ukrytego sygnalizuje tekstu ukrytego lub zwijania jest rozwinięte lub zwinięte przez użytkownika.  
  
4.  Wywołanie <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession.AddHiddenRegions%2A> można dodać jeden lub więcej nowych konspektu regionów jednocześnie, określając następujące informacje w `reHidReg` (<xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion>) parametr:  
  
    1.  Określ wartość `hrtConcealed` w `iType` członkiem <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> struktury, aby wskazać, tworzysz ukryte region, a nie region konspektu.  
  
        > [!NOTE]
        >  Jeśli ukryte regiony są ukryte, Edytor automatycznie wyświetla linie wokół ukryte obszary wskazanie ich obecności.  
  
    2.  Określ, czy region jest kontrolowane przez klienta lub kontrolowanych przez Edytor w `dwBehavior` członkami <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> struktury. Inteligentne implementacji zwijania może zawierać zarówno konspektu kontrolowane przez Edytor i klienta i regiony tekstu ukrytego.