---
title: Entrega de notificación de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816922"
---
# <a name="handing-address-book-notification"></a>Entrega de notificación de la libreta de direcciones
  
**Se aplica a**: Outlook 
  
Las notificaciones de la libreta de direcciones, permitir que un cliente obtener más información de eventos que se producen en cualquier entrada de la libreta de direcciones o en un valor determinado. Se pueden registrar para estas notificaciones a través de la libreta de direcciones MAPI mediante una llamada a [IAddrBook::Advise](iaddrbook-advise.md) o a través de la jerarquía de un contenedor de la libreta de direcciones o una tabla de contenido mediante una llamada a [IMAPITable::Advise](imapitable-advise.md). 
  
Especifique el identificador de entrada de un contenedor de la libreta de direcciones, una lista de distribución o un usuario de mensajería si va a registrar para las notificaciones en una entrada en particular y NULL si se registra para las notificaciones en la libreta de direcciones completa. El identificador de entrada debe representar un usuario de mensajería o lista de distribución en un contenedor de la libreta de direcciones. **IAddrBook::Advise** examina este identificador de entrada para determinar qué dirección proveedor de libretas es responsable del objeto correspondiente y reenvía la llamada al método de [IABLogon::Advise](iablogon-advise.md) del proveedor de la libreta de dirección adecuada. 
  
Los clientes pueden registrar para los siguientes tipos de eventos en las entradas de la libreta de direcciones:
  
- Error crítico
    
- Cualquiera de los eventos del objeto (creado, modificado, eliminado, movido o copiado)
    
- Tabla modificado
    
Normalmente, el registro se produce sólo en el contenido del contenedor de la libreta de direcciones y las tablas de jerarquía. Es muy poco frecuente que los clientes registren con los objetos de lista de distribución y de usuario de mensajería de nivel inferior. Esto es debido a que:
  
- Muchos de los proveedores de la libreta de direcciones no admiten notificaciones en sus listas de distribución y usuarios de mensajería.
    
- Las notificaciones de tabla son suficientes para el seguimiento de los cambios e informando de ellos a los usuarios.
    

