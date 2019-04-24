---
title: elemento Weather (elemento datos) (esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica las condiciones meteorológicas de una ubicación.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355149"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>elemento Weather (elemento datos) (esquema de información meteorológica de Outlook)

Especifica las condiciones meteorológicas de una ubicación.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo. xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[datos](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Define el elemento Weather.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[recientes](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones meteorológicas actuales.  <br/> |
|[ID](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones meteorológicas futuras de al menos tres días de anticipación, como hoy: hoy, mañana, día después de mañana.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|atribución  <br/> |XS: String  <br/> |necesario  <br/> |Especifica el origen de la información meteorológica.  <br/> |Un valor de tipo XS: String  <br/> |
|degreetype  <br/> |XS: String  <br/> |necesario  <br/> |Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |XS: String  <br/> |necesario  <br/> |Especifica la dirección URL de la imagen para la ubicación.  <br/> |Un valor de tipo XS: String  <br/> |
|TimeZone  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica el desplazamiento GMT.  <br/> |Un valor comprendido entre-11 y 12 inclusive  <br/> |
|url  <br/> |XS: String  <br/> |necesario  <br/> |Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.  <br/> |Un valor de tipo XS: String  <br/> |
|weatherlocationcode  <br/> |XS: String  <br/> |necesario  <br/> |Especifica el código que está asociado con la ubicación que se usa para distinguir varias ubicaciones que tienen el mismo nombre.  <br/> |Un valor de tipo XS: String  <br/> |
|weatherlocationname  <br/> |XS: String  <br/> |necesario  <br/> |Especifica el nombre de la ubicación que aparece en el control desplegable.  <br/> |Un valor de tipo XS: String  <br/> |
   

