---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 876c8fc3667929e3c2e7403e71e6d392981d34f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573358"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene información sobre un objeto que ha sufrido un cambio, como que se copian o modificado.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a>Miembros

 **cbEntryID**
  
> Recuento de bytes en el identificador de entrada que señala el miembro **lpEntryID** . 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto afectado.
    
 **ulObjType**
  
> Tipo de objeto afectado. Tipos posibles son los siguientes:
    
MAPI_STORE 
  
> Almacén de mensajes. 
    
MAPI_ADDRBOOK 
  
> Libreta de direcciones. 
    
MAPI_FOLDER 
  
> Carpeta.
    
MAPI_ABCONT 
  
> Contenedor de la libreta de direcciones.
    
MAPI_MESSAGE 
  
> Mensaje.
    
MAPI_MAILUSER 
  
> Usuario de mensajería.
    
MAPI_ATTACH 
  
> Objeto Attachment.
    
MAPI_DISTLIST 
  
> Lista de distribución.
    
MAPI_PROFSECT 
  
> Sección de perfil.
    
MAPI_STATUS 
  
> Objeto de estado.
    
MAPI_SESSION 
  
> Objeto de sesión.
    
 **cbParentID**
  
> Recuento de bytes en el identificador de entrada que señala el miembro **lpParentID** . 
    
 **lpParentID**
  
> Puntero al identificador de entrada del elemento primario del objeto afectado.
    
 **cbOldID**
  
> Recuento de bytes en el identificador de entrada que señala el miembro **lpOldID** . 
    
 **lpOldID**
  
> Puntero al identificador de entrada del objeto original. Este puntero puede ser NULL si el evento no requiere un objeto original.
    
 **cbOldParentID**
  
> Recuento de bytes en el identificador de entrada que señala el miembro **lpOldParentID** . 
    
 **lpOldParentID**
  
> Puntero al identificador de entrada del elemento primario del objeto original. Este puntero puede ser NULL si el evento no requiere un objeto original.
    
 **lpPropTagArray**
  
> Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad que identifica propiedades afectadas por el evento. 
    
## <a name="remarks"></a>Comentarios

La estructura **OBJECT_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) . Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **OBJECT_NOTIFICATION** , el miembro **ulEventType** de la estructura de **notificación** se establece en uno de los siguientes tipos de eventos: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
El evento de búsqueda completa, representado por el tipo de evento fnevSearchComplete, indica que se ha completado la búsqueda inicial del dominio para la carpeta de una búsqueda.
  
Los siguientes miembros que contienen información sobre el objeto original se usan sólo en los eventos de mover y copiar. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Estos miembros no se aplican a los otros tipos de eventos.
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Descripción general de notificación y eventos de notificación.  <br/> |
|[Administrar notificaciones](handling-notifications.md) <br/> |Explicación de cómo los clientes deben controlar las notificaciones.  <br/> |
|[Compatibilidad con la notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Estructuras MAPI](mapi-structures.md)

