---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425445"
---
# <a name="error_notification"></a>ERROR_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la información relacionada con un error crítico. Esto hace que se genere una notificación de error. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a>Members

 **cbEntryID**
  
> Recuento de bytes en el identificador de entrada señalado por **lpEntryID**. 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto que provoca el error.
    
 **scode**
  
> Valor de error para el error crítico. 
    
 **ulFlags**
  
> Máscara de bits de las marcas usadas para designar el formato del texto al que apunta el miembro **lpszError** en la estructura señalada por **lpMAPIError**. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
 **lpMAPIError**
  
> Puntero a una [estructura MAPIERROR](mapierror.md) que describe el error. 
    
## <a name="remarks"></a>Comentarios

La **ERROR_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el **miembro info** de la estructura [NOTIFICATION.](notification.md) Cuando el **miembro info** de una estructura **NOTIFICATION** contiene una estructura **ERROR_NOTIFICATION,** el **miembro ulEventType** de la estructura **NOTIFICATION** se establece en  _fnevCriticalError_.
  
El valor del **miembro cbEntryID** y el **miembro lpEntryID** puede ser NULL. 
  
Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Discusión sobre cómo los clientes deben administrar las notificaciones.  <br/> |
|[Notificación de eventos de soporte técnico](supporting-event-notification.md) <br/> |Discusión sobre cómo los proveedores de servicios pueden usar **el método IMAPISupport** para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[Notificaci�n](notification.md)


[Estructuras MAPI](mapi-structures.md)

