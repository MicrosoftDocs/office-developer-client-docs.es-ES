---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415722"
---
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la información relacionada con un evento específico del proveedor de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a>Miembros

 **ulEvent**
  
> Código de evento extendido definido por el proveedor.
    
 **cb**
  
> Recuento de bytes en los parámetros específicos del evento a los que apunta **pbEventParameters**. 
    
 **pbEventParameters**
  
> Puntero a parámetros específicos del evento. El tipo de parámetros que se usan depende del valor del **miembro ulEvent;** estos parámetros los documenta el proveedor que emitió el evento. 
    
## <a name="remarks"></a>Comentarios

La **EXTENDED_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro **de** información de la [estructura notification.](notification.md) Cuando el miembro  **de** información de una estructura notification contiene una estructura **EXTENDED_NOTIFICATION,** el miembro **ulEventType** de la estructura **NOTIFICATION** se establece en _fnevExtended_.
  
El evento extendido lo define un proveedor de servicios para representar un tipo de cambio que no puede estar cubierto por ninguno de los demás eventos predefinidos. Solo los clientes que sepan antes de registrar que un proveedor de servicios admite un evento extendido pueden registrarse para ese evento. No es posible que los clientes determinen sin conocimientos avanzados si un proveedor de servicios admite un evento extendido. Si un proveedor de servicios admite un evento extendido, muestra cómo controlar dicho evento cuando se recibe.
  
La sesión envía una notificación extendida cuando un cliente cierra sesión. Regístrese para esta notificación llamando a [IMAPISession::Advise](imapisession-advise.md) con el parámetro  _lpEntryID_ establecido en NULL y el parámetro  _cbEntryID_ establecido en cero. 
  
Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Discusión sobre cómo deben administrarse las notificaciones los clientes.  <br/> |
|[Notificación de eventos de soporte técnico](supporting-event-notification.md) <br/> |Discusión sobre cómo los proveedores de servicios pueden usar [los métodos IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Consulte también



[Notificaci�n](notification.md)


[Estructuras MAPI](mapi-structures.md)

