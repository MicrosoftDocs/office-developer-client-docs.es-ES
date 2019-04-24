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
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307787"
---
# <a name="long-term-entry-identifiers"></a>Identificadores de entrada a largo plazo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de servicios asigna un identificador de entrada a largo plazo a un objeto cuando un objeto requiere un identificador con una duración prolongada. Los identificadores de entrada a largo plazo siempre son válidos durante semanas o meses y pueden ser válidos en otras estaciones de trabajo, según el proveedor. Los identificadores a largo plazo creados por los proveedores de libreta de direcciones para destinatarios personalizados son universalmente válidos. 
  
Los identificadores de entrada a largo plazo se asignan a los almacenes de mensajes, carpetas, mensajes, contenedores de libretas de direcciones, usuarios de mensajería y listas de distribución. Cuando las aplicaciones cliente llaman al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de estos objetos, siempre es un identificador de entrada a largo plazo que se devuelve. 
  
Los identificadores de entrada a largo plazo deben ser únicos en todos los almacenes de mensajes del perfil activo; por lo tanto, cuando se copia un mensaje o una carpeta de un almacén de mensajes a otro, se le debe asignar un nuevo identificador de entrada. Cuando se mueve un objeto de almacén de mensajes, el proveedor de almacenamiento de mensajes que implementa el movimiento determina si el identificador de entrada original seguirá siendo válido. Algunos proveedores de servicios asignan nuevos identificadores de entrada a los objetos movidos; otros no. Si hay un cambio, el nuevo identificador de entrada se incluirá en la información que se pasa a los clientes cuando se les notifica el movimiento. 
  
Normalmente, los proveedores de almacenamiento de mensajes implementan el comportamiento siguiente cuando mueven carpetas:
  
- Cuando se mueve una carpeta de un almacén de mensajes a otro almacén de un tipo diferente, se garantiza que el identificador de entrada cambiará.
    
- Cuando se mueve una carpeta de un almacén de mensajes a otro almacén del mismo tipo, el identificador de entrada casi siempre cambia.
    
- Cuando se mueve una carpeta a otra ubicación dentro del mismo almacén de mensajes, el identificador de entrada puede o no cambiar según el proveedor de almacenamiento de mensajes.
    
El cambio de nombre de una carpeta sin cambiar la carpeta principal normalmente no hace que cambie el identificador de entrada. 
  
## <a name="see-also"></a>Vea también



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

