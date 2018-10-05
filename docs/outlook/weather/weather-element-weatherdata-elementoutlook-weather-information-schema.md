---
title: meteorología elemento (weatherdata) (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica las condiciones del tiempo de una ubicación.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390663"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>meteorología elemento (weatherdata) (esquema de información de meteorología de Outlook)

Especifica las condiciones del tiempo de una ubicación.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Define el elemento de meteorología.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[actual](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones del tiempo actual.  <br/> |
|[previsión](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|atribución  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el origen de la información meteorológica.  <br/> |Un valor del tipo xs: String  <br/> |
|degreetype  <br/> |xs:string  <br/> |necesario  <br/> |Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |necesario  <br/> |Especifica la dirección URL de la imagen de la ubicación.  <br/> |Un valor del tipo xs: String  <br/> |
|zona horaria  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el desplazamiento de GMT.  <br/> |Un valor comprendido entre -11 y 12 inclusive  <br/> |
|url  <br/> |xs:string  <br/> |necesario  <br/> |Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.  <br/> |Un valor del tipo xs: String  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el código que está asociado con la ubicación que se usa para distinguir múltiples ubicación que tienen el mismo nombre.  <br/> |Un valor del tipo xs: String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el nombre de la ubicación que aparece en el control de lista desplegable.  <br/> |Un valor del tipo xs: String  <br/> |
   

