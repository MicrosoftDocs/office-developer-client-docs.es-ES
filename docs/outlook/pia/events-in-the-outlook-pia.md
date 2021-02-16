---
title: Eventos del PIA de Outlook
TOCTitle: Events in the Outlook PIA
ms:assetid: 1f9eafb3-6645-4e27-81fa-5d73bf94ae40
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb644571(v=office.15)
ms:contentKeyID: 55119782
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29217a633c02390587a370847291ef62d5621ce8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325795"
---
# <a name="events-in-the-outlook-pia"></a>Eventos del PIA de Outlook

Al examinar el ensamblado de interoperabilidad primario (PIA) de Outlook, es posible que note que muchas interfaces y muchos delegados de eventos tienen nombres que son nombres conocidos de objetos y eventos del modelo de objetos de Outlook. A diferencia de la biblioteca de tipos COM, los eventos en el PIA de Outlook no están definidos en la misma interfaz como métodos y propiedades del mismo objeto. Las interfaces, los delegados y las clases auxiliares de receptores relacionados con eventos se importan o se crean a fin de que sean compatibles con los eventos del PIA de Outlook. En este tema, se describen las interfaces, los delegados y las clases auxiliares de receptores relacionados con eventos.

## <a name="where-do-the-event-interfaces-delegates-and-sink-helper-classes-come-from"></a>Origen de interfaces, delegados y clases auxiliares de receptores de eventos

Para crear el PIA, Outlook usa el importador de la biblioteca de tipos (TLBIMP) en .NET Framework para convertir definiciones de tipo de la biblioteca de tipos COM en definiciones equivalentes de un ensamblado de Common Language Runtime (CLR). TLBIMP importa los siguientes dos tipos de interfaces para cada objeto:

  - La interfaz principal (por ejemplo, la interfaz [\_Application](https://msdn.microsoft.com/library/bb611255\(v=office.15\)))

  - La interfaz de eventos (por ejemplo, la interfaz [\_ApplicationEvents](https://msdn.microsoft.com/library/bb609229\(v=office.15\))11)

TLBIMP procesa las interfaces importadas y crea varias interfaces, delegados y clases, incluida la interfaz .NET (por ejemplo, la interfaz [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))). Si el objeto tiene eventos, se crea lo siguiente:

  - La interfaz de eventos .NET (por ejemplo, la interfaz [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)))

  - El delegado para cada evento (por ejemplo, el delegado [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\)))

  - La clase auxiliar de receptores (por ejemplo, la clase [ApplicationEvents\_11\_SinkHelper](https://msdn.microsoft.com/library/bb609842\(v=office.15\)))

### <a name="multiple-versions-of-events"></a>Varias versiones de eventos

Algunos objetos que existieron en varias versiones de Outlook tienen implementaciones diferentes de eventos en las distintas versiones, y se les ha agregado eventos adicionales a medida que se han publicado nuevas versiones. A fin de admitir eventos que varían según la versión, Outlook distingue estas interfaces, delegados y clases relacionados con eventos mediante la incorporación de un número de versión en el nombre. Por ejemplo:

  - En las interfaces de eventos importadas del objeto **Application** se incluyen:
    
      - La versión más antigua para Outlook 98 y Outlook 2000: la interfaz [ApplicationEvents](https://msdn.microsoft.com/library/bb644093\(v=office.15\))
    
      - La versión para Outlook 2002: la interfaz [ApplicationEvents\_10](https://msdn.microsoft.com/library/bb647702\(v=office.15\))
    
      - La versión para Outlook 2003 y versiones posteriores: la interfaz [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\))

  - En las interfaces .NET creadas por TLBIMP para el objeto **Application** se incluyen:
    
      - La versión más antigua para Outlook 98 y Outlook 2000: la interfaz [ApplicationEvents\_Event](https://msdn.microsoft.com/library/bb609380\(v=office.15\))
    
      - La versión para Outlook 2002: la interfaz [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\))
    
      - La versión para Outlook 2003 y versiones posteriores: la interfaz [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\))

  - Los delegados que TLBIMP crea para cada evento en cada versión del objeto **Application**, por ejemplo, un delegado para cada versión del evento ItemSend:
    
      - La versión más antigua para Outlook 98 y Outlook 2000: el delegado [ApplicationEvents\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb622515\(v=office.15\))
    
      - La versión para Outlook 2002: el delegado [ApplicationEvents\_10\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb646436\(v=office.15\))
    
      - La versión para Outlook 2003 y versiones posteriores: el delegado [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\))

Como es lógico, los eventos que se agregan a una versión posterior no aparecen en las interfaces de eventos de versiones anteriores y no tienen delegados correspondientes en versiones anteriores. Por ejemplo, el evento [AttachmentSelectionChange](https://msdn.microsoft.com/library/ff184926\(v=office.15\)) se agregó al objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) en Outlook 2010 y, por lo tanto, no forma parte de las interfaces de eventos anteriores del objeto Explorer:

  - Interfaz ExplorerEvents

  - Interfaz ExplorerEvents\_Event

Por otro lado, puede encontrar el evento en la interfaz de eventos .NET más reciente, ExplorerEvents\_10\_Event, y su delegado para la versión de Outlook 2010, [ExplorerEvents\_10\_AttachmentSelectionChangeEventHandler](https://msdn.microsoft.com/library/ff185177\(v=office.15\)).

## <a name="what-the-event-interfaces-delegates-and-sink-helper-classes-are-for"></a>Para qué sirven las interfaces, los delegados y las clases auxiliares de receptores de eventos

Con el objeto **Application** como ejemplo, esta sección describe qué contienen las interfaces y clases indicadas anteriormente:

  - La interfaz principal, \_Application, define todos los métodos y las propiedades de Application. Salvo en un caso que se describe más adelante, esta interfaz no suele usarse en el código.

  - Las interfaces de eventos importadas por TLBIMP, como ApplicationEvents\_11 y ApplicationEvents\_10, definen métodos que se asignan a eventos de Application en la versión correspondiente de Outlook. Esta interfaz no se usa en el código.

  - Las interfaces de eventos creadas por TLBIMP, como ApplicationEvents\_11\_Event y ApplicationEvents\_10\_Event, definen todos los eventos de Application en la versión correspondiente de Outlook. Cuando se diseña un controlador de eventos para un evento en una versión en particular, se debe implementar el controlador de eventos como método y se debe conectar el método al evento definido en la versión correspondiente de la interfaz de eventos .NET.  Salvo en un caso que se analiza a continuación, normalmente no se hace referencia a la interfaz de eventos en el código.

  - La interfaz .NET, Application, hereda la interfaz \_Application y la interfaz ApplicationEvents\_11\_Event. Generalmente, esta es la única interfaz que se usa en código administrado para obtener acceso al objeto, método y propiedad, y a los últimos miembros de eventos del objeto **Application**. No obstante, hay dos excepciones en las que para conectarse a un evento no se usa la interfaz .NET, sino una interfaz diferente:
    
      - Al obtener acceso a un evento que comparte el mismo nombre que un método de ese objeto, debe realizar la conversión a la interfaz de eventos adecuada para conectarse al evento. Por ejemplo, para conectarse al evento [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)), debe realizar la conversión a la interfaz ApplicationEvents\_11\_Event.
    
      - Al conectarse a una versión anterior de un evento que se ha ampliado posteriormente en una versión posterior de Outlook, debe conectarse a la versión del evento de la interfaz anterior. Por ejemplo, si quiere conectarse a la versión del evento Quit del objeto **Application** implementado para Outlook 2002 en lugar de a la última versión, conéctese al evento [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) definido en la interfaz ApplicationEvents\_10\_Event, en lugar de al evento Quit definido en la interfaz ApplicationEvents\_11\_Event.

  - Los delegados ofrecen un marco para crear controladores personalizados para eventos específicos en una versión específica de Outlook. Por ejemplo, si quiere agregar una comprobación de la existencia de una línea de asunto en un elemento de Outlook antes de enviarlo, implemente la comprobación en un método callback que tenga la misma firma que el delegado, ApplicationEvents\_11\_ItemSendEventHandler. Después conecte el método callback como controlador de eventos para el evento ItemSend definido en la interfaz ApplicationEvents\_11\_Event. Para obtener más información sobre cómo conectar el método callback como controlador de eventos para un objeto, consulte [Conexión con controladores de eventos personalizados](connecting-to-custom-event-handlers.md).

  - Las clases SinkHelper creadas por TLBIMP, por ejemplo, ApplicationEvents\_11\_SinkHelper y [ApplicationEvents\_10\_SinkHelper](https://msdn.microsoft.com/library/bb644070\(v=office.15\)), son objetos auxiliares de eventos para eventos Application en la versión correspondiente de Outlook. No deben usarse estas clases en el código.

## <a name="see-also"></a>Vea también

- [Relación del PIA de Outlook con el modelo de objetos](relating-the-outlook-pia-with-the-object-model.md)
- [Objetos del PIA de Outlook](objects-in-the-outlook-pia.md)
- [Métodos y propiedades del PIA de Outlook](methods-and-properties-in-the-outlook-pia.md)
- [Desarrollo de complementos de Outlook administrados con el PIA de Outlook](developing-managed-outlook-add-ins-using-the-outlook-pia.md)

