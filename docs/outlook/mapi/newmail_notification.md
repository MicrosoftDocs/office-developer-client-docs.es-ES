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
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326246"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la información relacionada con la llegada de un mensaje nuevo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Número de bytes en el identificador de entrada al que apunta el miembro **lpEntryID** . 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del mensaje recién llegado.
    
 **cbParentID**
  
> Número de bytes en el identificador de entrada al que apunta el miembro **lpParentID** . 
    
 **lpParentID**
  
> Puntero al identificador de entrada de la carpeta de recepción del mensaje recién llegado.
    
 **ulFlags**
  
> Máscara de la máscara usada para describir el formato de las propiedades de cadena incluidas en el mensaje. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 **lpszMessageClass**
  
> Puntero a la clase de mensaje del mensaje recién llegado. 
    
 **ulMessageFlags**
  
> Máscara de la máscara de los marcadores que describe el estado actual del mensaje recién llegado. El miembro **ulMessageFlags** es una copia de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.
    
## <a name="remarks"></a>Comentarios

La estructura **NEWMAIL_NOTIFICATION** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) . Cuando el miembro de **información** de una estructura de **notificación** contiene una estructura **NEWMAIL_NOTIFICATION** , el miembro **ulEventType** de la estructura de **notificación** se establece en _fnevNewMail._
  
MAPI usa la estructura **NEWMAIL_NOTIFICATION** sólo como miembro de la estructura de **notificación** , que contiene información acerca de un evento de notificación para el receptor de notificaciones. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Descripción de cómo deben administrar los clientes las notificaciones.  <br/> |
|[Admitir notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[Notificaci�n](notification.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

