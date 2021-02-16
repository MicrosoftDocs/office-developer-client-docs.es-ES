---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432880"
---
# <a name="notification"></a>NOTIFICATION
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información sobre un evento que se ha producido y los datos que se han visto afectados por el evento.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a>Miembros

**ulEventType**
  
> Tipo de evento de notificación que se ha producido. El valor del **miembro ulEventType** corresponde a la estructura que se incluye en la unión **de** información. El **miembro ulEventType** se puede establecer en uno de los siguientes valores: 
    
 _fnevCriticalError_
  
> Se ha producido un error global, como un cierre de sesión en curso. El **miembro** de información contiene [una ERROR_NOTIFICATION](error_notification.md) de datos. 
    
 _fnevExtended_
  
> Se ha producido un evento interno definido por un proveedor de servicios determinado. El **miembro** de información contiene [una EXTENDED_NOTIFICATION](extended_notification.md) datos. 
    
 _fnevNewMail_
  
> Se ha entregado un mensaje a la carpeta de recepción adecuada para la clase de mensaje y está esperando a ser procesado. El **miembro** de información contiene [una NEWMAIL_NOTIFICATION](newmail_notification.md) de datos. 
    
 _fnevObjectCopied_
  
> Se ha copiado un objeto MAPI. El **miembro** de información contiene [una OBJECT_NOTIFICATION](object_notification.md) de datos. 
    
 _fnevObjectCreated_
  
> Se ha creado un objeto MAPI. El **miembro** de información contiene **una OBJECT_NOTIFICATION** de datos. 
    
 _fnevObjectDeleted_
  
> Se ha eliminado un objeto MAPI. El **miembro** de información contiene **una OBJECT_NOTIFICATION** de datos. 
    
 _fnevObjectModified_
  
> Un objeto MAPI ha cambiado. El **miembro** de información contiene **una OBJECT_NOTIFICATION** de datos. 
    
 _fnevObjectMoved_
  
> Se ha movido un almacén de mensajes o un objeto de libreta de direcciones. El **miembro** de información contiene **una OBJECT_NOTIFICATION** de datos. 
    
 _fnevSearchComplete_
  
> Una operación de búsqueda ha finalizado y los resultados están disponibles. El **miembro** de información contiene **una OBJECT_NOTIFICATION** de datos. 
    
 _fnevTableModified_
  
> La información de una tabla ha cambiado. El **miembro** de información contiene [una TABLE_NOTIFICATION](table_notification.md) de datos. 
    
**info**
  
> Unión de estructuras de notificación que describen los datos afectados para un tipo determinado de evento. La estructura incluida en el **miembro de** información depende del valor del **miembro ulEventType.** 
    
## <a name="remarks"></a>Comentarios

Una o más estructuras **de** notificación se pasan como parámetros de entrada con cada llamada al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de un receptor de aviso registrado. Las **estructuras notification** contienen información sobre los eventos concretos que se han producido y describen los objetos afectados. 
  
Para que los clientes o proveedores de servicios que reciban una notificación puedan usar la estructura para procesar el evento, deben comprobar el tipo de evento tal como se indica en el **miembro ulEventType.** Por ejemplo, el ejemplo de código que se muestra aquí comprueba la llegada de un mensaje nuevo y, al detectar un evento de este tipo, imprime la clase de mensaje del mensaje. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Discusión sobre cómo deben administrarse las notificaciones los clientes.  <br/> |
|[Notificación de eventos de soporte técnico](supporting-event-notification.md) <br/> |Discusión sobre cómo los proveedores de servicios pueden usar [el método IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Consulte también


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Estructuras MAPI](mapi-structures.md)

