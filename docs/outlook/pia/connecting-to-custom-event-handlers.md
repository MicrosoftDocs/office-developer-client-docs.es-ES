---
title: Conexión con controladores de eventos personalizados
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58722b8b140f89f0fe29a3e52db578a423a0160a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351425"
---
# <a name="connecting-to-custom-event-handlers"></a><span data-ttu-id="8d880-102">Conexión con controladores de eventos personalizados</span><span class="sxs-lookup"><span data-stu-id="8d880-102">Connecting to custom event handlers</span></span>

<span data-ttu-id="8d880-p101">Outlook genera eventos para notificar a los complementos sobre algo que está sucediendo, como que la Bandeja de entrada está recibiendo un nuevo elemento de correo. Los complementos pueden indicar a Outlook que lleve a cabo determinadas acciones ante la repetición de un evento específico. Este mecanismo de alerta y devolución de llamada es compatible con delegados de .NET Framework. El ensamblado de interoperabilidad primario (PIA) de Outlook define delegados a los que puede conectar métodos de devolución de llamada para controlar los eventos correspondientes. En este tema se describe este proceso, que consiste en definir un método de devolución de llamada y conectarlo como un controlador de eventos para el objeto de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8d880-p101">Outlook raises events to notify add-ins about something happening, such as the Inbox receiving a new mail item. Add-ins can specify to Outlook that upon the occurrence of a specific event, certain actions should take place. This alert and callback mechanism is supported by delegates of the .NET Framework. The Outlook Primary Interop Assembly (PIA) defines delegates to which you can connect callback methods to handle corresponding events. This topic describes this process of defining a callback method and connecting it as an event handler to the Outlook object.</span></span>

## <a name="creating-a-callback-method"></a><span data-ttu-id="8d880-108">Creación de un método de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="8d880-108">Creating a Callback method</span></span>

<span data-ttu-id="8d880-109">Una devolución de llamada es un método que se implementa para controlar la repetición de un evento específico, y se ejecuta por origen de notificación.</span><span class="sxs-lookup"><span data-stu-id="8d880-109">A callback is a method that is implemented to handle the occurrence of a specific event and is executed by a notification source.</span></span> <span data-ttu-id="8d880-110">En Outlook, los complementos pueden implementar métodos de devolución de llamada para responder a determinados eventos generados por Outlook.</span><span class="sxs-lookup"><span data-stu-id="8d880-110">In Outlook, add-ins can implement callback methods to respond to certain events raised by Outlook.</span></span> <span data-ttu-id="8d880-111">El método de devolución de llamada debe coincidir con la firma del delegado del evento.</span><span class="sxs-lookup"><span data-stu-id="8d880-111">This callback method must match the signature of the delegate of that event.</span></span> <span data-ttu-id="8d880-112">Por ejemplo, para implementar un controlador de eventos para el evento [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), debe declarar el método de devolución de llamada que coincida con la firma del delegado correspondiente:</span><span class="sxs-lookup"><span data-stu-id="8d880-112">For example, to implement an event handler for the [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) event, you must declare the callback method that matches the signature of the corresponding delegate:</span></span>

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

<span data-ttu-id="8d880-p103">Al definir el método de devolución de llamada, omita la palabra clave **Delegate**, ya que de lo contrarío podría se definirá otro delegado. A continuación, se muestra un ejemplo de método de devolución de llamada, **MyItemSendEventHandler**:</span><span class="sxs-lookup"><span data-stu-id="8d880-p103">When defining the callback method, ignore the **Delegate** keyword which otherwise would define another delegate. A sample callback method, **MyItemSendEventHandler**, is shown below:</span></span>

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a><span data-ttu-id="8d880-115">Conexión a un método de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="8d880-115">Connecting a Callback method</span></span>

<span data-ttu-id="8d880-p104">Después de implementar un método de devolución de llamada para un evento, puede conectarlo al objeto de Outlook para que Outlook llame al método como controlador de eventos de dicho evento. Tenga en cuenta que un evento se puede controlar con más de un controlador de eventos y éste es el punto donde entran en juego los delegados que asignan el control de eventos a los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="8d880-p104">After implementing a callback method for an event, you can connect it to the Outlook object so that Outlook knows to call the method as an event handler of that event. Note that an event can be handled by more than one event handler, and this is where delegates that assign event handling to event handlers come into play.</span></span>

<span data-ttu-id="8d880-118">Siguiendo con el último ejemplo sobre cómo especificar un controlador de eventos para el evento **ItemSend** del objeto **Application**; para conectar **MyItemSendEventHandler** al objeto **Application** en C\#, cree una instancia del objeto de delegado, pase **MyItemSendEventHandler** al constructor del objeto de delegado y, a continuación, agréguelo al evento **ItemSend** usando el operador +=:</span><span class="sxs-lookup"><span data-stu-id="8d880-118">Continuing with the last example of specifying a event handler for the **ItemSend** event of the **Application** object, to connect **MyItemSendEventHandler** to the **Application** object in C\#, create an instance of the delegate object, pass **MyItemSendEventHandler** to the constructor of the delegate object, and then add this delegate object to the **ItemSend** event using the += operator:</span></span>

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

<span data-ttu-id="8d880-119">En Visual Basic, deberá usar la instrucción **AddHandler** para asociar el evento **ItemSend** al controlador de eventos **MyItemSendEventHandler**:</span><span class="sxs-lookup"><span data-stu-id="8d880-119">In Visual Basic, you use the **AddHandler** statement to associate the **ItemSend** event with the **MyItemSendEventHandler** event handler:</span></span>

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a><span data-ttu-id="8d880-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d880-120">See also</span></span>

- [<span data-ttu-id="8d880-121">Eventos del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="8d880-121">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)
- [<span data-ttu-id="8d880-122">Objetos del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="8d880-122">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)

