---
title: Objetos y la arquitectura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391049"
---
# <a name="objects-and-the-mapi-architecture"></a>Objetos y la arquitectura MAPI

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Todos los objetos que define MAPI se dividen en una o más capas en la arquitectura de MAPI. La capa de interfaz de cliente contiene todos los objetos que puede implementar una aplicación cliente, el Visor de formulario o el servidor de formulario. La capa de interfaz de proveedor de servicio contiene los objetos que puede implementar un proveedor de servicios de cualquier tipo. Esta capa incluye objetos implementados por libretas de direcciones, almacenes de mensajes, los proveedores de transporte y las bibliotecas de formularios. La capa que representa el subsistema MAPI se coloca entre las capas de interfaz de proveedor de cliente y el servicio. La capa MAPI contiene todos los objetos que implementa MAPI para que los clientes o proveedores de servicios para utilizar. 
  
La siguiente ilustración se muestra donde cada uno de los objetos MAPI encaja en la arquitectura MAPI. Los objetos se representan con los nombres de sus interfaces derivadas. Por ejemplo, se muestra un objeto de receptor advise como [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), la interfaz que se deriva de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) y que cada objeto de receptor advise implementa. Las interfaces que capas de puente se usa o implementadas por varios componentes. Aunque la capa MAPI aparece separar los niveles de cliente y de proveedor, lo que implica que deben flujo de todas las comunicaciones a través de MAPI, no es el caso. Los clientes pueden y comunicarse directamente a los objetos de proveedor de servicio. 
  
**Capas de objetos en MAPI**
  
![Capas de objetos en MAPI] (media/amapi_38.gif "Capas de objetos en MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

