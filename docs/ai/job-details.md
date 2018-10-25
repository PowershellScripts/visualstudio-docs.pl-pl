---
ms.technology: vs-ai-tools
ms.openlocfilehash: ebf412dbeb4e0ecc391c52d7da5ea49d12e6231f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49930365"
---
# <a name="view-recent-job-performance-and-details"></a>Wyświetl ostatnią wydajność zadania i szczegóły

Po przesłaniu zadania można wyświetlić listę zadań, aby wyświetlić ich stan, czas trwania i nie tylko.

1. W **Eksploratora serwera**, rozwiń węzeł kontekstu obliczeniowego określone.
2. Kliknij dwukrotnie **zadań**.
3. Zobaczysz listę zadania przesłane do danego kontekstu obliczeniowego.
4. Wybierz konkretną **zadania** na liście, aby wyświetlić szczegóły.

![Monitorowanie zadań](media/job-details/monitor-jobs.png)

> Historia zadania przesłane do maszyn wirtualnych systemu Linux są przechowywane na maszynie Wirtualnej w folderze/tmp katalogu. W związku z tym w każdym przypadku, gdy zostanie ona ponownie uruchomiona w historii zadań jest wyczyszczone. Stałe rekordu historii zadania skonfigurować swoją maszynę Wirtualną jako kontekst obliczeniowy w Azure Machine learning, następnie prześlij zadanie usługi Azure Machine Learning (Wybieranie maszyny Wirtualnej jako kontekst obliczeniowy).