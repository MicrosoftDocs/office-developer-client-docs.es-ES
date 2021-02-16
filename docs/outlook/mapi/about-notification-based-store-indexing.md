---
title: Acerca Notification-Based indexación de la Tienda
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
# <a name="about-notification-based-store-indexing"></a>Acerca Notification-Based indexación de la Tienda

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de almacén MAPI puede especificar si el controlador de protocolo MAPI rastrea e indiza los mensajes del almacén, o si el almacén envía notificaciones al indizador cuando hay mensajes que se van a indizar. Este último se conoce como indización basada en notificaciones y un almacén que admite la indización basada en notificaciones es un conocido como almacén de pusher.
  
Un proveedor de almacén que admite la indización basada en notificaciones establece STORE_PUSHER_OK **marca** en la **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** propiedad. El controlador de protocolo MAPI o un cliente puede obtener **la PR_STORE_SUPPORT_MASK** propiedad para determinar las características del almacén. 
  
Siempre que haya datos adjuntos, una carpeta o un mensaje que se indexe, el proveedor de almacenamiento genera un localizador uniforme de recursos (URL) MAPI que identifica el objeto que se va a indizar y lo envía al indizador. Esta dirección URL MAPI está codificada en Unicode y debe identificar de forma única el objeto para el controlador de protocolo MAPI. Para obtener más información acerca de las direcciones URL DE MAPI, vea Acerca de las [direcciones URL mapi Notification-Based indización.](about-mapi-urls-for-notification-based-indexing.md)
  
Dado que un indizador no siempre puede indizar todo antes de que se produzca un apagado en un almacén de pusher, el almacén de pusher debe conservar lo que se debe insertar. Cuando un proveedor de almacén envía una notificación sobre un objeto que debe indizarse, especifica el tipo de notificación **fnevIndexing** en el miembro **ulEventType** de la estructura **[NOTIFICATION.](notification.md)** El miembro **información** de la estructura **notificación** contiene una estructura **[EXTENDED_NOTIFICATION](extended_notification.md)**. El proveedor del almacén identifica el proceso en la **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** propiedad. También identifica el proceso en la estructura [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) y pasa esta información como parte del miembro **pbEventParameters** de la **estructura EXTENDED_NOTIFICATION** datos. Si el proceso se cierra o se bloquea, el controlador de protocolo MAPI podrá detectarlo inmediatamente y detener la indización del almacén del pusher. 
  
## <a name="see-also"></a>Consulte también



[Información sobre la API del almacén](about-the-store-api.md)
  
[Constantes MAPI](mapi-constants.md)

