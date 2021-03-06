---
title: FRAMEINFO | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- FRAMEINFO
helpviewer_keywords:
- FRAMEINFO structure
ms.assetid: 95001b89-dddb-45bb-889d-8327994e38a5
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1ed3ddbbbffb6e1a92e4c5038fad8f901ecf303e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49834035"
---
# <a name="frameinfo"></a>FRAMEINFO
W tym artykule opisano ramki stosu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct tagFRAMEINFO {   
   FRAMEINFO_FLAGS    m_dwValidFields;  
   BSTR               m_bstrFuncName;  
   BSTR               m_bstrReturnType;  
   BSTR               m_bstrArgs;  
   BSTR               m_bstrLanguage;  
   BSTR               m_bstrModule;  
   UINT64             m_addrMin;  
   UINT64             m_addrMax;  
   IDebugStackFrame2* m_pFrame;  
   IDebugModule2*     m_pModule;  
   BOOL               m_fHasDebugInfo;  
   BOOL               m_fStaleCode;  
   BOOL               m_fAnnotatedFrame;  
} FRAMEINFO;  
```  
  
```csharp  
public struct FRAMEINFO {   
   public uint              m_dwValidFields;  
   public string            m_bstrFuncName;  
   public string            m_bstrReturnType;  
   public string            m_bstrArgs;  
   public string            m_bstrLanguage;  
   public string            m_bstrModule;  
   public ulong             m_addrMin;  
   public ulong             m_addrMax;  
   public IDebugStackFrame2 m_pFrame;  
   public IDebugModule2     m_pModule;  
   public int               m_fHasDebugInfo;  
   public int               m_fStaleCode;  
   public int               m_fAnnotatedFrame;  
} FRAMEINFO;  
```  
  
## <a name="members"></a>Elementy członkowskie  
 m_dwValidFields  
 Kombinacja flag z [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md) wyliczenia, która określa, które pola są wypełniane.  
  
 m_bstrFuncName  
 Nazwa funkcji skojarzone z ramki stosu.  
  
 m_bstrReturnType  
 Zwracany typ ramki stosu.  
  
 m_bstrArgs  
 Argumenty do funkcji skojarzonych z ramki stosu.  
  
 m_bstrLanguage  
 Język, w którym funkcja jest zaimplementowana.  
  
 m_bstrModule  
 Nazwa modułu ramki stosu.  
  
 m_addrMin  
 Adres minimalny stos fizycznych.  
  
 m_addrMAX  
 Adres maksymalnej stosu fizycznych.  
  
 m_pFrame  
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) obiekt, który reprezentuje tej ramki stosu.  
  
 m_pFrame  
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) obiekt, który reprezentuje moduł, który zawiera tej ramki stosu.  
  
 m_fHasDebugInfo  
 Niezerowa Koniunkcja (`TRUE`) Jeśli informacje o debugowaniu istnieje w podanej ramce.  
  
 m_fHasDebugInfo  
 Niezerowa Koniunkcja (`TRUE`) Jeśli ramka stosu jest skojarzony z kodem, który nie jest już prawidłowy.  
  
 m_fHasDebugInfo  
 Niezerowa Koniunkcja (`TRUE`), jeśli ramka stosu jest oznaczona przez Menedżer debugowania sesji (SDM).  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest przekazywany do [GetInfo](../../../extensibility/debugger/reference/idebugstackframe2-getinfo.md) metodę, aby wypełnić. Ta struktura również znajduje się na liście, który jest zawarty w [IEnumDebugFrameInfo2](../../../extensibility/debugger/reference/ienumdebugframeinfo2.md) interfejs, który z kolei jest zwracany z wywołania [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugstackframe2-getinfo.md)   
 [IEnumDebugFrameInfo2](../../../extensibility/debugger/reference/ienumdebugframeinfo2.md)   
 [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)