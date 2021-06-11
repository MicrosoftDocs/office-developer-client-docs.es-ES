---
title: Desarrollo de una aplicación cliente MAPI
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
# <a name="developing-a-mapi-client-application"></a>Desarrollo de una aplicación cliente MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente MAPI se escriben con la interfaz de cliente MAPI orientada a objetos. Los clientes MAPI interactúan con uno o varios sistemas de mensajería a través del subsistema MAPI y los proveedores de servicios compatibles con MAPI. Esta interacción puede producirse de muchas maneras diferentes; hay una gran variedad en las aplicaciones cliente. La mayoría de los clientes son clientes de mensajería, ya sea integrando la mensajería en su conjunto de características establecido o realizando la mensajería como su característica principal. Otras características que pueden proporcionar los clientes MAPI son la administración de perfiles o la libreta de direcciones y la administración del almacén de mensajes.
  
Todos los clientes de mensajería inicializan las bibliotecas MAPI e inician una **sesión** con el subsistema MAPI. Para obtener más información, vea [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md). Una vez establecida una sesión, un cliente puede:
  
- Controla los mensajes salientes, incluidas las respuestas, los mensajes reenviados y las retransmisiones.
    
- Controlar los mensajes entrantes.
    
- Controla el almacén de mensajes abriendo carpetas y mensajes, creando, modificando, copiando y enviando mensajes, rastreando conversaciones y buscando una o varias carpetas.
    
- Controla la libreta de direcciones creando y modificando destinatarios, localizando entradas y recorriendo la jerarquía de contenedores.
    
- Controla un proveedor de transporte mediante la reconfiguración, la configuración de opciones y el orden de transporte y el envío de mensajes a petición.
    
- Controlar la notificación de eventos.
    
- Controlar formularios.
    
- Controlar los perfiles y los servicios de mensajes.
    
Use los temas de esta sección para ayudarle a implementar estas tareas básicas y las características específicas que harán que su cliente MAPI sea único.
  

