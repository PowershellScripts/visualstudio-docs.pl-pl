---
title: '&lt;zależność&gt; — Element (wdrażanie ClickOnce) | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#osVersionInfo
- urn:schemas-microsoft-com:asm.v2#os
- http://www.w3.org/2000/09/xmldsig#Transform
- urn:schemas-microsoft-com:asm.v2#dependency
- http://www.w3.org/2000/09/xmldsig#DigestValue
- urn:schemas-microsoft-com:asm.v2#assemblyIdentity
- http://www.w3.org/2000/09/xmldsig#DigestMethod
- http://www.w3.org/2000/09/xmldsig#Transforms
- urn:schemas-microsoft-com:asm.v2#hash
- urn:schemas-microsoft-com:asm.v2#dependentAssembly
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <dependency> element [ClickOnce deployment manifest]
ms.assetid: 9b4d2082-0347-4922-ac70-85f11b913039
caps.latest.revision: 29
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: af4b3fc79118e25fb5631de1a4ea4d5897355bf1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49214931"
---
# <a name="ltdependencygt-element-clickonce-deployment"></a>&lt;zależność&gt; — Element (wdrażanie ClickOnce)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Identyfikuje wersję aplikacji do zainstalowania i lokalizację w manifeście aplikacji.  
  
## <a name="syntax"></a>Składnia  
  
```  
  
      <dependency>   
   <dependentAssembly  
      preRequisite  
      visible  
      dependencyType  
      codeBase  
      size  
   >   
      <assemblyIdentity   
         name   
         version   
         publicKeyToken   
         processorArchitecture   
         language  
         type  
      />   
      <hash>  
         <dsig:Transforms>  
            <dsig:Transform  
                Algorithm  
            />  
         </dsig:Transforms>  
         <dsig:DigestMethod />  
         <dsig:DigestValue>  
         </dsig:DigestValue>  
      </hash>  
  
   </dependentAssembly>   
</dependency>  
```  
  
## <a name="elements-and-attributes"></a>Atrybuty i elementy  
 `dependency` Element jest wymagany. Go nie ma żadnych atrybutów. Manifest wdrożenia mogą mieć wiele `dependency` elementów.  
  
 `dependency` Element najczęściej wyraża zależności dla głównej aplikacji na zestawach zawartych w [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacji. Jeśli aplikacja Main.exe wykorzystuje zestaw o nazwie DotNetAssembly.dll, tego zestawu musi być wymieniony w sekcji zależności. Zależność, jednak można również wyrazić innych typów zależności, takie jak zależności od określonej wersji środowiska CLR zestawu w globalnej pamięci podręcznej zestawów (GAC) lub obiektów COM. Ponieważ jest to technologia wdrożenia bezobsługowego [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] nie można zainicjować pobranie i zainstalowanie tego rodzaju zależności, ale uniemożliwia uruchomienie aplikacji, jeśli nie istnieją co najmniej jedną z określonymi zależnościami.  
  
## <a name="dependentassembly"></a>dependentAssembly  
 Wymagane. Ten element zawiera `assemblyIdentity` elementu. W poniższej tabeli przedstawiono atrybuty `dependentAssembly` obsługuje.  
  
|Atrybut|Opis|  
|---------------|-----------------|  
|`preRequisite`|Opcjonalna. Określa, że ten zestaw powinna już istnieć w pamięci podręcznej GAC. Prawidłowe wartości to `true` i `false`. Jeśli `true`i określony zestaw nie istnieje w pamięci podręcznej GAC, aplikacja nie może uruchomić.|  
|`visible`|Opcjonalna. Określa tożsamość aplikacji najwyższego poziomu, łącznie z jej zależnościami. Używane wewnętrznie przez [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] na potrzeby zarządzania i aktywacji aplikacji.|  
|`dependencyType`|Wymagane. Relacja między tą zależnością i aplikacji. Prawidłowe wartości to:<br /><br /> -   `install`. Składnik stanowi oddzielną instalacją od bieżącej aplikacji.<br />-   `preRequisite`. Składnik jest wymagany przez bieżącą aplikację.|  
|`codebase`|Opcjonalna. Pełna ścieżka do manifestu aplikacji.|  
|`size`|Opcjonalna. Rozmiar manifest aplikacji, w bajtach.|  
  
## <a name="assemblyidentity"></a>assemblyIdentity  
 Wymagane. Ten element jest elementem podrzędnym `dependentAssembly` elementu. Zawartość `assemblyIdentity` musi być taka sama, jak opisano w [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] manifestu aplikacji. W poniższej tabeli przedstawiono atrybuty `assemblyIdentity` elementu.  
  
|Atrybut|Opis|  
|---------------|-----------------|  
|`Name`|Wymagane. Określa nazwę aplikacji.|  
|`Version`|Wymagane. Określa numer wersji aplikacji, w następującym formacie: `major.minor.build.revision`|  
|`publicKeyToken`|Wymagane. Określa ciąg szesnastkowy 16 znaków, który reprezentuje ostatnie 8 bajtów Skrót SHA-1 klucza publicznego, w ramach której aplikacja lub zestaw jest podpisany. Klucz publiczny używany do podpisywania musi wynosić 2048 bitów lub nowszej.|  
|`processorArchitecture`|Wymagane. Określa procesor. Prawidłowe wartości to `x86` dla Windows 32-bitowe i `IA64` dla Windows 64-bitowych.|  
|`Language`|Opcjonalna. Określa część dwóch kodów języka zestawu. Na przykład: EN-US, który oznacza dla języka angielskiego (US). Wartość domyślna to `neutral`. Tego elementu jest `asmv2` przestrzeni nazw.|  
|`type`|Opcjonalna. Dla zapewnienia zgodności z Windows side-by-side zainstalować technologii. Jest to jedyna wartość dozwolone `win32`.|  
  
## <a name="hash"></a>hash  
 `hash` Element jest opcjonalny element podrzędny elementu `file` elementu. `hash` Element nie ma żadnych atrybutów.  
  
 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] używa konsolidatorze skrótów wszystkich plików w aplikacji w celu sprawdzenia zabezpieczeń, aby upewnić się, że żaden z plików zostały zmienione po wdrożeniu. Jeśli `hash` element nie jest uwzględniony, ten test nie zostanie wykonane. W związku z pominięciem `hash` element nie jest zalecane.  
  
## <a name="dsigtransforms"></a>DSIG:TRANSFORMS  
 `dsig:Transforms` Element jest wymagany element podrzędny elementu `hash` elementu. `dsig:Transforms` Element nie ma żadnych atrybutów.  
  
## <a name="dsigtransform"></a>DSIG:Transform  
 `dsig:Transform` Element jest wymagany element podrzędny elementu `dsig:Transforms` elementu. W poniższej tabeli przedstawiono atrybuty `dsig:Transform` elementu.  
  
|Atrybut|Opis|  
|---------------|-----------------|  
|`Algorithm`|Algorytm używany do obliczania skrótu dla tego pliku. Obecnie tylko wartość używana przez [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] jest `urn:schemas-microsoft-com:HashTransforms.Identity`.|  
  
## <a name="dsigdigestmethod"></a>DSIG:DigestMethod  
 `dsig:DigestMethod` Element jest wymagany element podrzędny elementu `hash` elementu. W poniższej tabeli przedstawiono atrybuty `dsig:DigestMethod` elementu.  
  
|Atrybut|Opis|  
|---------------|-----------------|  
|`Algorithm`|Algorytm używany do obliczania skrótu dla tego pliku. Obecnie tylko wartość używana przez [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] jest `http://www.w3.org/2000/09/xmldsig#sha1`.|  
  
## <a name="dsigdigestvalue"></a>DSIG:DigestValue  
 `dsig:DigestValue` Element jest wymagany element podrzędny elementu `hash` elementu. `dsig:DigestValue` Element nie ma żadnych atrybutów. Jego wartość tekstowa jest obliczana wartość skrótu dla określonego pliku.  
  
## <a name="remarks"></a>Uwagi  
 Manifesty wdrożenia zwykle mają jeden `assemblyIdentity` element, który identyfikuje nazwa i wersja manifestu aplikacji.  
  
## <a name="example"></a>Przykład  
 Poniższy kod przedstawia przykład `dependency` element [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] manifest wdrożenia.  
  
```  
<!-- Identify the assembly dependencies -->  
<dependency>  
  <dependentAssembly dependencyType="install" allowDelayedBinding="true" codebase="MyApplication.exe" size="16384">  
    <assemblyIdentity name="MyApplication" version="0.0.0.0" cultural="neutral" processorArchitecture="msil" />  
    <hash>  
      <dsig:Transforms>  
        <dsig:Transform Algorithm="urn:schemas-microsoft-com:HashTransforms.Identity" />  
      </dsig:Transforms>  
      <dsig:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />  
       <dsig:DigestValue>YzXYZJAvj9pgAG3y8jXUjC7AtHg=</dsig:DigestValue>  
    </hash>  
  </dependentAssembly>  
</dependency>  
```  
  
## <a name="example"></a>Przykład  
 Poniższy przykład kodu określa zależność z zestawem już zainstalowane w GAC.  
  
```  
<dependency>  
  <dependentAssembly dependencyType="preRequisite" allowDelayedBinding="true">  
    <assemblyIdentity name="GACAssembly" version="1.0.0.0" language="neutral" processorArchitecture="msil" />  
  </dependentAssembly>  
</dependency>  
```  
  
## <a name="example"></a>Przykład  
 Poniższy przykład kodu określa zależność od określonej wersji środowiska uruchomieniowego języka wspólnego.  
  
```  
<dependency>  
  <dependentAssembly dependencyType="preRequisite" allowDelayedBinding="true">  
    <assemblyIdentity name="Microsoft.Windows.CommonLanguageRuntime" version="2.0.50215.0" />  
  </dependentAssembly>  
</dependency>  
```  
  
## <a name="example"></a>Przykład  
 Poniższy przykład kodu określa zależności systemu operacyjnego.  
  
```  
<dependency>  
   <dependentOS supportUrl="http://www.microsoft.com" description="Microsoft Windows Operating System">  
      <osVersionInfo>  
         <os majorVersion="4" minorVersion="10" />  
      </osVersionInfo>  
   </dependentOS>  
</dependency>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Manifest wdrażania ClickOnce](../deployment/clickonce-deployment-manifest.md)   
 [\<zależność > Element](../deployment/dependency-element-clickonce-application.md)



