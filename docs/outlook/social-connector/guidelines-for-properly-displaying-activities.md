---
title: Directrices para mostrar las actividades correctamente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Proveedores de Outlook Social Connector (OSC) pueden establecer los elementos getActivities y dynamicActivitiesLookupEx para tener el OSC almacenar elementos de actividad en la memoria.
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821085"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Directrices para mostrar las actividades correctamente

Proveedores de Outlook Social Connector (OSC) pueden establecer la **getActivities** y elementos de **dynamicActivitiesLookupEx** tener el OSC almacenan elementos de actividad en la memoria. En este tema se describe la extensibilidad del proveedor OSC fuentes de las API que llama el OSC para obtener o actualizar las actividades y detalles de propietario de la actividad, si el proveedor de OSC admite la sincronización de actividad de la red social. El tema también enumera algunos elementos secundarios del elemento **activityFeed** que el proveedor OSC debe establecer para que el OSC para mostrar las actividades correctamente en la tarjeta de contacto de Office o el panel de personas de Outlook. 
  
- El OSC llama al método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para obtener y almacenar las actividades en la carpeta de suministro de noticias para el usuario que ha iniciado la sesión. El proveedor OSC debe implementar **GetActivitiesEx** para devolver una cadena XML de _las actividades_ que cumple con el proveedor de OSC definición del esquema XML del elemento **activityFeed** . 
    
- El proveedor de OSC debe establecer el elemento **ownerID** , que es un elemento secundario del elemento **activityDetails** . **ownerID** es una cadena opaca que identifica al propietario de la actividad en la red social. 
    
- El proveedor de OSC debe establecer los elementos **nameHint** y **emailAddress** en el nodo **publisherVariable** del elemento **templateVariables** . 
    
   Tenga en cuenta que, según el esquema XML del proveedor OSC, el elemento **nameHint** es un elemento opcional. El OSC lo usa para que coincida con el nombre para mostrar del usuario seleccionado en la tarjeta de contacto o el panel de personas. De forma similar, el elemento **emailAddress** es un elemento opcional en el esquema XML. El OSC lo usa para que coincida con la dirección SMTP del usuario seleccionado en la tarjeta de contacto o el panel de personas. 
    
   Si sólo se especifica el elemento **ownerID** , pero no se especificaron uno o ambos de **nameHint** y **emailAddress** , el OSC llama al método de [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) y, a continuación, en la [ISocialPerson::GetDetails](isocialperson-getdetails.md) método para obtener más información acerca de la persona identificada por el **ownerID**. Cuando el OSC llama a **ISocialPerson::GetDetails**, el proveedor debe devolver **persona** XML que especifica los elementos **fullName** y **emailAddress** . 
    
## <a name="see-also"></a>Vea también

- [XML de actividades](xml-for-activities.md)  
- [XML de amigos](xml-for-friends.md)  
- [XML de capacidades](xml-for-capabilities.md)

