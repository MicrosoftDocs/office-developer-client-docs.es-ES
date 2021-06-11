---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426271"
---
# <a name="status_object_notification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un objeto de estado que se ha visto afectado por un cambio. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Recuento de bytes en el identificador de entrada al que apunta el **miembro lpEntryID.** 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto de estado modificado.
    
 **cValues**
  
> Recuento de [estructuras SPropValue](spropvalue.md) en la matriz señalada por el **miembro lpPropVals.** 
    
 **lpPropVals**
  
> Puntero a una matriz de **estructuras SPropValue** que describen las propiedades del objeto de estado modificado. 
    
## <a name="remarks"></a>Comentarios

La **STATUS_OBJECT_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro **de información** de la estructura [notification.](notification.md) La **STATUS_OBJECT_NOTIFICATION** se incluye con una notificación de objeto de estado para un evento de tipo  _fnevStatusObjectModified_. La notificación de objeto status es una notificación MAPI interna; los clientes y los proveedores de servicios no pueden registrarse y los proveedores de servicios no pueden generarlo.
  
Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Discusión sobre cómo los clientes deben administrar las notificaciones.  <br/> |
|[Notificación de eventos de soporte técnico](supporting-event-notification.md) <br/> |Discusión sobre cómo los proveedores de servicios pueden usar **el método IMAPISupport** para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

