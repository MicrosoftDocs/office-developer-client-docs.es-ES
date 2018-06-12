---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3c480c420753b2da6c57b3961589d5c2e2e8022a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818429"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Se aplica a**: Outlook 
  
Identifica exclusivamente una conexión entre un receptor con notificación, un origen de advise y MAPI.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Miembros

 **cb**
  
> Recuento de bytes en el miembro **ab** . 
    
 **AB**
  
> Matriz de bytes que describe la clave de notificación.
    
## <a name="remarks"></a>Notas

Los métodos [suscribir](imapisupport-subscribe.md) y [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) usan la estructura **NOTIFKEY** para generar las notificaciones para el receptor de notificaciones adecuados sobre el origen de advise adecuado. 
  
Proveedores de servicios de generan claves de notificación cuando se llama a su método **Advise** y deseen llamar **suscribirse** para controlar el registro de la notificación y el envío subsiguientes de notificaciones. Una clave de notificación puede ser el identificador de entrada del origen de advise o puede ser cualquier otro elemento de identificación, como una constante. Por ejemplo, un proveedor de almacén de mensajes es posible que use la ruta de acceso de una carpeta como su clave de notificación. 
  
La clave de notificación debe trabajar a través de varios procesos. 
  
Los requisitos de ámbito para una clave de notificación son similares a las de un identificador de entrada a largo plazo. Sin embargo, a diferencia de un identificador de entrada, una clave de notificación debe ser binario comparable. Normalmente, una clave de notificación incluye un valor **GUID** definido por el proveedor de servicios seguido de otra información específica del proveedor único para el objeto. 
  
Para obtener una descripción del uso de la estructura **NOTIFKEY** para administrar las conexiones entre los receptores advise y los objetos que generan las notificaciones, vea [Compatibilidad con notificación de evento](supporting-event-notification.md). 
  
## <a name="see-also"></a>Ver también



[Estructuras MAPI](mapi-structures.md)

