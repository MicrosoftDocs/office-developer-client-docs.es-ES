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
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816774"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**Hace referencia a**: Outlook 
  
Describe la información que se relacionan con un error crítico. Esto hace que se genere una notificación de error. 
  
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
  
> Recuento de bytes en el identificador de entrada que señala **lpEntryID**. 
    
 **lpEntryID**
  
> Puntero al identificador de entrada del objeto que provoca el error.
    
 **SCODE**
  
> Valor de error para el error crítico. 
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato del texto que señala el miembro **lpszError** en la estructura que señala **lpMAPIError**. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 **lpMAPIError**
  
> Puntero a una estructura [MAPIERROR](mapierror.md) que describe el error. 
    
## <a name="remarks"></a>Comentarios

La estructura **ERROR_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) . Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **ERROR_NOTIFICATION** , se establece el miembro **ulEventType** de la estructura de **notificación** en _fnevCriticalError_.
  
El valor del miembro **cbEntryID** y el miembro **lpEntryID** puede ser NULL. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos de MAPI](event-notification-in-mapi.md) <br/> |Descripción general de notificación y eventos de notificación.  <br/> |
|[Administrar las notificaciones](handling-notifications.md) <br/> |Explicación de cómo los clientes deben controlar las notificaciones.  <br/> |
|[Admitir notificaciones de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[Notificaci�n](notification.md)


[Estructuras MAPI](mapi-structures.md)

