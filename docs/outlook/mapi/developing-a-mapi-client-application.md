---
title: Desarrollar una aplicación de cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 42558fcc3d94b108c0dabb92d62f7c61fdf3039f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816666"
---
# <a name="developing-a-mapi-client-application"></a>Desarrollar una aplicación de cliente MAPI

  
  
**Hace referencia a**: Outlook 
  
Las aplicaciones cliente MAPI se escriben con la interfaz de cliente MAPI orientado a objetos. Los clientes MAPI interactúan con uno o varios sistemas de mensajería a través de los proveedores de servicio compatible con MAPI y el subsistema MAPI. Esta interacción puede producirse de muchas maneras diferentes; hay una enorme diversidad en aplicaciones cliente. La mayoría de los clientes son clientes, ya sea la integración de mensajería en su conjunto de características establecida o realización de mensajería como su característica principal de mensajería. Otras características que es posible que proporcionan los clientes MAPI son la administración de perfiles o mensaje y la libreta de direcciones del almacén de administración.
  
Todos los clientes de mensajería inicialización las bibliotecas de MAPI e iniciar una **sesión** con el subsistema MAPI. Para obtener más información, vea [Obtener acceso a objetos mediante el uso de la sesión](accessing-objects-by-using-the-session.md). Después de que se ha establecido una sesión, un cliente puede:
  
- Controlar los mensajes salientes, incluidas las respuestas, reenviado mensajes y retransmisiones.
    
- Administrar los mensajes entrantes.
    
- Controlar el almacén de mensajes por abrir carpetas y mensajes, crear, modificar, copiar y envío de mensajes, las conversaciones de seguimiento y una o varias carpetas de búsqueda.
    
- Controlar la libreta de direcciones mediante la creación y modificación de los destinatarios, buscar las entradas y atravesar la jerarquía de contenedor.
    
- Controlan un proveedor de transporte mediante la realización de reconfiguración, establecer el orden de las opciones y el transporte y enviar mensajes a petición.
    
- Controlar la notificación de evento.
    
- Administrar formularios.
    
- Administrar perfiles y servicios de mensajes.
    
Utilice los temas de esta sección para ayudarle a implementar estas tareas básicas y las características específicas que harán que el cliente MAPI único.
  

