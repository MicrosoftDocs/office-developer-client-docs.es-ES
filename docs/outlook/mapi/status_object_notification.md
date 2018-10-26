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
ms.openlocfilehash: ba93cd0343121751ab12514fe3f09e5a480d5b23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582276"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Miembros

 **cbEntryID**
  
> Recuento de bytes en el identificador de entrada que señala el miembro **lpEntryID** . 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto estado cambiado.
    
 **cValues**
  
> Recuento de las estructuras de [SPropValue](spropvalue.md) en la matriz indicada por el miembro **lpPropVals** . 
    
 **lpPropVals**
  
> Puntero a una matriz de estructuras **SPropValue** que describen las propiedades del objeto de estado cambiado. 
    
## <a name="remarks"></a>Comentarios

La estructura **STATUS_OBJECT_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) . La estructura **STATUS_OBJECT_NOTIFICATION** se incluye con una notificación de objeto de estado para un evento de tipo _fnevStatusObjectModified_. Notificación de estado de objeto es una notificación de MAPI interno; los clientes y proveedores de servicios no se pueden registrar para él y proveedores de servicios lo no pueden generar.
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Descripción general de notificación y eventos de notificación.  <br/> |
|[Administrar notificaciones](handling-notifications.md) <br/> |Explicación de cómo los clientes deben controlar las notificaciones.  <br/> |
|[Compatibilidad con la notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

