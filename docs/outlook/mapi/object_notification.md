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
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430171"
---
# <a name="object_notification"></a>OBJECT_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información sobre un objeto que se ha sometido a un cambio, como copiarse o modificarse.
  
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
  
> Número de bytes en el identificador de entrada al que apunta el **miembro lpEntryID.** 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto afectado.
    
 **ulObjType**
  
> Tipo de objeto afectado. Los tipos posibles son los siguientes:
    
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
  
> Datos adjuntos.
    
MAPI_DISTLIST 
  
> Lista de distribución.
    
MAPI_PROFSECT 
  
> Sección de perfil.
    
MAPI_STATUS 
  
> Objeto Status.
    
MAPI_SESSION 
  
> Objeto Session.
    
 **cbParentID**
  
> Recuento de bytes en el identificador de entrada al que apunta el **miembro lpParentID.** 
    
 **lpParentID**
  
> Puntero al identificador de entrada del objeto primario del objeto afectado.
    
 **cbOldID**
  
> Recuento de bytes en el identificador de entrada al que apunta el **miembro lpOldID.** 
    
 **lpOldID**
  
> Puntero al identificador de entrada del objeto original. Este puntero puede ser NULL si el evento no requiere un objeto original.
    
 **cbOldParentID**
  
> Recuento de bytes en el identificador de entrada al que apunta el **miembro lpOldParentID.** 
    
 **lpOldParentID**
  
> Puntero al identificador de entrada del objeto primario del objeto original. Este puntero puede ser NULL si el evento no requiere un objeto original.
    
 **lpPropTagArray**
  
> Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad que identifican las propiedades afectadas por el evento. 
    
## <a name="remarks"></a>Comentarios

La **OBJECT_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro **de** información de la [estructura notification.](notification.md) Cuando el miembro  **de** información de una estructura notification contiene una estructura **OBJECT_NOTIFICATION,** el miembro **ulEventType** de la estructura **NOTIFICATION** se establece en uno de los siguientes tipos de eventos: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
El evento de búsqueda completa, representado por el tipo de evento fnevSearchComplete, indica que se ha completado la búsqueda inicial del dominio para una carpeta de búsqueda.
  
Los siguientes miembros que contienen información sobre el objeto original solo se usan en eventos de movimiento y copia. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Estos miembros no se aplican a los otros tipos de eventos.
  
Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Discusión sobre cómo los clientes deben controlar las notificaciones.  <br/> |
|[Notificación de eventos de soporte técnico](supporting-event-notification.md) <br/> |Discusión sobre cómo los proveedores de servicios pueden usar [el método IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Consulte también



[Notificaci�n](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Estructuras MAPI](mapi-structures.md)

