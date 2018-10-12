---
title: Przegląd pamięci podręcznej funkcji ClickOnce | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Windows applications, ClickOnce deployemtn
- ClickOnce applications, cache
- ClickOnce deployment, cache
ms.assetid: e379921e-9ef1-4326-bbf3-53ba67925526
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 5e976877a045b6efc7ca3d9fb103b9d1a8e88df7
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49217298"
---
# <a name="clickonce-cache-overview"></a>Przegląd pamięci podręcznej w technologii ClickOnce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Wszystkie [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacje, czy są one zainstalowane lokalnie, czy hostowanego w trybie online, są przechowywane na komputerze klienckim w [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)]aplikacji *pamięci podręcznej*. A [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] pamięci podręcznej to rodzina ukrytych katalogów w katalogu ustawienia lokalnego folderu Documents and Settings bieżącego użytkownika. Ta pamięć podręczna przechowuje pliki wszystkich aplikacji, w tym zestawy, pliki konfiguracji, aplikacji i ustawień użytkownika i katalog danych. Pamięć podręczna jest również odpowiedzialny za migracją katalog danych aplikacji do najnowszej wersji. Aby uzyskać więcej informacji na temat migracji danych, zobacz [Accessing Local and Remote Data in ClickOnce Applications](../deployment/accessing-local-and-remote-data-in-clickonce-applications.md).  
  
 W jednej lokalizacji do przechowywania danych aplikacji, [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] przejmuje zadań związanych z zarządzaniem fizycznych instalacji aplikacji przez użytkownika. Pamięć podręczna pomaga również w izolowania aplikacji dzięki przechowywaniu zestawów i plików danych dla wszystkich aplikacji i ich różne wersje oddzielić od siebie nawzajem. Na przykład po uaktualnieniu [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacji, wersji i jej zasoby danych są dostarczane za pomocą ich własnych katalogów w pamięci podręcznej.  
  
## <a name="cache-storage-quota"></a>Limit przydziału magazynu pamięci podręcznej  
 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacje, które są hostowane w trybie online są ograniczone ilości miejsca na ich mogą zajmować zgodnie z limitem przydziału, który ogranicza rozmiar [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] pamięci podręcznej. Rozmiar pamięci podręcznej, który ma zastosowanie do wszystkich użytkowników aplikacji online; pojedynczej aplikacji częściowo zaufanej, online jest ograniczona do zajmuje połowę miejsca limitu przydziału. Zainstalowane aplikacje nie są ograniczone przez rozmiar pamięci podręcznej i nie wliczają limit pamięci podręcznej. Dla wszystkich [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacji w pamięci podręcznej zachowuje tylko bieżącej wersji i wcześniej zainstalowanej wersji.  
  
 Domyślnie komputery klienckie mają 250 MB magazynu dla online [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacji. Pliki danych nie są wliczane do tego limitu. Administrator systemu zwiększyć lub zmniejszyć ten limit przydziału na komputerze klienckim w szczególności, zmieniając klucz rejestru HKEY_CURRENT_USER\Software\Classes\Software\Microsoft\Windows\CurrentVersion\Deployment\OnlineAppQuotaInKB, który jest wartością typu DWORD. który określa rozmiar pamięci podręcznej w kilobajtach. Na przykład aby zmniejszyć rozmiar pamięci podręcznej do 50 MB, należy zmienić tę wartość do 51200.  
  
## <a name="see-also"></a>Zobacz też  
 [Uzyskiwanie dostępu do danych lokalnych i zdalnych w aplikacjach ClickOnce](../deployment/accessing-local-and-remote-data-in-clickonce-applications.md)



