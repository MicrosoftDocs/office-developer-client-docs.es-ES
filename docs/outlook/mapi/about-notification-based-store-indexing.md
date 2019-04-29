---
title: Acerca de la indización de almacén basada en notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409177"
---
# <a name="about-notification-based-store-indexing"></a>Acerca de la indización de almacén basada en notificaciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de almacén MAPI puede especificar si el controlador de protocolo MAPI rastrea e indiza los mensajes del almacén, o si el almacén envía notificaciones al indizador cuando hay mensajes que se van a indizar. Este último se conoce como indización basada en notificaciones y un almacén que admite la indización basada en notificaciones es conocido como almacén de extracción.
  
Un proveedor de almacenamiento que admite la indización basada en notificaciones establece la marca **STORE_PUSHER_OK** en la propiedad **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** . El controlador del protocolo MAPI o un cliente puede obtener la propiedad **PR_STORE_SUPPORT_MASK** para determinar las características del almacén. 
  
Siempre que hay un dato adjunto, una carpeta o un mensaje que se va a indizar, el proveedor del almacén genera un localizador uniforme de recursos (URL) de MAPI que identifica el objeto que se va a indizar y lo envía al indizador. Esta dirección URL MAPI se codifica en Unicode y debe identificar de forma única el objeto en el controlador de protocolo MAPI. Para obtener más información acerca de las direcciones URL de MAPI, vea acerca de las [direcciones URL MAPI para la indizaCión basada en notificaciones](about-mapi-urls-for-notification-based-indexing.md).
  
Dado que un indizador no siempre puede indizar todos los elementos antes de que se produzca el cierre en un almacén de inserción, el almacén de inserción debe persistir lo que deba insertarse. Cuando un proveedor de almacén envía una notificación sobre un objeto que debe indizarse, especifica el tipo de notificación **fnevIndexing** en el miembro **ulEventType** de la estructura de **[notificación](notification.md)** . El miembro **información** de la estructura **notificación** contiene una estructura ** [EXTENDED_NOTIFICATION](extended_notification.md)**. El proveedor de almacenamiento identifica el proceso en la propiedad **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** . También identifica el proceso en la estructura [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) y pasa esta información como parte del miembro **pbEventParameters** de la estructura **EXTENDED_NOTIFICATION** . Si el proceso se apaga o se bloquea, el controlador del protocolo MAPI podrá detectar de inmediato y detener la indización del almacén de inserción. 
  
## <a name="see-also"></a>Ver también



[Información sobre la API del almacén](about-the-store-api.md)
  
[Constantes MAPI](mapi-constants.md)

