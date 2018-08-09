---
title: Controlar la notificación de almacenamiento de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 898f8b6ff3d0b0dd42a670596b54171f18b4a5e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816941"
---
# <a name="handling-message-store-notification"></a>Controlar la notificación de almacenamiento de mensajes
  
**Hace referencia a**: Outlook 
  
Para registrar las notificaciones del almacén de mensajes, llamar a los métodos [IMAPISession::Advise](imapisession-advise.md) o [IMsgStore::Advise](imsgstore-advise.md) y especificar un almacén de mensajes, la carpeta o el identificador de mensaje de entrada en el contenido del parámetro _lpEntryID_ . Los proveedores de almacén de mensajes admitan notificaciones de objeto y de tabla. Si registrar con objetos de almacén de mensaje en particular, con las tablas de jerarquía y contenido de carpeta que describen estos objetos o con ambos objetos y tablas depende de las notificaciones que esperaba, las llamadas que realice para realizar operaciones, y cómo el proveedor de almacenamiento de mensaje admite la notificación. 
  
Debido a que MAPI permite flexibilidad en el modo en que los proveedores admiten notificaciones, tenga en cuenta que no siempre recibirá el mismo tipo de notificación en respuesta a un evento concreto de todos los proveedores de almacén de mensajes. Algunos proveedores de almacén de mensajes no admiten notificaciones en absoluto. Para determinar si el almacén de mensajes que está utilizando es compatible con notificación, busque el bit STORE_NOTIFY_OK en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
En un extremo del espectro del almacén de mensajes proveedores que admiten la notificación son los proveedores que generan notificaciones "rich"; Estos proveedores de envían notificaciones descriptivas para todos los registrado orígenes de aviso. En el otro extremo está el mensaje de los proveedores de almacén que admiten notificaciones limitadas; Estos proveedores de envían notificaciones general para un número limitado de orígenes de advise. 
  
Por ejemplo, si copia un mensaje a una carpeta con la que se ha registrado para recibir copian ambos objetos y objeto movido las notificaciones, puede o no puede recibir la notificación del objeto copiado. Si recibe depende de:
  
- El método al que llamar para realizar la copia. Esto podría ser [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)o [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Cómo el mensaje almacenar proveedor implementa el método copy.
    
- Si admite o no el proveedor de almacenamiento de mensaje notificaciones de objetos que se copian en las carpetas.
    
Debido a que no hay ningún directrices estrictas que describen cómo implementar la notificación de eventos para el mensaje de los proveedores de almacén, los clientes no se puede esperar un comportamiento coherente. MAPI realizar recomendaciones sobre cómo del almacén de mensajes notificación de evento de implementar proveedores y en la siguiente tabla muestra estas recomendaciones. Leer la tabla de la siguiente manera: después de realizar la operación en la primera columna, espera recibir una notificación de los tipos que aparecen en la segunda columna si se ha registrado para ese tipo de con el objeto que aparece en la tercera columna. Por ejemplo, después de haber creado una carpeta, recibirá una notificación de _fnevObjectCreated_ sólo si se ha registrado para las notificaciones de _fnevObjectCreated_ con el almacén de mensajes. 
  
|**Operation**|**Tipo de evento**|**Origen de aviso**|
|:-----|:-----|:-----|
|Cree una carpeta  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar una carpeta  <br/> | _fnevObjectDeleted_ <br/> |Carpeta eliminados del almacén de mensajes  <br/> |
|Mover una carpeta de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Se movió carpeta del almacén de mensajes  <br/> |
|Copiar una carpeta de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Mensaje de almacenar y copiar carpeta (no se ha enviado para la nueva copia de la carpeta ninguna notificación de _fnevObjectCreated_ )  <br/> |
|Cambio en una propiedad de la carpeta calculado (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Carpeta Changed (ninguna notificación a la carpeta principal) del almacén de mensajes  <br/> |
|Crear un mensaje  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar un mensaje, lo que provoca que un cambio en el elemento primario (propiedad) de la carpeta **PR_CONTENT_COUNT**  <br/> | _fnevObjectDeleted_ <br/> |Mensaje eliminado del almacén de mensajes  <br/> |
|Mover un mensaje de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Se movió mensaje del almacén de mensajes  <br/> |
|Copiar un mensaje de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Almacén de mensajes copiados mensaje (ninguna notificación _fnevObjectCreated_ para la nueva copia del mensaje)  <br/> |
|Guardar un mensaje, lo que provoca que un cambio en el elemento primario (propiedad) de la carpeta **PR_CONTENT_COUNT**  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes Guardar sólo por primera vez  <br/> |
|Guardar un mensaje  <br/> | _fnevObjectModified_ <br/> |Almacén de mensajes en guarda después de la primera guardar el mensaje Changed (ninguna notificación a la carpeta principal)  <br/> |
|Completar una operación de búsqueda  <br/> | _fnevSearchComplete_ <br/> |Carpeta de búsqueda del almacén de mensajes  <br/> |
|Nuevo mensaje  <br/> | _fnevNewMail_ <br/> |Almacén de mensajes  <br/> |
   
> [!NOTE]
> Cuando recibe una notificación de objeto modificado, recuerde que la parte de matriz de etiqueta de propiedad de la estructura [OBJECT_NOTIFICATION](object_notification.md) indicada por el parámetro _lpNotifications_ en la llamada de **OnNotify** puede o no puede ser NULL. Los proveedores de almacén de mensajes no son necesarios para insertar información de la propiedad de esta matriz y no más. Asegúrese de que el método **OnNotify** puede tratar el caso donde el puntero _lpPropTagArray_ es NULL. 
  
Para la mayoría, si no todas las notificaciones de objetos, actualice la vista de la carpeta afectado o carpetas.
  

