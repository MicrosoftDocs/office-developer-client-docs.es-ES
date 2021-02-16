---
title: Elemento activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: El elemento activityDetails almacena los datos sin procesar de un único elemento de fuente de actividad. Cada elemento de fuente de actividades debe tener su propio elemento activityDetails. Se hace referencia a los datos del elemento activityDetails en las plantillas de actividad mediante el uso de elementos de nombre.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434875"
---
# <a name="activitydetails-element"></a>Elemento activityDetails

El **elemento activityDetails** almacena los datos sin procesar de un único elemento de fuente de actividad. Cada elemento de fuente de actividades debe tener su **propio elemento activityDetails.** Se hace referencia a los datos del **elemento activityDetails** en las plantillas de actividad mediante el uso de **elementos de** nombre. Todos los datos del **elemento activityDetails** deben tener un **elemento name.** 
  
En la tabla siguiente se describen los seis elementos que requiere el elemento **activityDetails.** 
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**ownerID** <br/> |Identificador del usuario de la red social que generó este elemento de fuente de actividades.  <br/> |
|**objectID** <br/> |Una cadena única para el elemento de fuente de actividades para detectar elementos de fuente duplicados.  <br/> |
|**applicationId** <br/> |Uno de los dos identificadores únicos que se usan para hacer coincidir el elemento de fuente de actividades con su plantilla. Si tiene varias aplicaciones u otras agrupaciones, puede usarse como organizador de plantillas de primer nivel.  <br/> |
|**templateId** <br/> |El segundo identificador único que se usa para hacer coincidir el elemento de fuente de actividades con su plantilla. Puede usarse como organizador de plantillas de segundo nivel.  <br/> |
|**publishDate** <br/> |Fecha y hora en que se publicó el elemento de fuente de actividades.  <br/> |
|**templateVariables** <br/> |Los datos que se usarán en los tokens para la plantilla de elemento de fuente de actividades.  <br/> |
   
Para obtener un ejemplo de XML de fuente de actividades, vea [el ejemplo XML de fuente de actividades](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Consulte también

- [Información general sobre XML para un elemento de fuente de actividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Variables de plantilla](template-variables.md) 
- [Directrices para mostrar actividades correctamente](guidelines-for-properly-displaying-activities.md)  
- [XML para actividades](xml-for-activities.md)  
- [Esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

