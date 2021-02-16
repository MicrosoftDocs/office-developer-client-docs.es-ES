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
  
Identifica de forma única una conexión entre un receptor de avisos, un origen de avisos y MAPI.
  
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
  
> Número de bytes en el **miembro** ab. 
    
 **ab**
  
> Matriz de bytes que describe la clave de notificación.
    
## <a name="remarks"></a>Comentarios

Los [métodos Subscribe](imapisupport-subscribe.md) y [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) usan la estructura **NOTIFKEY** para generar notificaciones al receptor de avisos adecuado sobre el origen de aviso adecuado. 
  
Los proveedores de servicios generan claves de notificación cuando se llama al método **Advise** y quieren llamar a **Subscribe** para controlar el registro de notificaciones y el envío posterior de notificaciones. Una clave de notificación puede ser el identificador de entrada del origen del aviso o puede ser cualquier otro elemento de identificación, como una constante. Por ejemplo, un proveedor de almacenamiento de mensajes puede usar la ruta de acceso de una carpeta como clave de notificación. 
  
La clave de notificación debe funcionar en varios procesos. 
  
Los requisitos de ámbito para una clave de notificación son similares a los de un identificador de entrada a largo plazo. Sin embargo, a diferencia de un identificador de entrada, una clave de notificación debe ser binaria comparable. Normalmente, una clave de notificación incluye un **valor GUID** definido por el proveedor de servicios seguido de otra información específica del proveedor exclusiva del objeto. 
  
Para obtener una explicación del uso de la estructura **NOTIFKEY** para administrar las conexiones entre los receptores de avisos y los objetos que generan las notificaciones, consulte Notificación de eventos [de soporte](supporting-event-notification.md)técnico. 
  
## <a name="see-also"></a>Consulte también



[Estructuras MAPI](mapi-structures.md)

