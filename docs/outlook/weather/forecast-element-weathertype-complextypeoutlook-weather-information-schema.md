---
title: previsión de elemento (weatherType complexType) (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.'
ms.openlocfilehash: c618b753ddf8a72fce270800675982f1a7f7af5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821228"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>previsión de elemento (weatherType complexType) (esquema de información de meteorología de Outlook)

Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[meteorología](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones del tiempo de una ubicación.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: Date  <br/> |necesario  <br/> |Especifica la fecha de la previsión.  <br/> |Un valor de tipo de xs: Date  <br/> |
|día  <br/> |xs:string  <br/> |necesario  <br/> |Especifica un día para la previsión.  <br/> |Un valor del tipo xs: String  <br/> |
|alta  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura máxima prevista.  <br/> |Un valor del tipo xs: Integer  <br/> |
|baja  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura más baja prevista.  <br/> |Un valor del tipo xs: Integer  <br/> |
|precip  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la posibilidad de porcentaje de precipitación.  <br/> |Un valor del tipo xs: Integer  <br/> |
|shortday  <br/> |xs:string  <br/> |necesario  <br/> |Especifica un día de forma abreviada.  <br/> |Un valor del tipo xs: String  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica un código de las condiciones previstas.  <br/> |Un valor del tipo xs: Integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |necesario  <br/> |Especifica una o dos palabras que describen las condiciones previstas.  <br/> |Un valor del tipo xs: String  <br/> |
   

