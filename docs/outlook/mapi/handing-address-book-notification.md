---
title: Administrar las notificaciones de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413538"
---
# <a name="handing-address-book-notification"></a>Administrar las notificaciones de la libreta de direcciones
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las notificaciones de la libreta de direcciones permiten a un cliente conocer los eventos que se producen en cualquier entrada de la libreta de direcciones o en una entrada determinada. Puede registrarse para estas notificaciones a través de la libreta de direcciones MAPI llamando a [IAddrBook::Advise](iaddrbook-advise.md) o a través de la jerarquía o la tabla de contenido de un contenedor de libreta de direcciones llamando a [IMAPITable::Advise](imapitable-advise.md). 
  
Especifique el identificador de entrada de un contenedor de libreta de direcciones, una lista de distribución o un usuario de mensajería si está registrando notificaciones en una entrada determinada y NULL si se registra para notificaciones en toda la libreta de direcciones. El identificador de entrada debe representar un usuario de mensajería o una lista de distribución en un contenedor de libreta de direcciones. **IAddrBook::Advise** examina este identificador de entrada para determinar qué proveedor de libreta de direcciones es responsable del objeto correspondiente y reenvía la llamada al método [IABLogon::Advise](iablogon-advise.md) del proveedor de libreta de direcciones correspondiente. 
  
Los clientes pueden registrarse para los siguientes tipos de eventos en las entradas de la libreta de direcciones:
  
- Error crítico
    
- Cualquiera de los eventos de objeto (creado, modificado, eliminado, movido o copiado)
    
- Tabla modificada
    
Normalmente, el registro solo se produce en el contenido del contenedor de la libreta de direcciones y en las tablas de jerarquía. Es raro que los clientes se registren con los objetos de lista de distribución y usuario de mensajería de nivel inferior. Esto se debe a:
  
- Muchos proveedores de libretas de direcciones no admiten notificaciones en sus listas de distribución y usuarios de mensajería.
    
- Las notificaciones de tabla son suficientes para realizar un seguimiento de los cambios y notificarlos a los usuarios.
    

