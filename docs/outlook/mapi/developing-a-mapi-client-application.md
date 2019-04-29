---
title: Desarrollo de una aplicación de cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410038"
---
# <a name="developing-a-mapi-client-application"></a>Desarrollo de una aplicación de cliente MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente de MAPI se escriben con la interfaz de cliente MAPI orientada a objetos. Los clientes MAPI interactúan con uno o varios sistemas de mensajería a través del subsistema MAPI y los proveedores de servicios compatibles con MAPI. Esta interacción puede producirse de muchas maneras diferentes; hay una variedad enorme en las aplicaciones cliente. La mayoría de los clientes son clientes de mensajería, ya sea integrando la mensajería en su conjunto de características establecido o realizando mensajería como característica principal. Otras características que pueden proporcionar los clientes MAPI son la administración de perfiles o la administración de la libreta de direcciones y el almacén de mensajes.
  
Todos los clientes de mensajería inicializan las bibliotecas MAPI e inician una **sesión** con el subsistema MAPI. Para obtener más información, vea [acceso a objetos mediante la sesión](accessing-objects-by-using-the-session.md). Una vez establecida la sesión, un cliente puede:
  
- Administrar los mensajes salientes, incluidas las respuestas, los mensajes reenviados y las retransmisiones.
    
- Controlar los mensajes entrantes.
    
- Controlar el almacén de mensajes mediante la apertura de carpetas y mensajes, la creación, modificación, copia y el envío de mensajes, el seguimiento de conversaciones y la búsqueda de una o varias carpetas.
    
- Controle la libreta de direcciones mediante la creación y modificación de destinatarios, la ubicación de entradas y el recorrido de la jerarquía de contenedores.
    
- Administrar un proveedor de transporte mediante la realización de una reconfiguración, la configuración de las opciones y el orden de transporte y el envío de mensajes a petición.
    
- Controlar la notificación de eventos.
    
- Controlar los formularios.
    
- Administrar perfiles y servicios de mensajes.
    
Use los temas de esta sección para ayudarle a implementar estas tareas básicas y las características específicas que harán que el cliente MAPI sea único.
  

