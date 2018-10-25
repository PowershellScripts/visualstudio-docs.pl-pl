---
title: Projektant przepływu pracy — inicjowanie korelacji, okno dialogowe
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- InitializeCorrelation.UI
ms.assetid: 2a0a1cd3-7b9e-493e-9264-fcf85289ffcf
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: edfdef1c1f946e2c5f677d0ff1578a40ea7bcd8f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49906237"
---
# <a name="initialize-correlation-dialog-box"></a>Inicjowanie korelacji, okno dialogowe

**Inicjowanie korelacji** okno dialogowe jest używany w Projektancie przepływu pracy do edytowania <xref:System.ServiceModel.Activities.InitializeCorrelation.CorrelationData%2A> właściwość <xref:System.ServiceModel.Activities.InitializeCorrelation> działania. Aby uzyskać więcej informacji, zobacz [InitializeCorrelation](../workflow-designer/initializecorrelation-activity-designer.md).

W poniższej tabeli opisano elementy interfejsu użytkownika **inicjowanie korelacji** okno dialogowe:

|Element interfejsu użytkownika|Opis|
|-|-----------------|
|**Korelacja**|<xref:System.ServiceModel.Activities.CorrelationHandle> Korelacji, aby zainicjować.|
|**Inicializace zapnuta**|Parą klucz/wartość, która zawiera dane do zainicjowania. Ta wartość odpowiada <xref:System.ServiceModel.Activities.InitializeCorrelation.CorrelationData%2A> właściwości. Przykładem parę prawidłowy klucz/wartość jest klucz o nazwie "OrderID", skojarzone ze zmienną o nazwie OrderID.|

## <a name="to-launch-the-initialize-correlation-dialog-box"></a>Aby uruchomić okno dialogowe Inicjowanie korelacji

Kliknij przycisk **widoku** na **InitializeCorrelation** działanie projektanta lub wybierz <xref:System.ServiceModel.Activities.InitializeCorrelation> działania w Projektancie przepływu pracy. Następnie kliknij przycisk oznaczony wielokropkiem obok <xref:System.ServiceModel.Activities.InitializeCorrelation.CorrelationData%2A> właściwość w siatce właściwości.

## <a name="see-also"></a>Zobacz także

- [InitializeCorrelation](../workflow-designer/initializecorrelation-activity-designer.md)