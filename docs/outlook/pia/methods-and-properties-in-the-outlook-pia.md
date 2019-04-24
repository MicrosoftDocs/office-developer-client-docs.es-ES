---
title: Métodos y propiedades del PIA de Outlook
TOCTitle: Methods and properties in the Outlook PIA
ms:assetid: ec7742de-ead6-41dd-90a3-1280fdf09d54
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612528(v=office.15)
ms:contentKeyID: 55119780
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90c13559094fbffd2dbe9a99602ee235c92d9445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351040"
---
# <a name="methods-and-properties-in-the-outlook-pia"></a><span data-ttu-id="631d7-102">Métodos y propiedades del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="631d7-102">Methods and properties in the Outlook PIA</span></span>

<span data-ttu-id="631d7-103">En este tema se describe cómo obtener acceso a los métodos y las propiedades de un objeto de código administrado usando el ensamblado de interoperabilidad primario (PIA) de Outlook.</span><span class="sxs-lookup"><span data-stu-id="631d7-103">This topic describes how to access methods and properties of an object in managed code by using the Outlook Primary Interop Assembly (PIA).</span></span>

## <a name="where-helper-objects-come-from"></a><span data-ttu-id="631d7-104">Origen de los objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="631d7-104">Where Helper objects come from</span></span>

<span data-ttu-id="631d7-p101">Para crear el PIA, Outlook usa el importador de la biblioteca de tipos (TLBIMP) en .NET Framework para convertir definiciones de tipo de la biblioteca de tipos COM en definiciones equivalentes de un ensamblado de Common Language Runtime (CLR). En COM, un objeto es en realidad una coclase que consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="631d7-p101">To create the Outlook PIA, Outlook uses the Type Library Importer (TLBIMP) in the .NET Framework to convert type definitions in the COM type library into equivalent definitions in a common language runtime (CLR) assembly. In COM, an object is actually a coclass that consists of the following:</span></span>

- <span data-ttu-id="631d7-107">La interfaz principal (por ejemplo, la interfaz [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="631d7-107">The primary interface (for example, the [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)) interface).</span></span>

- <span data-ttu-id="631d7-108">La interfaz de eventos (por ejemplo, la interfaz [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="631d7-108">The event interface (for example, the [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\)) interface).</span></span>

<span data-ttu-id="631d7-109">TLBIMP importa la interfaz primaria y la interfaz de eventos de cada objeto y crea una cantidad de interfaces, delegados y clases, entre los que se encuentra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="631d7-109">TLBIMP imports the primary interface and the event interface for each object and creates a number of interfaces, delegates, and classes, among which are the following:</span></span>

- <span data-ttu-id="631d7-110">La interfaz de eventos .NET (por ejemplo, la interfaz [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="631d7-110">The .NET event interface (for example, the [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\)) interface).</span></span>

- <span data-ttu-id="631d7-111">La clase .NET (por ejemplo, la clase [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="631d7-111">The .NET class (for example, the [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\)) class).</span></span>

- <span data-ttu-id="631d7-112">La interfaz .NET (por ejemplo, la interfaz [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="631d7-112">The .NET interface (for example, the [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) interface).</span></span>

## <a name="what-the-helper-objects-are-for"></a><span data-ttu-id="631d7-113">Función de los objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="631d7-113">What the Helper objects are for</span></span>

<span data-ttu-id="631d7-114">Continuando con el objeto **FormRegion** como ejemplo, la siguiente lista examina lo que contiene cada interfaz y clase enumeradas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="631d7-114">Continuing to use the **FormRegion** object as an example, the following list examines what each interface and class listed earlier contains.</span></span>

- <span data-ttu-id="631d7-115">La interfaz \_FormRegion define todos los métodos y propiedades de FormRegion.</span><span class="sxs-lookup"><span data-stu-id="631d7-115">The \_FormRegion interface defines all the methods and properties of FormRegion.</span></span> <span data-ttu-id="631d7-116">Salvo en un caso que se describe más adelante, esta interfaz no suele usarse en el código.</span><span class="sxs-lookup"><span data-stu-id="631d7-116">Typically you do not use this interface in code, except for a condition discussed below.</span></span>

- <span data-ttu-id="631d7-117">La interfaz **FormRegionEvents** define métodos que se asignan a eventos de FormRegion.</span><span class="sxs-lookup"><span data-stu-id="631d7-117">The **FormRegionEvents** interface defines methods mapping to events of FormRegion.</span></span> <span data-ttu-id="631d7-118">Esta interfaz no se usa en el código.</span><span class="sxs-lookup"><span data-stu-id="631d7-118">You do not use this interface in code.</span></span>

- <span data-ttu-id="631d7-119">TLBIMP procesa aún más la interfaz **FormRegionEvents** para crear la interfaz **FormRegionEvents**\_Event que define todos los eventos de FormRegion.</span><span class="sxs-lookup"><span data-stu-id="631d7-119">TLBIMP further processes the **FormRegionEvents** interface to create the **FormRegionEvents**\_Event interface that defines all the events of FormRegion.</span></span> <span data-ttu-id="631d7-120">Salvo en un caso que se describe más adelante, esta interfaz no suele usarse en el código.</span><span class="sxs-lookup"><span data-stu-id="631d7-120">Typically you do not use this interface in code, except for a condition discussed below.</span></span>

- <span data-ttu-id="631d7-p105">La clase FormRegionClass define todos los miembros de eventos, propiedades y métodos de FormRegion. Ésta es la clase a la que se atribuye la interfaz FormRegion para asociarla en segundo plano, de modo que puede escribir un código para crear una instancia de la interfaz FormRegion. Sin embargo, esta interfaz no se usa directamente en código.</span><span class="sxs-lookup"><span data-stu-id="631d7-p105">The FormRegionClass class defines all the method, property, and event members of FormRegion. This is the class that the FormRegion interface is attributed to associate with behind the scenes so that you can write code to create an instance of the FormRegion interface. However, you do not use this interface directly in code.</span></span>

- <span data-ttu-id="631d7-124">La interfaz FormRegion hereda la interfaz \_FormRegion y la interfaz **FormRegionEvents**\_Event.</span><span class="sxs-lookup"><span data-stu-id="631d7-124">The FormRegion interface inherits the \_FormRegion interface and the **FormRegionEvents**\_Event interface.</span></span> <span data-ttu-id="631d7-125">La figura 1 ilustra esta relación de herencia.</span><span class="sxs-lookup"><span data-stu-id="631d7-125">Figure 1 illustrates this inheritance relationship.</span></span>
    
  <span data-ttu-id="631d7-126">**Figura 1. La interfaz FormRegion hereda métodos y propiedades de la interfaz \_FormRegion y eventos de la interfaz FormRegionEvents\_Event**</span><span class="sxs-lookup"><span data-stu-id="631d7-126">**Figure 1. The FormRegion interface inherits methods and properties from the \_FormRegion interface, and inherits events from the FormRegionEvents\_Event interface**</span></span>

  ![La interfaz FormRegion hereda métodos y propiedades de la interfaz _FormRegion y eventos de la interfaz FormRegionEvents_Event](media/pia-form-region-interface.gif)
    
  <span data-ttu-id="631d7-128">Generalmente, FormRegion es la única interfaz que se usa en código administrado para obtener acceso al objeto y a los miembros de eventos, propiedades y métodos del objeto **FormRegion**.</span><span class="sxs-lookup"><span data-stu-id="631d7-128">Typically, FormRegion is the one interface you use in managed code to access the object and the method, property, and event members of the **FormRegion** object.</span></span>

<span data-ttu-id="631d7-129">Usando el objeto **Application** como otro ejemplo, debe acceder al objeto **Application** y a sus métodos, propiedades y eventos a través de la interfaz [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="631d7-129">Using the **Application** object as another example, you access the **Application** object, methods, properties, and events through the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) interface.</span></span> <span data-ttu-id="631d7-130">Sin embargo, hay tres excepciones en las que debe usar una interfaz diferente, o según el idioma, podría ser conveniente que usase una interfaz diferente:</span><span class="sxs-lookup"><span data-stu-id="631d7-130">There are however three exceptions where you must use a different interface, or depending on the language, you would want to use a different interface:</span></span>

- <span data-ttu-id="631d7-131">Al acceder a un método que comparte el mismo nombre que un evento, es recomendable realizar la conversión a la interfaz principal para llamar al método.</span><span class="sxs-lookup"><span data-stu-id="631d7-131">When you access a method that shares the same name as an event, a good practice is to cast to the primary interface to call the method.</span></span> <span data-ttu-id="631d7-132">Por ejemplo, el objeto **Application** tiene un método [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) y un evento [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="631d7-132">For example, the **Application** object has a [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) method and a [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)) event.</span></span> <span data-ttu-id="631d7-133">En Visual Basic. NET, puede obtener acceso al método Quit a través de la interfaz Application.</span><span class="sxs-lookup"><span data-stu-id="631d7-133">In Visual Basic .NET, you can access the Quit method through the Application interface.</span></span> <span data-ttu-id="631d7-134">C\#, puede evitar una advertencia de compilador convirtiendo el método Quit a la interfaz principal tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="631d7-134">In C\#, you can avoid a compiler warning by casting the Quit method to the primary interface, as shown in the following code sample:</span></span>
    
   ```csharp
      void DemoApp()
      {
          Outlook.Application myApp = new Outlook.Application();
          // Other application code here
          ((Outlook._Application)myApp).Quit();
      }
   ```

- <span data-ttu-id="631d7-135">Al obtener acceso a un evento que comparte el mismo nombre que un método de ese objeto, debe realizar la conversión a la interfaz de eventos adecuada para conectarse al evento.</span><span class="sxs-lookup"><span data-stu-id="631d7-135">When you access an event that shares the same name as a method of that object, you must cast to the appropriate event interface to connect to the event.</span></span> <span data-ttu-id="631d7-136">De manera similar al ejemplo anterior, para conectarse al evento [Quit\_, debe realizar la conversión a la interfaz ApplicationEvents\_11](https://msdn.microsoft.com/library/bb622725\(v=office.15\))Event.</span><span class="sxs-lookup"><span data-stu-id="631d7-136">Similar to the example above, to connect to the Quit event, you cast to the [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)) interface.</span></span>

- <span data-ttu-id="631d7-137">Al conectarse a una versión anterior de un evento que se ha ampliado posteriormente en una versión posterior de Outlook, debe conectarse a la versión del evento de la interfaz anterior.</span><span class="sxs-lookup"><span data-stu-id="631d7-137">When you connect to an earlier version of an event that has been subsequently extended in a later version of Outlook, you must connect to the version of the event in the earlier interface.</span></span> <span data-ttu-id="631d7-138">Por ejemplo, si quiere conectarse a la versión del evento Quit del objeto **Application** implementado para Outlook 2002 en lugar de a la última versión, conéctese al evento [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) definido en la interfaz [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)), en lugar de al evento Quit definido en la interfaz ApplicationEvents\_11\_Event.</span><span class="sxs-lookup"><span data-stu-id="631d7-138">For example, if you want to connect to the version of the Quit event for the **Application** object implemented for Outlook 2002 instead of the latest version, connect to the [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) event defined in the [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)) interface, instead of the Quit event defined in the ApplicationEvents\_11\_Event interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="631d7-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="631d7-139">See also</span></span>

- [<span data-ttu-id="631d7-140">Relación del PIA de Outlook con el modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="631d7-140">Relating the Outlook PIA with the object model</span></span>](relating-the-outlook-pia-with-the-object-model.md)
- [<span data-ttu-id="631d7-141">Objetos del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="631d7-141">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)
- [<span data-ttu-id="631d7-142">Eventos del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="631d7-142">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)

