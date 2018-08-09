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
ms.openlocfilehash: 5e23d9b829a941e3add8b8d8e137c73052b08aa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19816789"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**Hace referencia a**: Outlook 
  
Describe la información que se relaciona con un evento que es específico del proveedor de servicio. 
  
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

## <a name="members"></a>Members

 **ulEvent**
  
> Código de evento extendido que está definido por el proveedor.
    
 **cb**
  
> Recuento de bytes en los parámetros específicos del evento que señala **pbEventParameters**. 
    
 **pbEventParameters**
  
> Puntero a los parámetros específicos del evento. El tipo de parámetros que se usan depende del valor del miembro **ulEvent** ; Estos parámetros se documentan por el proveedor que ha emitido el evento. 
    
## <a name="remarks"></a>Comentarios

La estructura **EXTENDED_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) . Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **EXTENDED_NOTIFICATION** , se establece el miembro **ulEventType** de la estructura de **notificación** en _fnevExtended_.
  
El evento extendido está definido por un proveedor de servicios para representar un tipo de cambio que no se debe estar cubierto por cualquiera de los demás eventos predefinidos. Solo los clientes que saber antes de que registran que un proveedor de servicios admite un evento extendido pueden registrar para dicho evento. No es posible para los clientes determinar sin conocimientos avanzados si un proveedor de servicios admite un evento extendido. Si un proveedor de servicios admite un evento extendido, se muestra cómo controlar un evento cuando se recibe.
  
Se envía una notificación extendida por la sesión cuando un cliente cierra la sesión. Registre esta notificación mediante una llamada a [IMAPISession::Advise](imapisession-advise.md) con el parámetro _lpEntryID_ establecido en NULL y el parámetro de _cbEntryID_ que se establece en cero. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos de MAPI](event-notification-in-mapi.md) <br/> |Descripción general de notificación y eventos de notificación.  <br/> |
|[Administrar las notificaciones](handling-notifications.md) <br/> |Explicación de cómo los clientes deben controlar las notificaciones.  <br/> |
|[Admitir notificaciones de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar los métodos [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)


[Estructuras MAPI](mapi-structures.md)

