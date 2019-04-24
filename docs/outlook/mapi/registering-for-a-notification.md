---
title: Registro de una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328409"
---
# <a name="registering-for-a-notification"></a>Registro de una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede registrarse para la libreta de direcciones o notificaciones de almacén de mensajes como parte de su proceso de inicialización.
  
MAPI admite la notificación en la libreta de direcciones independientemente de si alguno de los proveedores de la libreta de direcciones lo admite. La compatibilidad con la notificación en almacenes de mensajes depende del proveedor de almacén de mensajes en particular. Para determinar si un proveedor de almacén de mensajes determinado admite notificaciones, compruebe su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si el almacén de mensajes admite notificaciones, se establecerá el bit STORE_NOTIFY_OK. 
  
Para registrarse en el caso de las notificaciones, llame **** al método Advise del objeto de origen Advise. Muchos objetos implementan **Advise** y los clientes se pueden registrar con estos objetos de varias maneras. 
  
 **Para registrar una notificación**
  
1. Cree un objeto receptor de notificaciones MAPI e incremente su recuento de referencia.
    
2. Si corresponde, llame a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear un objeto de notificación de notificaciones que contenga el receptor de notificaciones original y, a continuación, libere el receptor de avisos original.. 
    
3. Llame a uno de los siguientes métodos de **aviso** para completar el registro: 
    
  - Llame a [IMAPISession:: Advise](imapisession-advise.md) para registrarse para notificaciones de sesión o para notificaciones en un objeto de almacén de mensajes o de la libreta de direcciones. 
    
  - Llame a [IAddrBook:: Advise](iaddrbook-advise.md) para registrarse en las notificaciones de la libreta de direcciones o para las notificaciones en un usuario de mensajería, un contenedor o una lista de distribución. 
    
  - Llame a [IABLogon:: Advise](iablogon-advise.md) para registrarse directamente con un proveedor de libreta de direcciones para notificaciones en un usuario de mensajería, un contenedor o una lista de distribución. 
    
  - Llame a [IMsgStore:: Advise](imsgstore-advise.md) para registrarse en las notificaciones del almacén de mensajes o para las notificaciones de una carpeta o un mensaje. 
    
  - Llame a [IMSLogon:: Advise](imslogon-advise.md) para registrarse directamente con un proveedor de almacenamiento de mensajes para notificaciones de una carpeta o un mensaje. 
    
  - Llame al [IMAPITable:: Advise](imapitable-advise.md) para registrarse en las notificaciones de tabla. 
    
4. Cache el número de conexión devuelto por **Advise**.
    
5. Si usa un receptor de notificaciones englobado, suéltelo. Una vez registrado el receptor de notificaciones de contenido, ya no lo necesita.
    
Llamar a * * IMAPISession:: adVise * * le permite registrarse para recibir notificaciones de errores críticos en la sesión general o para varias notificaciones de objetos individuales. Las sesiones envían notificaciones de errores críticos a los clientes que han iniciado sesión en sesiones compartidas cuando otro cliente que utiliza la sesión compartida llama al método [IMAPISession:: Logoff](imapisession-logoff.md) . Para registrarse para las notificaciones de sesión, pase NULL para el parámetro de identificador de entrada. Para registrar las notificaciones en un objeto individual, pase el identificador de entrada del objeto. El método **IMAPISession** reenvía la llamada al proveedor de servicios adecuado, según determine la parte **MAPIUID** del identificador de entrada. Llamar a **IMAPISession:: Advise** para registrar las notificaciones de objeto es más sencillo que llamar al método Advise de un proveedor de servicios. **** 
  
Registrarse con la libreta de direcciones es similar a registrarse en la sesión. Para registrarse para recibir una notificación de error crítico de la libreta de direcciones, pase NULL para el identificador de entrada. Para registrarse en el caso de las notificaciones de un objeto de la libreta de direcciones en particular, especifique el identificador de entrada adecuado y el evento o eventos de interés. Tenga en cuenta que muchos proveedores de libretas de direcciones no admiten notificaciones en objetos individuales. En su lugar, admiten notificaciones de tabla en sus tablas de contenido y jerarquía. 
  
Se recomienda liberar el receptor de notificaciones que se implementa o se crea con [HrAllocAdviseSink](hrallocadvisesink.md) inmediatamente después de una devolución correcta de **** una llamada de Advise. Esto se debe a que es posible que los proveedores de servicios liberen su receptor **** de notificaciones después de la llamada a Advise, pero antes de que se realice una llamada de unaconsejable. **** Una vez que haya dado al origen del aviso un puntero a su receptor de notificaciones y el recuento de referencia se ha incrementado en este receptor de notificaciones, es aconsejable liberarlo a menos que tenga un uso a largo plazo para él. 
  
> [!NOTE]
> Todos los números de conexión que representan registros de asesoría válidos no se publicarán hasta que se realice la llamada de **Unadvise** . 
  

