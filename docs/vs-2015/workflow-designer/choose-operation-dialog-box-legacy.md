---
title: Wybierz operację, okno dialogowe (starsza wersja) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Workflow.Activities.Design.OperationPickerDialog.UI
ms.assetid: bc3ec902-7797-494e-af48-e70c97eb6779
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 75b553bd79936db7b6d8aa2f8fe361650d4ef03e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49189635"
---
# <a name="choose-operation-dialog-box-legacy"></a>Wybieranie operacji, okno dialogowe (starsza wersja)
W tym temacie opisano sposób użycia **wybierz operację** okno dialogowe w starszej wersji [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Użyj starszego [!INCLUDE[wfd2](../includes/wfd2-md.md)] konieczność docelowy: [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] lub [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 **Wybierz operację** okno dialogowe służy do wybierania operacji do skojarzenia z <xref:System.Workflow.Activities.ReceiveActivity> działania lub <xref:System.Workflow.Activities.SendActivity> działania. Aby uzyskać więcej informacji o korzystaniu z tego okna dialogowego z tych działań, zobacz [porady: Implementowanie operacji kontraktu usługi WCF (starsza wersja)](../workflow-designer/how-to-implement-a-windows-communication-foundation-contract-operation-legacy.md) i [porady: wywoływanie operacji kontraktu usługi WCF (starsza wersja)](../workflow-designer/how-to-invoke-a-windows-communication-foundation-contract-operation-legacy.md).  
  
 W poniższej tabeli opisano elementy interfejsu użytkownika **wybierz operację** okno dialogowe.  
  
|Element interfejsu użytkownika|Opis|  
|----------------|-----------------|  
|**Dodaj umowy**|Tworzy nową umowę. Można zdefiniować nowe operacje w niniejszej Umowie. (To jest używana z <xref:System.Workflow.Activities.ReceiveActivity> jedynie.)|  
|**Dodawanie operacji**|Dodaje nowe operacje do nowego kontraktu, który został utworzony w **wybierz operację** okno dialogowe. **Uwaga:** nowe operacje zostaną dodane tylko do umów, które zostały utworzone za pomocą **wybierz operację** okno dialogowe. <br /><br /> (To jest używana z <xref:System.Workflow.Activities.ReceiveActivity> jedynie.)|  
|**Importuj...**|Importuje uprzednio zdefiniowany kontraktu i umożliwia wybranie operacji z tej Umowy.|  
|**Nazwa operacji**|Nazwa aktualnie wybranej operacji. To pole tekstowe jest dostępny do edycji, tylko wtedy, gdy utworzono operację za pośrednictwem **wybierz operację** okno dialogowe.|  
|**Parametry**|Karta zawierającego definicje parametrów dla aktualnie wybranej operacji. **Uwaga:** definicjami parametrów można zmienić tylko wtedy, gdy utworzono operację za pośrednictwem **wybierz operację** okno dialogowe.|  
|**Właściwości**|Karty zawierające <xref:System.Net.Security.ProtectionLevel> ustawień komunikatów wysyłanych między klientem a usługą. **Uwaga:** na tej karcie jest włączona tylko wtedy, gdy utworzono operację za pośrednictwem **wybierz operację** okno dialogowe.|  
|**Uprawnienia**|Karty zawierające <xref:System.Workflow.Activities.OperationInfoBase.PrincipalPermissionName%2A> i <xref:System.Workflow.Activities.OperationInfoBase.PrincipalPermissionRole%2A> właściwości użytkowników, którzy mogą wywołać tę operację. Na przykład, jeśli tylko użytkownicy z grupy Administratorzy mieli możliwość wywołania tej operacji, następnie należy napisać "Administratorzy" **roli** pola tekstowego.<br /><br /> Ta karta jest włączony dla obu operacji, została utworzona za pośrednictwem **ChooseOperation** okno dialogowe i operacje, które zostały zaimportowane przy użyciu **importu** przycisku.|  
  
> [!NOTE]
>  **Wybierz operację** okno dialogowe zawiera tylko kontraktów lub operacji, które są używane przez inne <xref:System.Workflow.Activities.SendActivity> działań w przepływie pracy. Podobnie **wybierz operację** okno dialogowe <xref:System.Workflow.Activities.ReceiveActivity> działań pokazuje tylko kontraktów lub operacji, które są używane przez inne **działania ReceiveActivity** działań w przepływie pracy.  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: Implementowanie operacji kontraktu usługi WCF (starsza wersja)](../workflow-designer/how-to-implement-a-windows-communication-foundation-contract-operation-legacy.md)   
 [Porady: wywoływanie operacji kontraktu usługi WCF (starsza wersja)](../workflow-designer/how-to-invoke-a-windows-communication-foundation-contract-operation-legacy.md)   
 [Starsza wersja projektanta pomocy interfejsu użytkownika programu Windows Workflow Foundation](../workflow-designer/legacy-designer-for-windows-workflow-foundation-ui-help.md)