---
title: Identificadores de entrada a largo plazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 589420db48edb348a22f34ce72b948f4d8207ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818043"
---
# <a name="long-term-entry-identifiers"></a>Identificadores de entrada a largo plazo

  
  
**Hace referencia a**: Outlook 
  
Cuando un objeto requiere un identificador con una duración de tiempo prolongado, se asigna un identificador de entrada a largo plazo por un proveedor de servicios a un objeto. Los identificadores de entrada a largo plazo siempre son válidos para semanas o meses y pueden ser válidos en otras estaciones de trabajo, según el proveedor. Los identificadores a largo plazo creados por los proveedores de la libreta de direcciones para los destinatarios personalizados son válidos todo el mundo. 
  
Los identificadores de entrada a largo plazo se asignan a los almacenes de mensajes, carpetas, mensajes, contenedores de la libreta de direcciones, mensajería a los usuarios y distribución listas. Cuando las aplicaciones cliente de llaman al método [IMAPIProp::GetProps](imapiprop-getprops.md) de estos objetos, siempre es un identificador de entrada a largo plazo que se devuelve. 
  
Los identificadores de entrada a largo plazo deben ser únicos en todos los almacenes de mensajes en el perfil activo; por lo tanto, cuando un mensaje o una carpeta se copia desde el almacén de mensajes de uno a otro, se debe asignar un nuevo identificador de entrada. Cuando se mueve un objeto de almacén de mensajes, el proveedor de almacén de mensajes que implementa el movimiento determina si el identificador de entrada original seguirá siendo válido. Algunos proveedores de servicios de asignan los identificadores de entrada nueva a los objetos que se ha movido; otros no lo hacen. Si se produce un cambio, el nuevo identificador de entrada se incluirá en la información que se pasan a los clientes cuando reciben notificaciones del movimiento. 
  
Normalmente, los proveedores de almacén de mensajes implementan el siguiente comportamiento cuando se mueven las carpetas:
  
- Cuando se mueve una carpeta desde el almacén de mensajes de uno a otro almacén de un tipo diferente, se garantiza que el identificador de entrada cambia.
    
- Cuando se mueve una carpeta desde el almacén de mensajes de uno a otro almacén del mismo tipo, casi siempre se cambia el identificador de entrada.
    
- Cuando se mueve una carpeta a otra ubicación dentro del mismo almacén de mensajes, el identificador de entrada puede o no puede cambiar, según el proveedor de almacén de mensajes.
    
Cambio de nombre de una carpeta sin cambiar su carpeta principal normalmente no hace que el identificador de entrada cambiar. 
  
## <a name="see-also"></a>Vea también



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

