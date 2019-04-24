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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341121"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la información relacionada con un evento que es específico del proveedor de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Código de evento extendido definido por el proveedor.
    
 **cb**
  
> Número de bytes en los parámetros específicos de evento señalados por **pbEventParameters**. 
    
 **pbEventParameters**
  
> Puntero a parámetros específicos del evento. El tipo de parámetros que se usa depende del valor del miembro **ulEvent** ; Estos parámetros están documentados por el proveedor que emitió el evento. 
    
## <a name="remarks"></a>Comentarios

La estructura **EXTENDED_NOTIFICATION** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) . Cuando el miembro de **información** de una estructura de **notificación** contiene una estructura **EXTENDED_NOTIFICATION** , el miembro **ulEventType** de la estructura de **notificación** se establece en _fnevExtended_.
  
El evento extendido lo define un proveedor de servicios para representar un tipo de cambio que no puede estar cubierto por ningún otro evento predefinido. Solo los clientes que sepan que deben registrarse antes de que un proveedor de servicios admita un evento extendido pueden registrarse para ese evento. Los clientes no pueden determinar sin conocimiento avanzado si un proveedor de servicios admite un evento extendido. Si un proveedor de servicios admite un evento extendido, muestra cómo controlar dicho evento cuando se recibe.
  
La sesión envía una notificación extendida cuando un cliente cierra sesión. Para registrar esta notificación, llame a [IMAPISession:: Advise](imapisession-advise.md) con el parámetro _LPENTRYID_ establecido en NULL y el parámetro _cbEntryID_ establecido en cero. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Descripción de cómo deben administrar los clientes las notificaciones.  <br/> |
|[Admitir notificación de eventos](supporting-event-notification.md) <br/> |Información sobre cómo los proveedores de servicios pueden usar los métodos de [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)


[Estructuras MAPI](mapi-structures.md)

