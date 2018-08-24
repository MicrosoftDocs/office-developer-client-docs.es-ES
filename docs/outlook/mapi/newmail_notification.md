---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 779585f73a7032ae0259b30ebfc16868c733c7fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569515"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Describe la información que se relacionan con la llegada de un nuevo mensaje. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Recuento de bytes en el identificador de entrada que señala el miembro **lpEntryID** . 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del mensaje recién llegado.
    
 **cbParentID**
  
> Recuento de bytes en el identificador de entrada que señala el miembro **lpParentID** . 
    
 **lpParentID**
  
> Puntero al identificador de entrada de la carpeta de recepción para el mensaje recién llegado.
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para describir el formato de las propiedades de cadena incluido con el mensaje. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 **lpszMessageClass**
  
> Puntero a la clase de mensaje del mensaje recién llegado. 
    
 **ulMessageFlags**
  
> Máscara de bits de indicadores que describe el estado actual del mensaje recién llegado. El miembro **ulMessageFlags** es una copia de la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
## <a name="remarks"></a>Comentarios

La estructura **NEWMAIL_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) . Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **NEWMAIL_NOTIFICATION** , se establece el miembro **ulEventType** de la estructura de **notificación** en _fnevNewMail._
  
MAPI utiliza la estructura **NEWMAIL_NOTIFICATION** sólo como un miembro de la estructura de **notificación** , que contiene información acerca de un evento de notificación para el receptor de notificaciones. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos de MAPI](event-notification-in-mapi.md) <br/> |Descripción general de notificación y eventos de notificación.  <br/> |
|[Administrar las notificaciones](handling-notifications.md) <br/> |Explicación de cómo los clientes deben controlar las notificaciones.  <br/> |
|[Admitir notificaciones de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

