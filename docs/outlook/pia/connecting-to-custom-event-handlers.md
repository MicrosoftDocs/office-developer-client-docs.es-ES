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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711801"
---
# <a name="connecting-to-custom-event-handlers"></a>Conexión con controladores de eventos personalizados

Outlook genera eventos para notificar a los complementos sobre algo que está sucediendo, como que la Bandeja de entrada está recibiendo un nuevo elemento de correo. Los complementos pueden indicar a Outlook que lleve a cabo determinadas acciones ante la repetición de un evento específico. Este mecanismo de alerta y devolución de llamada es compatible con delegados de .NET Framework. El ensamblado de interoperabilidad primario (PIA) de Outlook define delegados a los que puede conectar métodos de devolución de llamada para controlar los eventos correspondientes. En este tema se describe este proceso, que consiste en definir un método de devolución de llamada y conectarlo como un controlador de eventos para el objeto de Outlook.

## <a name="creating-a-callback-method"></a>Creación de un método de devolución de llamada

Una devolución de llamada es un método que se implementa para controlar la repetición de un evento específico, y se ejecuta por origen de notificación. En Outlook, los complementos pueden implementar métodos de devolución de llamada para responder a determinados eventos generados por Outlook. El método de devolución de llamada debe coincidir con la firma del delegado del evento. Por ejemplo, para implementar un controlador de eventos para el evento [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), debe declarar el método de devolución de llamada que coincida con la firma del delegado correspondiente:

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

Al definir el método de devolución de llamada, omita la palabra clave **Delegate**, ya que de lo contrarío podría se definirá otro delegado. A continuación, se muestra un ejemplo de método de devolución de llamada, **MyItemSendEventHandler**:

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a>Conexión a un método de devolución de llamada

Después de implementar un método de devolución de llamada para un evento, puede conectarlo al objeto de Outlook para que Outlook llame al método como controlador de eventos de dicho evento. Tenga en cuenta que un evento se puede controlar con más de un controlador de eventos y éste es el punto donde entran en juego los delegados que asignan el control de eventos a los controladores de eventos.

Siguiendo con el último ejemplo sobre cómo especificar un controlador de eventos para el evento **ItemSend** del objeto **Application**; para conectar **MyItemSendEventHandler** al objeto **Application** en C\#, cree una instancia del objeto de delegado, pase **MyItemSendEventHandler** al constructor del objeto de delegado y, a continuación, agréguelo al evento **ItemSend** usando el operador +=:

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

En Visual Basic, deberá usar la instrucción **AddHandler** para asociar el evento **ItemSend** al controlador de eventos **MyItemSendEventHandler**:

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a>Vea también

- [Eventos del PIA de Outlook](events-in-the-outlook-pia.md)
- [Objetos del PIA de Outlook](objects-in-the-outlook-pia.md)

