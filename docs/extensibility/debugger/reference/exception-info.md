---
title: EXCEPTION_INFO | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- EXCEPTION_INFO
helpviewer_keywords:
- EXCEPTION_INFO structure
ms.assetid: d046957a-b97d-420b-b46b-c67cbaef709e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 4bbefc02a05d03dc966c05941ca08c05cce0a5a5
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49947917"
---
# <a name="exceptioninfo"></a>EXCEPTION_INFO
W tym artykule opisano, wystąpi wyjątek lub błąd czasu wykonywania zgłoszony przez debugowanego programu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct tagEXCEPTION_INFO {   
   IDebugProgram2* pProgram;  
   BSTR            bstrProgramName;  
   BSTR            bstrExceptionName;  
   DWORD           dwCode;  
   EXCEPTION_STATE dwState;  
   GUID            guidType;  
} EXCEPTION_INFO;  
```  
  
```csharp  
public struct EXCEPTION_INFO {   
   public IDebugProgram2 pProgram;  
   public string         bstrProgramName;  
   public string         bstrExceptionName;  
   public uint           dwCode;  
   public uint           dwState;  
   public Guid           guidType;  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 pProgram  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) obiekt, który reprezentuje program, w którym wyjątek wystąpił.  
  
 bstrProgramName  
 Nazwa programu, w którym wyjątek wystąpił.  
  
 bstrExceptionName  
 Nazwa wyjątku.  
  
 dwCode  
 Kod identyfikacyjny dla błędu lub wyjątku czasu wykonywania.  
  
 dwState  
 Wartość z zakresu od [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md) wyliczenie, które definiuje stan wyjątku.  
  
 guidType  
 Identyfikator GUID języka, każdy `guidLang` lub `guidEng`.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest przekazywany jako parametr do [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md) i [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md) metody. Ta struktura jest również przekazywany do [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) metodę, aby wypełnić.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)   
 [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md)   
 [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)