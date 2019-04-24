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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279794"
---
# <a name="objects-and-the-mapi-architecture"></a>Objetos y la arquitectura MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los objetos que define MAPI se clasifican en una o más capas de la arquitectura MAPI. La capa de interfaz de cliente contiene todos los objetos que puede implementar una aplicación cliente, un visor de formularios o un servidor de formularios. La capa de interfaz del proveedor de servicios contiene los objetos que puede implementar un proveedor de servicios de cualquier tipo. Esta capa incluye objetos implementados por las libretas de direcciones, los almacenes de mensajes, los proveedores de transporte y las bibliotecas de formularios. La capa que representa el subsistema MAPI está colocada entre las capas de la interfaz del proveedor de servicios y del cliente. La capa MAPI contiene todos los objetos que implementa MAPI para que los clientes o proveedores de servicios usen. 
  
En la siguiente ilustración se muestra dónde encaja cada uno de los objetos MAPI en la arquitectura MAPI. Los objetos se representan con los nombres de sus interfaces derivadas. Por ejemplo, un objeto de notificación de aviso se muestra como [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), la interfaz que se deriva de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) y que cada objeto de notificación de aviso implementa. Las interfaces que conforman las capas de puente se usan o implementan en varios componentes. A pesar de que la capa MAPI parece separar las capas del proveedor y del cliente, lo que implica que toda la comunicación debe fluir a través de MAPI, no es así. Los clientes pueden comunicarse directamente con los objetos de proveedor de servicios. 
  
**Capas de objetos en MAPI**
  
![Capas de objetos en MAPI] (media/amapi_38.gif "Capas de objetos en MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

