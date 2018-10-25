---
title: DISASSEMBLY_FLAGS | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- DISASSEMBLY_FLAGS
helpviewer_keywords:
- DISASSEMBLY_FLAGS enumeration
ms.assetid: c1ec5a4d-5d42-4660-932c-7348550140cb
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f6d42a7c5e9247359abfcdb4d65db5a4e0de247e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49916403"
---
# <a name="disassemblyflags"></a>DISASSEMBLY_FLAGS
Określa flagi dla dezasemblacji.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_DISASSEMBLY_FLAGS {   
   DF_DOCUMENTCHANGE     = 0x00000001,  
   DF_DISABLED           = 0x00000002,  
   DF_INSTRUCTION_ACTIVE = 0x00000004,  
   DF_DATA               = 0x00000008,  
   DF_HASSOURCE          = 0x00000010,  
   DF_DOCUMENT_CHECKSUM  = 0x00000020  
};  
typedef DWORD DISASSEMBLY_FLAGS;  
```  
  
```csharp  
public enum enum_DISASSEMBLY_FLAGS {   
   DF_DOCUMENTCHANGE     = 0x00000001,  
   DF_DISABLED           = 0x00000002,  
   DF_INSTRUCTION_ACTIVE = 0x00000004,  
   DF_DATA               = 0x00000008,  
   DF_HASSOURCE          = 0x00000010,  
   DF_DOCUMENT_CHECKSUM  = 0x00000020  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 DF_DOCUMENTCHANGE  
 Wskazuje, że ta instrukcja znajduje się w innym dokumencie niż poprzednia.  
  
 DF_DISABLED  
 Wskazuje, że ta instrukcja nie zostanie wykonany.  
  
 DF_INSTRUCTION_ACTIVE  
 Wskazuje, że tej instrukcji jest jednym z następnej instrukcji do wykonania (może istnieć więcej niż jeden).  
  
 DF_DATA  
 Wskazuje, czy tej instrukcji jest naprawdę danych (nie kodzie).  
  
 DF_HASSOURCE  
 Wskazuje, że ta instrukcja ma źródła. Niektóre instrukcje, takich jak profilowania lub wyrzucania elementów kodu, ma nie odpowiadającego jej źródła.  
  
 DF_DOCUMENT_CHECKSUM  
 Oznacza to, że `bstrDocumentUrl` pole zawiera dane sumy kontrolnej po adres URL dokumentu. Zobacz sekcję Spostrzeżenia, aby [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) struktury przechowywania danych sumy kontrolnej.  
  
## <a name="remarks"></a>Uwagi  
 Używane jako `dwFlags` członkiem [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) struktury.  
  
 Te flagi mogą być łączone przy użyciu bitowego operatora `OR`.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)