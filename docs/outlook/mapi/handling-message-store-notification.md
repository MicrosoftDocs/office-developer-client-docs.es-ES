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
  
Para registrar las notificaciones del almacén de mensajes, llame al método [IMAPISession::Advise](imapisession-advise.md) o [IMsgStore::Advise](imsgstore-advise.md) y especifique un almacén de mensajes, una carpeta o un identificador de entrada de mensaje en el contenido del parámetro _lpEntryID._ Los proveedores de almacenamiento de mensajes admiten notificaciones de objetos y tablas. Si se registra con objetos de almacén de mensajes concretos, con la jerarquía de carpetas y las tablas de contenido que describen estos objetos, o con objetos y tablas depende de las notificaciones que espera ver, de las llamadas que realice para realizar operaciones y de cómo el proveedor de almacenamiento de mensajes admita la notificación. 
  
Dado que MAPI permite flexibilidad en la forma en que los proveedores admiten notificaciones, tenga en cuenta que no siempre recibirá el mismo tipo de notificación en respuesta a un evento determinado de todos los proveedores de al almacenamiento de mensajes. Algunos proveedores de al almacenamiento de mensajes no admiten notificaciones en absoluto. Para determinar si el almacén de mensajes que está usando admite la notificación, busque el bit STORE_NOTIFY_OK en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
En un extremo del espectro de proveedores de al almacenamiento de mensajes que admiten notificaciones se encuentran los proveedores que generan notificaciones "enriquecciones"; estos proveedores envían notificaciones descriptivas para todos los orígenes de avisos registrados. En el otro extremo se encuentran los proveedores de al almacenamiento de mensajes que admiten notificaciones limitadas; estos proveedores envían notificaciones generales para un número restringido de orígenes de avisos. 
  
Por ejemplo, si copia un mensaje en una carpeta con la que se ha registrado para recibir notificaciones de objeto copiado y movido de objeto, puede o no recibir la notificación copiada del objeto. Si lo recibe o no depende de lo siguiente:
  
- El método al que llamó para realizar la copia. Puede ser [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)o [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Cómo implementa el proveedor de almacenamiento de mensajes el método de copia.
    
- Indica si el proveedor del almacén de mensajes admite notificaciones copiadas de objetos en carpetas.
    
Dado que no hay directrices estrictas que describan cómo implementar la notificación de eventos para los proveedores de almacenamiento de mensajes, los clientes no pueden esperar un comportamiento coherente. MAPI hace recomendaciones sobre cómo los proveedores de al almacenamiento de mensajes implementan la notificación de eventos y en la siguiente tabla se describen estas recomendaciones. Lea la tabla de la siguiente manera: después de realizar la operación en la primera columna, espere recibir una notificación del tipo enumerado en la segunda columna si se ha registrado para ese tipo con el objeto enumerado en la tercera columna. Por ejemplo, después de crear una carpeta, recibirá una notificación  _fnevObjectCreated_ solo si se ha registrado para las notificaciones  _fnevObjectCreated_ con el almacén de mensajes. 
  
|**Operación**|**Tipo de evento**|**Origen del aviso**|
|:-----|:-----|:-----|
|Crear una carpeta  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar una carpeta  <br/> | _fnevObjectDeleted_ <br/> |Carpeta De almacenamiento de mensajes eliminada  <br/> |
|Mover una carpeta de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Carpeta De almacenamiento de mensajes movida  <br/> |
|Copiar una carpeta de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Almacén de mensajes y carpeta copiada (no se envía  _ninguna notificación fnevObjectCreated_ para la nueva copia de la carpeta)  <br/> |
|Cambio en una propiedad de carpeta calculada (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Almacén de mensajes Carpeta modificada (sin notificación a la carpeta principal)  <br/> |
|Crear un mensaje  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar un mensaje, lo que provoca un cambio en la propiedad PR_CONTENT_COUNT **carpeta** principal  <br/> | _fnevObjectDeleted_ <br/> |Mensaje eliminado del almacén de mensajes  <br/> |
|Mover un mensaje de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Mensaje movido del almacén de mensajes  <br/> |
|Copiar un mensaje de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Mensaje copiado del almacén de mensajes (no  _fnevObjectCreated_ notification for new copy of the message)  <br/> |
|Guardar un mensaje, lo que provoca un cambio en la propiedad PR_CONTENT_COUNT **carpeta** principal  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes solo al guardar primero  <br/> |
|Guardar un mensaje  <br/> | _fnevObjectModified_ <br/> |Almacén de mensajes al guardar después del primer mensaje modificado guardado (sin notificación a la carpeta principal)  <br/> |
|Completar una operación de búsqueda  <br/> | _fnevSearchComplete_ <br/> |Carpeta de búsqueda del almacén de mensajes  <br/> |
|Mensaje nuevo  <br/> | _fnevNewMail_ <br/> |Almacén de mensajes  <br/> |
   
> [!NOTE]
> Cuando reciba una notificación de modificación de objeto, recuerde que la parte de la matriz de etiquetas de propiedad de la estructura [OBJECT_NOTIFICATION a](object_notification.md) la que apunta el parámetro  _lpNotifications_ en la llamada **OnNotify** puede o no ser NULL. Los proveedores de almacenamiento de mensajes no son necesarios para insertar información de propiedades en esta matriz y la mayoría no lo hacen. Asegúrese de que **el método OnNotify** puede controlar el caso en el que el puntero  _lpPropTagArray_ es NULL. 
  
Para la mayoría, si no todas las notificaciones de objetos, actualice la vista de la carpeta o carpetas afectadas.
  

