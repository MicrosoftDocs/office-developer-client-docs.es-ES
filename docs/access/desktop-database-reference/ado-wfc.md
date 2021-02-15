---
title: ADO para Windows Foundation Classes (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df9def320274df0eb4636aa237deb566dd5725b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281725"
---
# <a name="adowfc"></a><span data-ttu-id="5b4fc-102">ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="5b4fc-102">ADO/WFC</span></span>


<span data-ttu-id="5b4fc-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b4fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b4fc-p101">ADO para Windows Foundation Classes (ADO/WFC) se basa en el modelo de eventos de ADO y presenta una interfaz de programación de aplicaciones simplificada. En general, ADO/WFC intercepta eventos de ADO, consolida los parámetros de eventos en una sola clase de eventos y, a continuación, llama al controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p101">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface. In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</span></span>

<span data-ttu-id="5b4fc-106">**Para utilizar eventos de ADO en ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="5b4fc-106">**To use ADO events in ADO/WFC**</span></span>

1.  <span data-ttu-id="5b4fc-p102">Defina su propio controlador de eventos para procesar un evento. Por ejemplo, para procesar el evento **ConnectComplete** de la familia **ConnectionEvent**, podría utilizar este código:</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p102">Define your own event handler to process an event. For example, if you wanted to process the **ConnectComplete** event in the **ConnectionEvent** family, you might use this code:</span></span>
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  <span data-ttu-id="5b4fc-p103">Defina un objeto handler que represente su controlador de eventos. El objeto handler debe ser de tipo de datos **ConnectEventHandler** para un evento de tipo **ConnectionEvent**, o de tipo de datos **RecordsetEventHandler** para un evento de tipo **RecordsetEvent**. Por ejemplo, cree el siguiente código para su controlador de eventos **ConnectComplete**:</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p103">Define a handler object to represent your event handler. The handler object should be of data type **ConnectEventHandler** for an event of type **ConnectionEvent**, or data type **RecordsetEventHandler** for an event of type **RecordsetEvent**. For example, code the following for your **ConnectComplete** event handler:</span></span>
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    <span data-ttu-id="5b4fc-p104">El primer argumento del constructor **ConnectionEventHandler** es una referencia a la clase que contiene el controlador de eventos que se menciona en el segundo argumento. El compilador de Microsoft Visual J++ también admite una sintaxis equivalente:</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p104">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="5b4fc-p105">El primer argumento del constructor **ConnectionEventHandler** es una referencia a la clase que contiene el controlador de eventos que se menciona en el segundo argumento. El compilador de Microsoft Visual J++ también admite una sintaxis equivalente:</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p105">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="5b4fc-116">El único argumento es una referencia a la clase (**this**) y al método deseados dentro de la clase (**onConnectComplete**).</span><span class="sxs-lookup"><span data-stu-id="5b4fc-116">The single argument is a reference to the desired class (**this**) and method within the class (**onConnectComplete**).</span></span>

3.  <span data-ttu-id="5b4fc-117">Agregue su controlador de eventos a una lista de controladores designados para procesar un tipo determinado de evento.</span><span class="sxs-lookup"><span data-stu-id="5b4fc-117">Add your event handler to a list of handlers designated to process a particular type of event.</span></span> <span data-ttu-id="5b4fc-118">Utilice el método con un nombre como \**addOn\*\*\*EventName*(*controlador*).</span><span class="sxs-lookup"><span data-stu-id="5b4fc-118">Use the method with a name such as \**addOn\*\*\*EventName*(*handler*).</span></span>

4.  <span data-ttu-id="5b4fc-p107">ADO/WFC implementa internamente todos los controladores de eventos de ADO. Por tanto, un evento causado por una operación **Connection** o **Recordset** es interceptado por un controlador de eventos de ADO/WFC. El controlador de eventos de ADO/WFC pasa parámetros **ConnectionEvent** de ADO en una instancia de la clase **ConnectionEvent** de ADO/WFC, o parámetros **RecordsetEvent** de ADO en una instancia de la clase **RecordsetEvent** de ADO/WFC. Estas clases de ADO/WFC consolidan los parámetros de eventos de ADO; es decir, que cada clase de ADO/WFC contiene un elemento de datos para cada parámetro único en todos los métodos **ConnectionEvent** o **RecordsetEvent** de ADO.</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p107">ADO/WFC internally implements all the ADO event handlers. Therefore, an event caused by a **Connection** or **Recordset** operation is intercepted by an ADO/WFC event handler. The ADO/WFC event handler passes ADO **ConnectionEvent** parameters in an instance of the ADO/WFC **ConnectionEvent** class, or ADO **RecordsetEvent** parameters in an instance of the ADO/WFC **RecordsetEvent** class. These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO **ConnectionEvent** or **RecordsetEvent** methods.</span></span>

5.  <span data-ttu-id="5b4fc-p108">Después, ADO/WFC llama al controlador de eventos con el objeto event de ADO/WFC. Por ejemplo, el controlador **onConnectComplete** tiene una firma similar a:</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p108">ADO/WFC then calls your event handler with the ADO/WFC event object. For example, your **onConnectComplete** handler has a signature like this:</span></span>
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    <span data-ttu-id="5b4fc-125">El primer argumento es el tipo de objeto que envió el evento ([Connection](connection-object-ado.md) o [Recordset](recordset-object-ado.md)) y el segundo argumento es el objeto event de ADO/WFC (**ConnectionEvent** o **RecordsetEvent**).</span><span class="sxs-lookup"><span data-stu-id="5b4fc-125">The first argument is the type of object that sent the event ([Connection](connection-object-ado.md) or [Recordset](recordset-object-ado.md)), and the second argument is the ADO/WFC event object (**ConnectionEvent** or **RecordsetEvent**).</span></span> <span data-ttu-id="5b4fc-126">La firma del controlador de eventos es más sencilla que un evento de ADO.</span><span class="sxs-lookup"><span data-stu-id="5b4fc-126">The signature of your event handler is simpler than an ADO event.</span></span> <span data-ttu-id="5b4fc-127">Sin embargo, es necesario que comprenda el modelo de eventos de ADO para saber qué parámetros son aplicables a un evento y cómo responder.</span><span class="sxs-lookup"><span data-stu-id="5b4fc-127">However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</span></span>

6.  <span data-ttu-id="5b4fc-p110">Vuelva desde el controlador de eventos al controlador de ADO/WFC correspondiente al evento de ADO. ADO/WFC copia elementos de datos de eventos de ADO/WFC pertinentes de nuevo en los parámetros de eventos de ADO y, a continuación, vuelve el controlador de eventos de ADO.</span><span class="sxs-lookup"><span data-stu-id="5b4fc-p110">Return from your event handler to the ADO/WFC handler for the ADO event. ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</span></span>

7.  <span data-ttu-id="5b4fc-130">Cuando haya finalizado el procesamiento, quite su controlador de la lista de controladores de eventos de ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="5b4fc-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span></span> <span data-ttu-id="5b4fc-131">Utilice el método con un nombre como \**removeOn\*\*\*EventName*(*controlador*).</span><span class="sxs-lookup"><span data-stu-id="5b4fc-131">Use the method with a name such as \**removeOn\*\*\*EventName*(*handler*).</span></span>

