---
title: NOTIFICACIÓN
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818437"
---
# <a name="notification"></a>NOTIFICACIÓN
 
**Se aplica a**: Outlook 
  
Contiene información sobre un evento que se ha producido y los datos que se ha visto afectados por el evento.
  
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
  
> Tipo de evento de notificación que se ha producido. El valor del miembro **ulEventType** corresponde a la estructura que se incluye en la unión de **info** . El miembro **ulEventType** se puede establecer en uno de los siguientes valores: 
    
 _fnevCriticalError_
  
> Se ha producido un error global, como una sesión de apagado en curso. El miembro de la **información** contiene una estructura [ERROR_NOTIFICATION](error_notification.md) . 
    
 _fnevExtended_
  
> Se ha producido un evento interno definido por un proveedor de servicio en particular. El miembro de la **información** contiene una estructura [EXTENDED_NOTIFICATION](extended_notification.md) . 
    
 _fnevNewMail_
  
> Se ha entregado un mensaje a la correspondiente carpeta para la clase de mensaje de recepción y a la espera de ser procesados. El miembro de la **información** contiene una estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) . 
    
 _fnevObjectCopied_
  
> Se ha copiado un objeto MAPI. El miembro de la **información** contiene una estructura [OBJECT_NOTIFICATION](object_notification.md) . 
    
 _fnevObjectCreated_
  
> Se ha creado un objeto MAPI. El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectDeleted_
  
> Se ha eliminado un objeto MAPI. El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectModified_
  
> Un objeto MAPI ha cambiado. El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectMoved_
  
> Una dirección o el almacén de mensajes se ha movido el objeto de libro. El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** . 
    
 _fnevSearchComplete_
  
> Ha finalizado una operación de búsqueda y los resultados están disponibles. El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** . 
    
 _fnevTableModified_
  
> Ha cambiado la información de una tabla. El miembro de la **información** contiene una estructura [TABLE_NOTIFICATION](table_notification.md) . 
    
**Info**
  
> Unión de las estructuras de notificación que describe los datos afectados para un tipo de evento específico. La estructura que se incluyen en el miembro de la **información** depende del valor del miembro **ulEventType** . 
    
## <a name="remarks"></a>Notas

Una o más estructuras de **notificación** se pasan como parámetros de entrada con cada llamada al método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de un receptor de notificaciones registrados. Las estructuras de **notificación** contienen información acerca de los eventos particulares que se han producido y se describen los objetos afectados. 
  
Antes de que los clientes o proveedores de servicios de recibir una notificación pueden utilizar la estructura para procesar el evento, debe comprobar el tipo de evento como se indica en el miembro **ulEventType** . Por ejemplo, el código de ejemplo que se muestra aquí comprobaciones para la llegada de un nuevo mensaje y al detectar un evento de este tipo, imprime la clase de mensaje del mensaje. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Descripción general de notificación y eventos de notificación.  <br/> |
|[Administrar notificaciones](handling-notifications.md) <br/> |Explicación de cómo los clientes deben controlar las notificaciones.  <br/> |
|[Compatibilidad con la notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Ver también


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Estructuras MAPI](mapi-structures.md)

