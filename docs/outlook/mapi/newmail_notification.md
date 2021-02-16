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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439859"
---
# <a name="newmail_notification"></a>NEWMAIL_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la información relacionada con la llegada de un nuevo mensaje. 
  
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

## <a name="members"></a>Miembros

 **cbEntryID**
  
> Número de bytes en el identificador de entrada al que apunta el **miembro lpEntryID.** 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del mensaje recién llegado.
    
 **cbParentID**
  
> Recuento de bytes en el identificador de entrada al que apunta el **miembro lpParentID.** 
    
 **lpParentID**
  
> Puntero al identificador de entrada de la carpeta de recepción del mensaje recién llegado.
    
 **ulFlags**
  
> Máscara de bits de marcas usadas para describir el formato de las propiedades de cadena incluidas en el mensaje. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.
    
 **lpszMessageClass**
  
> Puntero a la clase de mensaje del mensaje recién llegado. 
    
 **ulMessageFlags**
  
> Máscara de bits de marcas que describe el estado actual del mensaje recién llegado. El **miembro ulMessageFlags** es una copia de la propiedad PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.
    
## <a name="remarks"></a>Comentarios

La **NEWMAIL_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro **de** información de la [estructura notification.](notification.md) Cuando el **miembro de** información de una estructura **notification** contiene una estructura **NEWMAIL_NOTIFICATION,** el miembro **ulEventType** de la estructura **NOTIFICATION** se establece en  _fnevNewMail._
  
MAPI usa la **NEWMAIL_NOTIFICATION** sólo como miembro  de la estructura de notificación, que contiene información sobre un evento de notificación para el receptor de avisos. 
  
Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Discusión sobre cómo los clientes deben controlar las notificaciones.  <br/> |
|[Notificación de eventos de soporte técnico](supporting-event-notification.md) <br/> |Discusión sobre cómo los proveedores de servicios pueden usar [el método IMAPISupport](imapisupportiunknown.md) para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Consulte también



[Notificaci�n](notification.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

