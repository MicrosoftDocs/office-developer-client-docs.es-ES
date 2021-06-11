---
title: elemento forecast (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Especifica las condiciones meteorológicas futuras de al menos tres días antes, incluido hoy: Hoy, Mañana, Día después de Mañana.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540983"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>elemento forecast (weatherType complexType) (Outlook Weather Information Schema)

Especifica las condiciones meteorológicas futuras de al menos tres días antes, incluido hoy: Hoy, Mañana, Día después de Mañana.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[tiempo](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones meteorológicas de una ubicación.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |necesario  <br/> |Especifica la fecha de la previsión.  <br/> |Valor del tipo xs:date  <br/> |
|día  <br/> |xs:string  <br/> |necesario  <br/> |Especifica un día para la previsión.  <br/> |Valor del tipo xs:string  <br/> |
|high  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura más alta prevista.  <br/> |Valor del tipo xs:integer  <br/> |
|low  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura más baja prevista.  <br/> |Valor del tipo xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el porcentaje de posibilidad de precipitación.  <br/> |Valor del tipo xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |necesario  <br/> |Especifica un día en forma abreviada.  <br/> |Valor del tipo xs:string  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica un código para las condiciones previstas.  <br/> |Valor del tipo xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |necesario  <br/> |Especifica de una a dos palabras que describen las condiciones previstas.  <br/> |Valor del tipo xs:string  <br/> |
   

