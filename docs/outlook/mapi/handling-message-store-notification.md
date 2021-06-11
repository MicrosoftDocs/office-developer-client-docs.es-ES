---
title: Administrar las notificaciones de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d370603dc7cfc015fe7b2757d1cf0525b3092c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428028"
---
# <a name="handling-message-store-notification"></a>Administrar las notificaciones de almacén de mensajes
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para registrar las notificaciones del almacén de mensajes, llame al método [IMAPISession::Advise](imapisession-advise.md) o [IMsgStore::Advise](imsgstore-advise.md) y especifique un identificador de entrada de mensaje, carpeta o almacén de mensajes en el contenido del parámetro _lpEntryID._ Los proveedores de almacén de mensajes admiten notificaciones de objeto y tabla. Tanto si se registra con objetos de almacén de mensajes concretos, con la jerarquía de carpetas y tablas de contenido que describen estos objetos, como con objetos y tablas, depende de las notificaciones que espera ver, las llamadas que realice para realizar operaciones y cómo el proveedor del almacén de mensajes admite la notificación. 
  
Dado que MAPI permite flexibilidad en la forma en que los proveedores admiten notificaciones, tenga en cuenta que no siempre recibirá el mismo tipo de notificación en respuesta a un evento determinado de todos los proveedores de almacén de mensajes. Algunos proveedores de almacén de mensajes no admiten notificaciones en absoluto. Para determinar si el almacén de mensajes que está usando admite la notificación, busque el bit STORE_NOTIFY_OK en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
En un extremo del espectro de proveedores de almacén de mensajes que admiten notificaciones se encuentran los proveedores que generan notificaciones "enriquecciones"; estos proveedores envían notificaciones descriptivas para todos los orígenes de asesoramiento registrados. En el otro extremo se encuentran los proveedores de almacén de mensajes que admiten notificaciones limitadas; estos proveedores envían notificaciones generales para un número restringido de orígenes de asesoramiento. 
  
Por ejemplo, si copia un mensaje en una carpeta con la que se ha registrado para recibir notificaciones de objetos copiados y movidos por objeto, puede o no recibir la notificación copiada del objeto. Si lo recibe o no depende de:
  
- El método al que llamó para realizar la copia. Puede ser [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)o [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Cómo implementa el proveedor del almacén de mensajes el método copy.
    
- Independientemente de si el proveedor del almacén de mensajes admite notificaciones copiadas de objetos en carpetas.
    
Dado que no hay directrices estrictas que describan cómo implementar la notificación de eventos para los proveedores de almacén de mensajes, los clientes no pueden esperar un comportamiento coherente. MAPI hace recomendaciones sobre cómo los proveedores del almacén de mensajes implementan la notificación de eventos y en la tabla siguiente se describen estas recomendaciones. Lea la tabla de la siguiente manera: después de realizar la operación en la primera columna, espere recibir una notificación del tipo enumerado en la segunda columna si se ha registrado para ese tipo con el objeto enumerado en la tercera columna. Por ejemplo, después de crear una carpeta, recibirá una notificación  _fnevObjectCreated_ solo si se ha registrado para las notificaciones  _fnevObjectCreated_ con el almacén de mensajes. 
  
|**Operación**|**Tipo de evento**|**Informar al origen**|
|:-----|:-----|:-----|
|Crear una carpeta  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar una carpeta  <br/> | _fnevObjectDeleted_ <br/> |Carpeta Eliminado del almacén de mensajes  <br/> |
|Mover una carpeta de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Almacén de mensajes Carpeta movida  <br/> |
|Copiar una carpeta de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Almacén de mensajes y carpeta copiada (ninguna  _notificación fnevObjectCreated_ enviada para la nueva copia de la carpeta)  <br/> |
|Cambio en una propiedad de carpeta calculada (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Almacén de mensajes Carpeta modificada (sin notificación a la carpeta principal)  <br/> |
|Crear un mensaje  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar un mensaje, lo que provoca un cambio en la propiedad PR_CONTENT_COUNT **carpeta** primaria  <br/> | _fnevObjectDeleted_ <br/> |Mensaje eliminado del almacén de mensajes  <br/> |
|Mover un mensaje de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Mensaje movido del almacén de mensajes  <br/> |
|Copiar un mensaje de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Almacén de mensajes Mensaje copiado (Sin  _notificación fnevObjectCreated_ para nueva copia del mensaje)  <br/> |
|Guardar un mensaje, lo que provoca un cambio en la propiedad PR_CONTENT_COUNT **carpeta** principal  <br/> | _fnevObjectCreated_ <br/> |Solo el almacén de mensajes en el primer guardado  <br/> |
|Guardar un mensaje  <br/> | _fnevObjectModified_ <br/> |Almacén de mensajes en los guardados después del primer mensaje cambiado guardado (sin notificación a la carpeta principal)  <br/> |
|Completar una operación de búsqueda  <br/> | _fnevSearchComplete_ <br/> |Carpeta de búsqueda del almacén de mensajes  <br/> |
|Nuevo mensaje  <br/> | _fnevNewMail_ <br/> |Almacén de mensajes  <br/> |
   
> [!NOTE]
> Cuando reciba una notificación de modificación de objeto, recuerde que la parte de la matriz de etiquetas de propiedad de la estructura [OBJECT_NOTIFICATION a](object_notification.md) la que apunta el parámetro  _lpNotifications_ en la llamada **OnNotify** puede ser NULL o no. Los proveedores de almacén de mensajes no son necesarios para insertar información de propiedades en esta matriz y la mayoría no lo hacen. Asegúrese de que **el método OnNotify** puede controlar el caso en el que el puntero  _lpPropTagArray_ es NULL. 
  
Para la mayoría, si no todas las notificaciones de objetos, actualice la vista de la carpeta o carpetas afectadas.
  

