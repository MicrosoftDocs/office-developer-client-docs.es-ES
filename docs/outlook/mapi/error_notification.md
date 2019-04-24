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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335738"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la información relacionada con un error crítico. Esto hace que se genere una notificación de error. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Número de bytes en el identificador de entrada al que apunta **lpEntryID**. 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto que provoca el error.
    
 **SCODE**
  
> Valor de error para el error crítico. 
    
 **ulFlags**
  
> Máscara de la máscara usada para designar el formato del texto al que señala el miembro **lpszError** en la estructura a la que apunta **lpMAPIError**. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 **lpMAPIError**
  
> Puntero a una estructura [MAPIERROR](mapierror.md) que describe el error. 
    
## <a name="remarks"></a>Comentarios

La estructura **ERROR_NOTIFICATION** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) . Cuando el miembro de **información** de una estructura de **notificación** contiene una estructura **ERROR_NOTIFICATION** , el miembro **ulEventType** de la estructura de **notificación** se establece en _fnevCriticalError_.
  
El valor del miembro **cbEntryID** y el miembro **LPENTRYID** puede ser null. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Descripción de cómo deben administrar los clientes las notificaciones.  <br/> |
|[Admitir notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[Notificaci�n](notification.md)


[Estructuras MAPI](mapi-structures.md)

