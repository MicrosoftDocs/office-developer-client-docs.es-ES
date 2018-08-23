---
title: Registrar una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a35add66fb685b3c17464269456edf6b456711e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570215"
---
# <a name="registering-for-a-notification"></a>Registrar una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede registrarse para notificaciones de almacén de mensaje o de la libreta de direcciones como parte de su proceso de inicialización.
  
MAPI admite la notificación en la libreta de direcciones, independientemente de si cualquiera de los proveedores de la libreta de direcciones compatible con. Soporte técnico para la notificación de almacenes de mensaje depende el proveedor de almacenamiento de mensaje en particular. Para determinar si un proveedor de almacén de mensajes determinado admite notificaciones, compruebe su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si el almacén de mensajes es compatible con las notificaciones, se establecerá el bit STORE_NOTIFY_OK. 
  
Registrar para las notificaciones mediante una llamada al método **Advise** de un objeto de origen advise. Muchos objetos implementan **Advise** y los clientes pueden registrar con esos objetos en una variedad de formas. 
  
 **Para registrar una notificación de**
  
1. Crear una MAPI objeto receptor de aviso e incrementar su recuento de referencia.
    
2. Si es necesario, llame a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear un objeto de receptor advise que se ajusta el receptor de notificaciones original, a continuación, el receptor de Consejo original de la versión.. 
    
3. Llame a uno de los siguientes métodos de **Advise** para completar el registro: 
    
  - Llame a [IMAPISession::Advise](imapisession-advise.md) para registrar para las notificaciones de sesión o para las notificaciones en un objeto de almacén de address book o mensaje. 
    
  - Llame a [IAddrBook::Advise](iaddrbook-advise.md) para registrar para las notificaciones de la libreta de direcciones o para las notificaciones en una lista de usuario, el contenedor o la distribución de mensajería. 
    
  - Llame a [IABLogon::Advise](iablogon-advise.md) para registrar directamente con un proveedor de la libreta de direcciones para las notificaciones en una lista de usuario, el contenedor o la distribución de mensajería. 
    
  - Llame a [IMsgStore::Advise](imsgstore-advise.md) para registrar para las notificaciones del almacén de mensajes o para las notificaciones en una carpeta o mensaje. 
    
  - Llame a [IMSLogon::Advise](imslogon-advise.md) para registrar directamente con un proveedor de almacén de mensajes para las notificaciones en una carpeta o mensaje. 
    
  - Llame a [IMAPITable::Advise](imapitable-advise.md) para registrar para las notificaciones de tabla. 
    
4. El número de conexión devuelto desde **Advise**la memoria caché.
    
5. Si usa un receptor de notificaciones ajustadas, liberarlo. Una vez que se registra el receptor de notificaciones ajustado, ya no se necesite.
    
Llamar a ** IMAPISession::Advise ** le permite registrar para las notificaciones de error crítico en la sesión general o de varias notificaciones en objetos individuales. Las sesiones de envían notificaciones de error crítico a los clientes iniciar sesión en sesiones compartidas cuando otro cliente de uso de la sesión compartida llama al método de [IMAPISession::Logoff](imapisession-logoff.md) . Para registrar para las notificaciones de sesión, pase NULL para el parámetro de identificador de entrada. Para registrar las notificaciones de en un objeto individual, pase el identificador de entrada del objeto. El método **IMAPISession** reenvía la llamada al proveedor de servicios adecuado, según lo determinado por la parte **MAPIUID** del identificador de entrada. Al llamar a **IMAPISession::Advise** para registrar las notificaciones del objeto es más sencillo que llamar al método **Advise** de un proveedor de servicios. 
  
Registrar con la libreta de direcciones es similar a registrar con la sesión. Para registrar la notificación de error crítico desde la libreta de direcciones, pase NULL para el identificador de entrada. Para registrar las notificaciones de en un objeto de la libreta de direcciones determinada, especifique el identificador de entrada apropiada y evento o eventos de interés. Tenga en cuenta que muchos de los proveedores de la libreta de direcciones no compatible con las notificaciones en objetos individuales. En su lugar, admiten las notificaciones de tabla en su contenido y las tablas de jerarquía. 
  
Es recomendable para liberar el receptor de notificaciones que implementan o crear con [HrAllocAdviseSink](hrallocadvisesink.md) inmediatamente después de una devolución de una llamada de **Advise** es correcta. Esto es debido a que es posible que los proveedores de servicio liberar el receptor de notificaciones después de la llamada **Advise** , pero antes de una **Unadvise** se realiza la llamada. Una vez que ha proporcionado el origen advise un puntero a su receptor de notificaciones y el recuento de referencia se incrementó en este receptor de notificaciones, es aconsejable liberarlo a menos que tenga un largo plazo usar para él. 
  
> [!NOTE]
> Todos los números de conexión que representan los registros de asesoría al válido no se liberará hasta que se realiza la llamada **Unadvise** . 
  

