---
title: Elemento activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un elemento activityTemplateContainer es una plantilla que le permite dar formato a los elementos de la fuente de actividades y volver a usar XML que especifica un diseño.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821090"
---
# <a name="activitytemplatecontainer-element"></a>Elemento activityTemplateContainer

Un elemento **activityTemplateContainer** es una plantilla que le permite dar formato a los elementos de la fuente de actividades y volver a usar XML que especifica un diseño. Utilice los identificadores (**applicationID** y **templateID**) para que coincida con un elemento de la fuente (**activityDetails**) a una plantilla (**activityTemplateContainer**). Almacenar los datos de diseño como parte del elemento **activityTemplate** . Para hacer referencia a datos que se extraen desde el elemento de fuente de actividades individuales, use las variables de plantilla como marcadores de posición para información como personas, vínculos y texto. 
  
En la siguiente tabla se describe los tres elementos que requiere el elemento **activityTemplateContainer** . 
  
|**Element**|**Descripción**|
|:-----|:-----|
|**applicationID** <br/> |Uno de los dos identificadores únicos que se usan para que coincida con el elemento de la fuente con su plantilla. Si tiene varias aplicaciones u otras agrupaciones, esto se puede usar como el organizador de una plantilla de primer nivel.  <br/> |
|**identificador de plantilla** <br/> |El segundo identificador único que se utiliza para que coincida con el elemento de la fuente con su plantilla. Esto se puede usar como el organizador de una plantilla de segundo nivel.  <br/> |
|**activityTemplate** <br/> |El diseño de la plantilla (elementos de**icono**, **título**y **datos** ) y el tipo de actividad (**tipo de** elemento).  <br/> |
   
En la siguiente tabla se describe los elementos secundarios de **activityTemplate**, que se describe el diseño y el tipo de una plantilla.
  
|**Element**|**Descripción**|
|:-----|:-----|
|**icon** <br/> |Un token de vínculo, que hace referencia a la dirección URL del icono para ese elemento de la fuente.  <br/> |
|**title** <br/> |La información necesaria para el elemento de la fuente.  <br/> |
|**tipo** <br/> |El tipo de actividad, como una actualización de estado, la foto o el documento.  <br/> |
|**data** <br/> |Información adicional para el elemento de la fuente, como imágenes, texto o vínculos.  <br/> |
   
Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Ver también

- [Elemento de la fuente de información general de XML de una actividad](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Variables de plantilla](template-variables.md)  
- [Instrucciones para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)  
- [XML de actividades](xml-for-activities.md)  
- [Esquema XML de proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

