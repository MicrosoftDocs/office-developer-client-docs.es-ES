---
title: Información sobre la indexación de almacenes basada en notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816355"
---
# <a name="about-notification-based-store-indexing"></a>Información sobre la indexación de almacenes basada en notificaciones

  
  
**Hace referencia a**: Outlook 
  
Un proveedor de almacén MAPI puede especificar si los mensajes de los rastreos de controlador de protocolo MAPI y los índices en el almacén, o si el almacén envía notificaciones al indizador cuando hay mensajes que se va a indizar. Se conoce como indización de notificación y un almacén que admite la indización de notificación es un conocido como un almacén de empuje.
  
Un proveedor de almacenamiento que admite la marca **STORE_PUSHER_OK** de conjuntos de indización basada en notificación en la propiedad **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** . El controlador de protocolo MAPI o un cliente puede obtener la propiedad **PR_STORE_SUPPORT_MASK** para determinar las características del almacén. 
  
Cada vez que hay un archivo adjunto, carpeta o un mensaje que se va a indizar, el proveedor de almacenamiento genera una MAPI localizador de recursos (URL) que identifica el objeto que se va a indizar y lo envía al indizador. Esta dirección URL de MAPI está codificada en Unicode y debe identificar de forma exclusiva el objeto para el controlador de protocolo MAPI. Para obtener más información acerca de las direcciones URL de MAPI, vea [Acerca de direcciones URL MAPI para indización basada en notificaciones](about-mapi-urls-for-notification-based-indexing.md).
  
Debido a que un indizador siempre no puede indizar todo el contenido antes de que se produce un apagado en un almacén de empuje, debe conservar el almacén de empuje lo que necesita que se va a insertar. Cuando un proveedor de almacén envía una notificación sobre un objeto que se debe indizar, especifica el tipo de notificación **fnevIndexing** en el miembro **ulEventType** de la estructura de **[notificación](notification.md)** . El miembro de la **información** de la estructura de **notificación** contiene una estructura **[EXTENDED_NOTIFICATION](extended_notification.md)** . El proveedor de almacenamiento identifica el proceso en la propiedad **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** . También identifica el proceso de la estructura de [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) y pasa esta información como parte del miembro **pbEventParameters** de la estructura **EXTENDED_NOTIFICATION** . Si el proceso se cierra o se bloquea, el controlador de protocolo MAPI podrán detectar inmediatamente y detener el almacén de empuje de indización. 
  
## <a name="see-also"></a>Vea también



[Información sobre la API del almacén](about-the-store-api.md)
  
[Constantes MAPI](mapi-constants.md)

