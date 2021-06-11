---
title: Directrices para mostrar las actividades correctamente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Los proveedores de Social Connector (OSC) pueden establecer los elementos getActivities y dynamicActivitiesLookupEx para que el OSC almacene elementos de actividad en la memoria.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422918"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Directrices para mostrar las actividades correctamente

Outlook Los proveedores de Social Connector (OSC) pueden establecer los elementos **getActivities** y **dynamicActivitiesLookupEx** para que el OSC almacene elementos de actividad en la memoria. En este tema se describen las API de extensibilidad del proveedor de OSC que llama el OSC para obtener o actualizar las actividades y los detalles del propietario de la actividad, si el proveedor de OSC admite la sincronización de fuentes de actividad desde la red social. En el tema también se enumeran algunos elementos secundarios del elemento **activityFeed** que el proveedor de OSC debe establecer para que el OSC muestre las actividades correctamente en el panel de contactos de Office o Outlook personas. 
  
- El OSC llama al método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para obtener y almacenar actividades en la carpeta De noticias del usuario que ha iniciado sesión. El proveedor de OSC debe implementar **GetActivitiesEx** para devolver una cadena _XML_ de actividades que cumpla con la definición de esquema XML del proveedor de OSC del **elemento activityFeed.** 
    
- El proveedor de OSC debe establecer el **elemento ownerID,** que es un elemento secundario del **elemento activityDetails.** **ownerID** es una cadena opaca que identifica al propietario de la actividad en la red social. 
    
- El proveedor de OSC debe establecer los elementos **nameHint** y **emailAddress** en el nodo **publisherVariable** del **elemento templateVariables.** 
    
   Tenga en cuenta que, según el esquema XML del proveedor de OSC, el **elemento nameHint** es un elemento opcional. El OSC lo usa para coincidir con el nombre para mostrar del usuario seleccionado en la tarjeta de contacto o en el panel personas. Del mismo modo, el **elemento emailAddress** es un elemento opcional en el esquema XML. El OSC lo usa para que coincida con la dirección SMTP del usuario seleccionado en la tarjeta de contacto o en el panel personas. 
    
   Si solo se especifica el elemento **ownerID,** pero no se especifica uno o ambos de **nameHint** y **emailAddress,** el OSC llama al método [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) y, a continuación, al método [ISocialPerson::GetDetails](isocialperson-getdetails.md) para obtener más información sobre la persona identificada por **el ownerID**. Cuando el OSC llama **a ISocialPerson::GetDetails**, el proveedor debe devolver **xml** de persona que especifique los elementos **fullName** **y emailAddress.** 
    
## <a name="see-also"></a>Vea también

- [XML para actividades](xml-for-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para funcionalidades](xml-for-capabilities.md)

