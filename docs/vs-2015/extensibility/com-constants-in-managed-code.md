---
title: Stałe modelu COM w kodzie zarządzanym | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- managed VSPackages, COM constants and macros
ms.assetid: b6663608-b049-44b0-a75b-080fdc5faafc
caps.latest.revision: 17
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 64b4ab68d973f380dcc4bc27314a69b2b605b4f1
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/16/2018
ms.locfileid: "51759471"
---
# <a name="com-constants-in-managed-code"></a>Stałe modelu COM w kodzie zarządzanym
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Framework pakietu zarządzanego (MPF) sprawia, że niektóre standardowe stałe modelu COM jest dostępne dla kodu zarządzanego. Te stałe są wymienione poniżej, dla której można się odwołać.  
  
## <a name="boolean-hresult-values"></a>Wartości HRESULT logiczna  
 <xref:Microsoft.VisualStudio.VSConstants.S_FALSE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.S_OK>  
  
## <a name="hresult-values"></a>Wartości HRESULT  
 <xref:Microsoft.VisualStudio.VSConstants.E_ABORT>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_ACCESSDENIED>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_FAIL>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_HANDLE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_INVALIDARG>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_NOINTERFACE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_NOTIMPL>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_OUTOFMEMORY>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_PENDING>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_POINTER>  
  
 <xref:Microsoft.VisualStudio.VSConstants.E_UNEXPECTED>  
  
 <xref:Microsoft.VisualStudio.VSConstants.UNDO_E_CLIENTABORT>  
  
## <a name="ole-errors"></a>Błędy OLE  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_ADVF>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_ADVISENOTSUPPORTED>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_BLANK>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_CANT_BINDTOSOURCE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_CANT_GETMONIKER>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_CANTCONVERT>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_CLASSDIFF>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_ENUM_NOMORE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_INVALIDHWND>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_INVALIDRECT>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_NOCACHE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_NOCONNECTION>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_NOSTORAGE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_NOT_INPLACEACTIVE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_NOTRUNNING>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_OLEVERB>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_PROMPTSAVECANCELLED>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_STATIC>  
  
 <xref:Microsoft.VisualStudio.VSConstants.OLE_E_WRONGCOMPOBJ>  
  
## <a name="ole-dispatch-errors"></a>Błędy wysyłania OLE  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_ARRAYISLOCKED>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_BADCALLEE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_BADINDEX>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_BADPARAMCOUNT>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_BADVARTYPE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_BUFFERTOOSMALL>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_DIVBYZERO>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_EXCEPTION>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_MEMBERNOTFOUND>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_NONAMEDARGS>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_NOTACOLLECTION>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_OVERFLOW>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_PARAMNOTFOUND>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_PARAMNOTOPTIONAL>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_TYPEMISMATCH>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_UNKNOWNINTERFACE>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_UNKNOWNLCID>  
  
 <xref:Microsoft.VisualStudio.VSConstants.DISP_E_UNKNOWNNAME>  
  
## <a name="see-also"></a>Zobacz też  
 [Obsługa błędów i wartości zwracane](../extensibility/error-handling-and-return-values.md)

