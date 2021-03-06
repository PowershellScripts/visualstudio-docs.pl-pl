---
title: 'Porady: udostępnianie usługi | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- services, providing
ms.assetid: 12bc1f12-47b1-44f6-b8db-862aa88d50d1
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 2408eace3ecea447c9b49ff17c729e3f4661b5d6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942559"
---
# <a name="how-to-provide-a-service"></a>Porady: świadczenia usług
Pakietu VSPackage oferuje usługi, które można użyć innych pakietów VSPackage. Do świadczenia usług, pakietu VSPackage należy zarejestrować usługę za pomocą programu Visual Studio, a następnie Dodaj usługę.  
  
 <xref:Microsoft.VisualStudio.Shell.Package> Klasa implementuje interfejsy <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider> i <xref:System.ComponentModel.Design.IServiceContainer>. <xref:System.ComponentModel.Design.IServiceContainer> zawiera metody wywołania zwrotnego, które zapewniają usługi na żądanie.  
  
 Aby uzyskać więcej informacji na temat usług, zobacz [usługa essentials](../extensibility/internals/service-essentials.md) .  
  
> [!NOTE]
>  Gdy pakietu VSPackage ma zostać zwolniony, Visual Studio czeka, aż wszystkie żądania dotyczące usług, które zapewnia pakietu VSPackage zostały dostarczone. Nie zezwalaj na nowe żądania dla tych usług. Nie należy jawnie wywołać <xref:Microsoft.VisualStudio.Shell.Interop.IProfferService.RevokeService%2A> metody, aby można było odwołać usługi podczas zwalniania.  
  
## <a name="implement-a-service"></a>Implementowanie usługi  
  
1. Utwórz projekt VSIX (**pliku** > **New** > **projektu** > **Visual C#**  >  **Rozszerzalności** > **projekt VSIX**).  
  
2. Dodanie pakietu VSPackage do projektu. Wybierz węzeł projektu w **Eksploratora rozwiązań** i kliknij przycisk **Dodaj** > **nowy element** > **elementy Visual C#**  >  **Rozszerzalności** > **pakietu Visual Studio**.  
  
3. Aby wdrożyć usługi, musisz utworzyć trzy typy:  
  
   - Interfejs, który zawiera opis usługi. Wiele z tych interfejsów są puste, oznacza to, ponieważ mają one żadnych metod.  
  
   - Interfejs, który opisuje interfejs usługi. Ten interfejs zawiera metody do zaimplementowania.  
  
   - Klasa, która implementuje interfejs usługi i usługi.  
  
     Poniższy przykład pokazuje podstawową implementację trzy typy. Konstruktor klasy usługi należy ustawić dostawcę usług.  
  
   ```csharp  
   public class MyService : SMyService, IMyService  
   {  
       private Microsoft.VisualStudio.OLE.Interop.IServiceProvider serviceProvider;  
       private string myString;  
       public MyService(Microsoft.VisualStudio.OLE.Interop.IServiceProvider sp)  
       {  
           Trace.WriteLine(  
                  "Constructing a new instance of MyService");  
           serviceProvider = sp;  
       }  
       public void Hello()  
       {  
           myString = "hello";  
       }  
       public string Goodbye()  
       {  
          return "goodbye";  
       }  
   }  
   public interface SMyService  
   {  
   }  
   public interface IMyService  
   {  
       void Hello();  
       string Goodbye();  
   }  
  
   ```  
  
### <a name="register-a-service"></a>Zarejestruj usługę  
  
1.  Aby zarejestrować usługę, należy dodać <xref:Microsoft.VisualStudio.Shell.ProvideServiceAttribute> do pakietu VSPackage, która dostarcza usługę. Oto przykład:  
  
    ```csharp  
    [ProvideService(typeof(SMyService))]  
    [PackageRegistration(UseManagedResourcesOnly = true)]  
    [Guid(VSPackage1.PackageGuidString)]  
    public sealed class VSPackage1 : Package  
    {. . . }  
    ```  
  
     Ten atrybut rejestruje `SMyService` z programem Visual Studio.  
  
    > [!NOTE]
    >  Aby zarejestrować to usługa, która zastępuje inną usługę o takiej samej nazwie, użyj <xref:Microsoft.VisualStudio.Shell.ProvideServiceOverrideAttribute>. Uwaga dozwolony jest tylko jeden zastąpienie usługi.  
  
### <a name="add-a-service"></a>Dodaj usługę  
  
1.  W inicjatorze pakietu VSPackage Dodaj usługę, a następnie dodaj metodę wywołania zwrotnego, trzeba utworzyć usługi. Oto zmiany do wprowadzenia <xref:Microsoft.VisualStudio.Shell.Package.Initialize%2A> metody:  
  
    ```csharp  
    protected override void Initialize()  
    {  
        ServiceCreatorCallback callback =new ServiceCreatorCallback(CreateService);  
  
        ((IServiceContainer)this).AddService(typeof(SMyService), callback);  
    . . .  
    }  
    ```  
  
2.  Implementuje metody wywołania zwrotnego, które należy utworzyć i zwracać usługi lub wartość null, jeśli nie można utworzyć.  
  
    ```csharp  
    private object CreateService(IServiceContainer container, Type serviceType)  
    {  
        if (typeof(SMyService) == serviceType)  
            return new MyService(this);  
        return null;  
    }  
    ```  
  
    > [!NOTE]
    >  Program Visual Studio można odrzucić żądanie do świadczenia usług. Robi to jeśli innego pakietu VSPackage już zawiera usługę.  
  
3.  Teraz możesz pobrać usługę i użycie jej metod. W poniższym przykładzie przy użyciu usługi w inicjatorze, ale możesz uzyskać odpowiednią usługę dowolne miejsce do korzystania z usługi.  
  
    ```csharp  
    protected override void Initialize()  
    {  
        ServiceCreatorCallback callback =new ServiceCreatorCallback(CreateService);  
  
        ((IServiceContainer)this).AddService(typeof(SMyService), callback);  
  
        MyService myService = (MyService) this.GetService(typeof(SMyService));  
        myService.Hello();  
        string helloString = myService.Goodbye();  
  
        base.Initialize();  
    }  
    ```  
  
     Wartość `helloString` powinien być "Hello".  
  
## <a name="see-also"></a>Zobacz także  
 [Porady: uzyskiwanie usługi](../extensibility/how-to-get-a-service.md)   
 [Użyj i świadczenia usług](../extensibility/using-and-providing-services.md)   
 [Podstawowe informacje o usłudze](../extensibility/internals/service-essentials.md)
