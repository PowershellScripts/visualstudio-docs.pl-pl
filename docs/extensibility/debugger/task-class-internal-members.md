---
title: "Task — klasa — wewnętrzne elementy członkowskie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- debug engines, Task class [.NET Framework]
- Task class [.NET Framework debug engines]
ms.assetid: 28e47c3b-9323-424a-80ac-6cc3bf19e09b
caps.latest.revision: "14"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5937d37cfed89ee7f10779f764b8d78d370eb362
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="task-class---internal-members"></a>Task — klasa — wewnętrzne elementy członkowskie
W tym temacie opisano wewnętrzne elementy członkowskie <xref:System.Threading.Tasks.Task?displayProperty=fullName> klasy, które pomagają implementować niestandardowe debugera. Aby uzyskać ogólne informacje o tej klasy, zobacz <xref:System.Threading.Tasks.Task> temat referencyjny.  
  
 **Namespace:**<xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Zestaw:** mscorlib (w bibliotece mscorlib.dll)  
  
 Ponieważ nie można uzyskać dostępu do tych wewnętrznych elementów członkowskich z programu .NET Framework, następującej składni podano języka wspólnego pośredniego (CIL).  
  
## <a name="syntax"></a>Składnia  
  
```  
.class public auto ansi System.Threading.Tasks.Task  
       extends System.Object  
       implements System.Threading.IThreadPoolWorkItem,  
                  System.IAsyncResult,  
                  System.IDisposable,  
                  System.Threading.ICancelableOperation  
```  
  
## <a name="members"></a>Elementy członkowskie  
  
### <a name="methods"></a>Metody  
  
|Nazwa|Opis|  
|----------|-----------------|  
|[SetNotificationForWaitCompletion — metoda](../../extensibility/debugger/setnotificationforwaitcompletion-method.md)|Ustawia lub czyści stanu TASK_STATE_WAIT_COMPLETION_NOTIFICATION.|  
|[NotifyDebuggerOfWaitCompletion — metoda](../../extensibility/debugger/notifydebuggerofwaitcompletion-method.md)|Metoda symbolu zastępczego używany jako obiekt docelowy punkt przerwania przez debuger.|  
  
### <a name="fields"></a>Pola  
  
|Nazwa|Opis|  
|----------|-----------------|  
|[m_action](../../extensibility/debugger/m-action-field.md)|Delegat, który reprezentuje kod do wykonania w <xref:System.Threading.Tasks.Task> obiektu.|  
|[m_contingentProperties](../../extensibility/debugger/m-contingentproperties-field.md)|Przechowuje dodatkowe właściwości <xref:System.Threading.Tasks.Task> obiektu.|  
|[m_parent](../../extensibility/debugger/m-parent-field.md)|Pole zapasowe dla <xref:System.Threading.Tasks.Task?displayProperty=fullName> nadrzędnego właściwości.|  
|[m_stateFlags](../../extensibility/debugger/m-stateflags-field.md)|Przechowuje informacje o bieżącym stanie <xref:System.Threading.Tasks.Task> obiektu.|  
|[m_stateObject](../../extensibility/debugger/m-stateobject-field.md)|Obiekt, który reprezentuje dane, które będą używane przez akcję.|  
|[m_taskId](../../extensibility/debugger/m-taskid-field.md)|Pole zapasowe dla <xref:System.Threading.Tasks.Task.Id%2A?displayProperty=fullName> właściwości.|  
|[s_taskIdCounter](../../extensibility/debugger/s-taskidcounter-field.md)|Identyfikator następnego dostępne <xref:System.Threading.Tasks.Task> obiektu.|  
|[TASK_STATE_CANCELED](../../extensibility/debugger/task-state-canceled-field.md)|Wskazuje, że zadanie zostało anulowane przed osiągnięciem uruchomiona lub jej anulowania potwierdzone i zakończona bez wyjątku zadania.|  
|[TASK_STATE_EXECUTED](../../extensibility/debugger/task-state-executed-field.md)|Wskazuje, że zadanie jest uruchomione.|  
|[TASK_STATE_FAULTED](../../extensibility/debugger/task-state-faulted-field.md)|Wskazuje, że zadanie zakończyło się z powodu nieobsługiwanego wyjątku.|  
|[TASK_STATE_RAN_TO_COMPLETION](../../extensibility/debugger/task-state-ran-to-completion-field.md)|Wskazuje, że zadań pomyślnie ukończył wykonywanie sekwencji.|  
|[TASK_STATE_WAITING_ON_CHILDREN](../../extensibility/debugger/task-state-waiting-on-children-field.md)|Wskazuje, że zadanie zakończono wykonywanie swojego delegata i niejawnie oczekuje na zakończenie zadań podrzędnych dołączonych.|  
  
## <a name="remarks"></a>Uwagi  
 Następujące metody wewnętrznej są przydatne do aparatu debugera, ponieważ ich oznaczenie wejścia do <xref:System.Threading.Tasks.Task> wykonanie kodu:  
  
-   `Execute`  
  
-   `ExecuteEntry`  
  
-   `ExecuteWithThreadLocal`  
  
-   `Finish`  
  
-   `InnerInvoke`  
  
-   `InternalWait`  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.Threading.Tasks.Task?displayProperty=fullName>   
 [Wewnętrzne rozszerzenia równoległe dla programu .NET Framework](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)