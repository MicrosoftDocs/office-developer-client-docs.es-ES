---
title: Long-Term identificadores de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409226"
---
# <a name="long-term-entry-identifiers"></a>Long-Term identificadores de entrada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de servicios asigna un identificador de entrada a largo plazo a un objeto cuando un objeto requiere un identificador con una vida útil prolongada. Los identificadores de entrada a largo plazo siempre son válidos durante semanas o meses y pueden ser válidos en otras estaciones de trabajo, según el proveedor. Los identificadores a largo plazo creados por proveedores de libretas de direcciones para destinatarios personalizados son universalmente válidos. 
  
Los identificadores de entrada a largo plazo se asignan a almacenes de mensajes, carpetas, mensajes, contenedores de libretas de direcciones, usuarios de mensajería y listas de distribución. Cuando las aplicaciones cliente llaman al método [IMAPIProp::GetProps](imapiprop-getprops.md) de estos objetos, siempre se devuelve un identificador de entrada a largo plazo. 
  
Los identificadores de entrada a largo plazo deben ser únicos en todos los almacenes de mensajes del perfil activo; por lo tanto, cuando se copia un mensaje o carpeta de un almacén de mensajes a otro, se le debe asignar un nuevo identificador de entrada. Cuando se mueve un objeto de almacén de mensajes, el proveedor de almacenamiento de mensajes que implementa el movimiento determina si el identificador de entrada original seguirá siendo válido. Algunos proveedores de servicios asignan nuevos identificadores de entrada a objetos movidos; otros no lo hacen. Si hay un cambio, el nuevo identificador de entrada se incluirá en la información que se pasa a los clientes cuando se les notifica el movimiento. 
  
Normalmente, los proveedores de almacenamiento de mensajes implementan el siguiente comportamiento al mover carpetas:
  
- Cuando se mueve una carpeta de un almacén de mensajes a otro almacén de otro tipo, se garantiza que el identificador de entrada cambie.
    
- Cuando se mueve una carpeta de un almacén de mensajes a otro almacén del mismo tipo, el identificador de entrada casi siempre cambia.
    
- Cuando se mueve una carpeta a otra ubicación dentro del mismo almacén de mensajes, el identificador de entrada puede cambiar o no, según el proveedor del almacén de mensajes.
    
Cambiar el nombre de una carpeta sin cambiar su carpeta principal normalmente no hace que cambie el identificador de entrada. 
  
## <a name="see-also"></a>Consulte también



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

