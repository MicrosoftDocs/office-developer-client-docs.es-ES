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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429631"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Identifica de forma única una conexión entre un receptor de notificaciones, un origen de notificaciones y MAPI.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Members

 **cb**
  
> Número de bytes en el miembro **AB** . 
    
 **listín**
  
> Matriz de bytes que describe la clave de notificación.
    
## <a name="remarks"></a>Comentarios

Los métodos [subscribe](imapisupport-subscribe.md) y [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) usan la estructura **NOTIFKEY** para generar notificaciones al receptor de notificaciones adecuado sobre el origen de la notificación correspondiente. 
  
Los proveedores de servicios generan claves de **** notificación cuando se llama a su método Advise y quieren llamar a **subscribe** para controlar el registro de notificaciones y el envío posterior de notificaciones. Una clave de notificación puede ser el identificador de entrada del origen de Advise o puede ser cualquier otro elemento de identificación, como una constante. Por ejemplo, un proveedor de almacenamiento de mensajes podría usar la ruta de acceso de una carpeta como su clave de notificación. 
  
La clave de notificación debe funcionar en varios procesos. 
  
Los requisitos de ámbito de una clave de notificación son similares a los de un identificador de entrada a largo plazo. Sin embargo, a diferencia de un identificador de entrada, una clave de notificación debe ser de comparación binaria. Normalmente, una clave de notificación incluye un valor **GUID** definido por el proveedor de servicios seguido de otra información específica del proveedor que es única para el objeto. 
  
Para obtener una descripción del uso de la estructura **NOTIFKEY** para administrar las conexiones entre los receptores de notificaciones y los objetos que generan las notificaciones, consulte [Supporting Event Notification](supporting-event-notification.md). 
  
## <a name="see-also"></a>Ver también



[Estructuras MAPI](mapi-structures.md)

