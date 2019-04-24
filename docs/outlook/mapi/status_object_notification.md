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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336445"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un objeto status que se ha visto afectado por un cambio. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Número de bytes en el identificador de entrada al que apunta el miembro **lpEntryID** . 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto de estado Changed.
    
 **cValues**
  
> Número de estructuras [SPropValue](spropvalue.md) en la matriz señalada por el miembro **lpPropVals** . 
    
 **lpPropVals**
  
> Puntero a una matriz de estructuras **SPropValue** que describen las propiedades del objeto status modificado. 
    
## <a name="remarks"></a>Comentarios

La estructura **STATUS_OBJECT_NOTIFICATION** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) . La estructura **STATUS_OBJECT_NOTIFICATION** se incluye con una notificación de objeto de estado para un evento de tipo _fnevStatusObjectModified_. La notificación de objeto de estado es una notificación de MAPI interna; los clientes y los proveedores de servicios no pueden registrarse para ti y los proveedores de servicios no pueden generarlos.
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Descripción de cómo deben administrar los clientes las notificaciones.  <br/> |
|[Admitir notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

