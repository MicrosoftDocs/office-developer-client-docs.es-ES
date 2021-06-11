---
title: elemento weather (elemento weatherdata) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica las condiciones meteorológicas de una ubicación.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541270"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>elemento weather (elemento weatherdata) (Outlook Weather Information Schema)

Especifica las condiciones meteorológicas de una ubicación.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Define el elemento weather.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[actual](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones meteorológicas actuales.  <br/> |
|[previsión](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones meteorológicas futuras de al menos tres días antes, incluido hoy: Hoy, Mañana, Día después de Mañana.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|atribución  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el origen de la información meteorológica.  <br/> |Valor del tipo xs:string  <br/> |
|degreetype  <br/> |xs:string  <br/> |necesario  <br/> |Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |necesario  <br/> |Especifica la dirección URL de la imagen de la ubicación.  <br/> |Valor del tipo xs:string  <br/> |
|zona horaria  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el desplazamiento GMT.  <br/> |Un valor entre -11 y 12 inclusive  <br/> |
|url  <br/> |xs:string  <br/> |necesario  <br/> |Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.  <br/> |Valor del tipo xs:string  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el código asociado a la ubicación usada para distinguir varias ubicación que tienen el mismo nombre.  <br/> |Valor del tipo xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el nombre de la ubicación que aparece en el control desplegable.  <br/> |Valor del tipo xs:string  <br/> |
   

