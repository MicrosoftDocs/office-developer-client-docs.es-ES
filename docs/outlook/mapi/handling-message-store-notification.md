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
  
Para registrarse en las notificaciones del almacén de mensajes, llame al método [IMAPISession:: Advise](imapisession-advise.md) o [IMsgStore:: Advise](imsgstore-advise.md) y especifique un almacén de mensajes, una carpeta o un identificador de entrada de mensaje en el contenido del parámetro _lpEntryID_ . Los proveedores de almacenamiento de mensajes admiten notificaciones de objetos y tablas. Tanto si se registra con objetos de almacén de mensajes concretos, como en las tablas de contenido y jerarquía de carpetas que describen estos objetos, o con objetos y tablas, depende de las notificaciones que se espera ver, las llamadas que se realizan para realizar operaciones y cómo el proveedor de almacenamiento de mensajes admite la notificación. 
  
Como MAPI permite flexibilidad en el modo en que los proveedores admiten las notificaciones, tenga en cuenta que no siempre recibirá el mismo tipo de notificación en respuesta a un evento concreto de todos los proveedores de almacenamiento de mensajes. Algunos proveedores de almacenamiento de mensajes no admiten notificaciones en absoluto. Para determinar si el almacén de mensajes que está usando admite la notificación, busque el bit STORE_NOTIFY_OK en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
En un extremo del espectro de proveedores de almacenamiento de mensajes que admiten notificaciones se encuentran los proveedores que generan notificaciones "enriquecidas"; estos proveedores envían notificaciones descriptivas para todos los orígenes de avisos registrados. En el otro extremo están los proveedores de almacenamiento de mensajes que admiten notificaciones limitadas; estos proveedores envían notificaciones generales para un número restringido de orígenes de notificaciones. 
  
Por ejemplo, si copia un mensaje en una carpeta con la que ha registrado para recibir notificaciones de objetos copiados y movidos de objetos, es posible que no reciba la notificación copiada del objeto. Si lo recibe depende de:
  
- El método al que ha llamado para realizar la copia. Puede ser [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIProp:: CopyTo](imapiprop-copyto.md)o [IMAPIProp:: CopyProps](imapiprop-copyprops.md).
    
- Cómo el proveedor de almacenamiento de mensajes implementa el método de copia.
    
- Si el proveedor de almacenamiento de mensajes admite o no notificaciones copiadas de objetos en las carpetas.
    
Debido a que no hay instrucciones estrictas que describan cómo implementar la notificación de eventos para los proveedores de almacenamiento de mensajes, los clientes no pueden esperar un comportamiento coherente. MAPI hace recomendaciones en cuanto a cómo implementan los proveedores de almacenamiento de mensajes la notificación de eventos y en la tabla siguiente se describen estas recomendaciones. Lea la tabla de la siguiente manera: después de realizar la operación en la primera columna, espere recibir una notificación del tipo enumerado en la segunda columna si se ha registrado para ese tipo con el objeto que aparece en la tercera columna. Por ejemplo, una vez que haya creado una carpeta, recibirá una notificación de _fnevObjectCreated_ solo si se ha registrado para notificaciones de _fnevObjectCreated_ con el almacén de mensajes. 
  
|**Operación**|**Tipo de evento**|**Informar al origen**|
|:-----|:-----|:-----|
|Crear una carpeta  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar una carpeta  <br/> | _fnevObjectDeleted_ <br/> |Carpeta eliminada del almacén de mensajes  <br/> |
|Mover una carpeta de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Carpeta movida del almacén de mensajes  <br/> |
|Copiar una carpeta de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Almacén de mensajes y carpeta copiada (no se ha enviado ninguna notificación _fnevObjectCreated_ para la nueva copia de la carpeta)  <br/> |
|Cambio en una propiedad de carpeta calculada (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)) **, PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Carpeta modificada del almacén de mensajes (sin notificación a la carpeta principal)  <br/> |
|Crear un mensaje  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes  <br/> |
|Eliminar un mensaje, lo que provoca un cambio en la propiedad **PR_CONTENT_COUNT** de la carpeta principal  <br/> | _fnevObjectDeleted_ <br/> |Mensaje eliminado del almacén de mensajes  <br/> |
|Mover un mensaje de una carpeta a otra  <br/> | _fnevObjectMoved_ <br/> |Mensaje movido al almacén de mensajes  <br/> |
|Copiar un mensaje de una carpeta a otra  <br/> | _fnevObjectCopied_ <br/> |Mensaje copiado del almacén de mensajes (sin notificación de _fnevObjectCreated_ para una nueva copia del mensaje)  <br/> |
|Guardar un mensaje, lo que provoca un cambio en la propiedad **PR_CONTENT_COUNT** de la carpeta principal  <br/> | _fnevObjectCreated_ <br/> |Almacén de mensajes en el primer solo guardado  <br/> |
|Guardar un mensaje  <br/> | _fnevObjectModified_ <br/> |Almacén de mensajes al guardar después de la primera vez que ha cambiado el mensaje (sin notificación a la carpeta principal)  <br/> |
|Completar una operación de búsqueda  <br/> | _fnevSearchComplete_ <br/> |Carpeta de búsqueda del almacén de mensajes  <br/> |
|Nuevo mensaje  <br/> | _fnevNewMail_ <br/> |Almacén de mensajes  <br/> |
   
> [!NOTE]
> Cuando recibe una notificación de modificación de objeto, recuerde que la parte de matriz de etiquetas de propiedad de la estructura [OBJECT_NOTIFICATION](object_notification.md) apuntado por el parámetro _lpNotifications_ en la llamada a la función de la función **Notify** puede o no ser null. No es necesario que los proveedores de almacenamiento de mensajes inserten información de propiedades en esta matriz y la mayoría no lo son. Asegúrese de que **** el método alnotify puede controlar el caso en el que el puntero _lpPropTagArray_ es NULL. 
  
Para la mayoría de las notificaciones de objeto, si no todas, actualice la vista de la carpeta o carpetas afectadas.
  

