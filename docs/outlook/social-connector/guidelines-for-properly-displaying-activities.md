---
title: Directrices para mostrar las actividades correctamente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Los proveedores de Outlook Social Connector (OSC) pueden establecer los elementos getActivities y dynamicActivitiesLookupEx para que los elementos de actividad de almacén de OSC estén en la memoria.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286184"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Directrices para mostrar las actividades correctamente

Los proveedores de Outlook Social Connector (OSC) pueden establecer los elementos **getActivities** y **dynamicActivitiesLookupEx** para que los elementos de actividad de almacén de OSC estén en la memoria. En este tema se describen las API de extensibilidad del proveedor OSC que el OSC llama para obtener o actualizar actividades y detalles del propietario de la actividad, si el proveedor de OSC admite la sincronización de fuentes de actividades desde la red social. El tema también enumera algunos elementos secundarios del elemento **activityFeed** que el proveedor OSC debe establecer para que el OSC muestre las actividades correctamente en la tarjeta de contacto de Office o en el panel de personas de Outlook. 
  
- El OSC llama al método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) para obtener y almacenar actividades en la carpeta de fuentes de noticias del usuario que ha iniciado sesión. El proveedor OSC debe implementar **GetActivitiesEx** para devolver una __ cadena XML Activities que cumpla con la definición del esquema XML del proveedor OSC del elemento **activityFeed** . 
    
- El proveedor OSC debe establecer el elemento **ownerID** , que es un elemento secundario del elemento **activityDetails** . **ownerID** es una cadena opaca que identifica al propietario de la actividad en la red social. 
    
- El proveedor OSC debe establecer los elementos **nameHint** y **emailAddress** en el nodo **publisherVariable** del elemento **templateVariables** . 
    
   Tenga en cuenta que, según el esquema XML del proveedor de OSC, el elemento **nameHint** es un elemento opcional. El OSC lo utiliza para hacer coincidir el nombre para mostrar del usuario seleccionado en el panel de la tarjeta de contacto o de personas. De forma similar, el elemento **emailAddress** es un elemento opcional en el esquema XML. El OSC lo usa para hacer coincidir la dirección SMTP del usuario seleccionado en el panel de la tarjeta de contacto o de personas. 
    
   Si solo se especifica el elemento **ownerID** , pero no se especifica uno o ambos **nameHint** y **emailAddress** , el OSC llama al método [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) y, a continuación, a [ISocialPerson:: GetDetails](isocialperson-getdetails.md) método para obtener más información sobre la persona identificada por el **ownerID**. Cuando el OSC llama a **ISocialPerson:: GetDetails**, el proveedor debe devolver el XML de **persona** que especifica los elementos **FullName** y **emailAddress** . 
    
## <a name="see-also"></a>Vea también

- [XML para actividades](xml-for-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para funcionalidades](xml-for-capabilities.md)

