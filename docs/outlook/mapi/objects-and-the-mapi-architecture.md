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
  
Todos los objetos que define MAPI están en una o más capas de la arquitectura MAPI. La capa de interfaz de cliente contiene todos los objetos que puede implementar una aplicación cliente, un visor de formularios o un servidor de formulario. La capa de interfaz del proveedor de servicios contiene los objetos que puede implementar un proveedor de servicios de cualquier tipo. Esta capa incluye objetos implementados por libretas de direcciones, almacenes de mensajes, proveedores de transporte y bibliotecas de formularios. La capa que representa el subsistema MAPI se coloca entre las capas de interfaz de cliente y proveedor de servicios. La capa MAPI contiene todos los objetos que MAPI implementa para que los clientes o proveedores de servicios los usen. 
  
En la siguiente ilustración se muestra dónde encaja cada uno de los objetos MAPI en la arquitectura MAPI. Los objetos se representan con los nombres de sus interfaces derivadas. Por ejemplo, un objeto receptor de aviso se muestra como [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), la interfaz que deriva de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) y que cada objeto receptor de aviso implementa. Varios componentes usan o implementan las interfaces que unen capas. Aunque la capa MAPI parece separar las capas de cliente y proveedor, lo que implica que toda la comunicación debe fluir a través de MAPI, este no es el caso. Los clientes pueden comunicarse directamente con objetos del proveedor de servicios. 
  
**Capas de objetos en MAPI**
  
![Capas de objetos en capas de]objetos MAPI en(media/amapi_38.gif "MAPI")
  
## <a name="see-also"></a>Consulte también

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Información general sobre el objeto MAPI y la interfaz](mapi-object-and-interface-overview.md)

