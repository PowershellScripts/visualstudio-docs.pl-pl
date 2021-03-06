---
ms.technology: vs-ai-tools
ms.openlocfilehash: 875bd78f6e1c6298d7f94360363dcf731cc3e992
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49874439"
---
# <a name="browse-storage-to-upload-data-or-download-models-and-logs"></a>Przeglądaj magazyn do przekazywania danych lub pobrać dzienniki i modeli

Możesz przeglądać cały magazyn na zdalnym komputerze lub udziału plików platformy Azure, aby umożliwić przekazywanie danych i pobierania modeli dzienników i. Lub, jeśli chcesz uzyskać dostęp do dzienników i dane wyjściowe zadania dotyczące określonego zadania, możecie również w przeglądarce zadania.

## <a name="to-access-all-data-on-the-remote-machine-or-file-share"></a>Dostęp do wszystkich danych na zdalnym komputerze lub udziału plikowego

1. Otwórz **Eksploratora serwera**.
2. Rozwiń węzeł kontekstu obliczeniowego usługi Batch AI lub maszynie zdalnej.
3. Kliknij prawym przyciskiem myszy **magazynu**; kliknij przycisk **Przeglądaj**.

    ![magazyn](media/manage-storage/browse-storage.png)

## <a name="to-access-job-specific-data-on-the-remote-machine-or-file-share"></a>Dostęp do danych z określonych zadań na zdalnym komputerze lub udziału plikowego

1. Otwórz [Historia zadania](job-details.md)
2. Wybierz zadanie.
3. Kliknij przycisk **pracy folderu** lub kliknij przycisk **StdOut / Stderr** umożliwiającą szybki dostęp do tych plików ważne dziennika.

    ![magazyn](media/manage-storage/job-workingfolder.png)