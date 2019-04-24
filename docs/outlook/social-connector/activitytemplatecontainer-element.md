---
title: Elemento activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un elemento activityTemplateContainer es una plantilla que permite dar formato a los elementos de la fuente de actividades y reutilizar XML que especifica un diseño.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281123"
---
# <a name="activitytemplatecontainer-element"></a>Elemento activityTemplateContainer

Un elemento **activityTemplateContainer** es una plantilla que permite dar formato a los elementos de la fuente de actividades y reutilizar XML que especifica un diseño. Use identificadores (**applicationID** y **templateID**) para hacer coincidir un elemento de fuente (**activityDetails**) con una plantilla (**activityTemplateContainer**). Almacene los datos de diseño como parte del elemento **activityTemplate** . Para hacer referencia a datos que se extraen del elemento de fuente de actividad individual, use variables de plantilla como marcadores de posición para obtener información como personas, vínculos y texto. 
  
En la tabla siguiente se describen los tres elementos que requiere el elemento **activityTemplateContainer** . 
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**applicationID** <br/> |Uno de los dos identificadores únicos que se usan para hacer coincidir el elemento de la fuente con su plantilla. Si tiene varias aplicaciones u otros grupos, puede usarse como organizador de plantillas de primer nivel.  <br/> |
|**templateID** <br/> |El segundo identificador único que se usa para hacer coincidir el elemento de la fuente con su plantilla. Se puede usar como un organizador de plantillas de segundo nivel.  <br/> |
|**activityTemplate** <br/> |El diseño de la plantilla (elementos**Icon**, **title**y **Data** ) y el tipo de actividad (elemento**Type** ).  <br/> |
   
En la tabla siguiente se describen los elementos secundarios de **activityTemplate**, que describen el diseño y el tipo de una plantilla.
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**icon** <br/> |Un token de vínculo, que hace referencia a la dirección URL del icono de ese elemento de fuente.  <br/> |
|**title** <br/> |La información necesaria para el elemento de fuente.  <br/> |
|**type** <br/> |El tipo de actividad, como una actualización del estado, la foto o el documento.  <br/> |
|**data** <br/> |Cualquier información adicional para el elemento de la fuente, como imágenes, texto o vínculos.  <br/> |
   
Para obtener un ejemplo de XML de fuente de actividades, consulte [ejemplo de XML de fuente de actividades](activity-feed-xml-example.md) .
  
## <a name="see-also"></a>Vea también

- [Información general sobre XML para un elemento de fuente de actividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Variables de plantilla](template-variables.md)  
- [Directrices para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)  
- [XML para actividades](xml-for-activities.md)  
- [Esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

