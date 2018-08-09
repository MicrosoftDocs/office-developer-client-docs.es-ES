---
title: Elemento activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: El elemento activityDetails almacena los datos sin procesar para un elemento de fuente de actividades único. Cada elemento de fuente de actividades deben tener su propio elemento activityDetails. Datos en el elemento activityDetails se hace referencia en las plantillas de actividad mediante el uso de elementos de nombre.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821087"
---
# <a name="activitydetails-element"></a>Elemento activityDetails

El elemento **activityDetails** almacena los datos sin procesar para un elemento de fuente de actividades único. Cada elemento de fuente de actividades deben tener su propio elemento **activityDetails** . Datos en el elemento **activityDetails** se hace referencia en las plantillas de actividad mediante el uso de elementos de **nombre** . Cada parte de los datos en el elemento **activityDetails** debe tener un elemento de **nombre** . 
  
En la siguiente tabla se describe los seis elementos que requiere el elemento **activityDetails** . 
  
|**Element**|**Descripción**|
|:-----|:-----|
|**ownerID** <br/> |El identificador del usuario en la red social que generó esta actividad de fuente de elemento.  <br/> |
|**objectID** <br/> |Una cadena única para la actividad de fuente elemento para detectar los elementos de fuente duplicado.  <br/> |
|**applicationId** <br/> |Uno de los dos identificadores únicos que se usan para que coincida con la actividad de fuente elemento con su plantilla. Si tiene varias aplicaciones u otras agrupaciones, esto se puede usar como el organizador de una plantilla de primer nivel.  <br/> |
|**templateId** <br/> |El segundo identificador único que se utiliza para que coincida con la actividad de fuente elemento con su plantilla. Esto se puede usar como el organizador de una plantilla de segundo nivel.  <br/> |
|**fecha de publicación** <br/> |La fecha y hora en que la actividad fuente elemento se publicó.  <br/> |
|**templateVariables** <br/> |Los datos que se usará en los tokens para la plantilla de elemento de la fuente de actividad.  <br/> |
   
Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Vea también

- [Elemento de la fuente de información general de XML de una actividad](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Variables de plantilla](template-variables.md) 
- [Instrucciones para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)  
- [XML de actividades](xml-for-activities.md)  
- [Esquema XML de proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

