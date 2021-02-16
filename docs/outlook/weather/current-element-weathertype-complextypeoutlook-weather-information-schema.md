---
title: elemento current (complexType weatherType) (Esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Especifica las condiciones meteorológicas actuales.
ms.openlocfilehash: 1303212da1336112599ae5328498cca0d4ab5f89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541011"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>elemento current (complexType weatherType) (Esquema de información meteorológica de Outlook)

Especifica las condiciones meteorológicas actuales.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="current"      type="currentType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[el tiempo](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones meteorológicas de una ubicación.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |necesario  <br/> |Especifica la fecha de hoy.  <br/> |Un valor del tipo xs:date  <br/> |
|day  <br/> |xs:string  <br/> |opcional  <br/> |Especifica un día para la previsión.  <br/> |Un valor del tipo xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura de la sensación meteorológica actual.  <br/> |Un valor del tipo xs:integer  <br/> |
|desa.  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el valor numérico actual de la humedad.  <br/> |Un valor del tipo xs:integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |necesario  <br/> |Especifica de dónde se observa la información meteorológica actual.  <br/> |Un valor del tipo xs:string  <br/> |
|observationtime  <br/> |xs:time  <br/> |necesario  <br/> |Especifica cuándo se observa la información meteorológica actual.  <br/> |Un valor del tipo xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |opcional  <br/> |Especifica un día en forma abreviada.  <br/> |Un valor del tipo xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica un código entero para las condiciones meteorológicas actuales.  <br/> |Un valor del tipo xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |necesario  <br/> |Especifica de una a dos palabras que describen las condiciones meteorológicas actuales.  <br/> |Un valor del tipo xs:string  <br/> |
|temperature  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura actual de la ubicación.  <br/> |Un valor del tipo xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |necesario  <br/> |Cadena que describe las condiciones actuales del aire.  <br/> |Un valor del tipo xs:string  <br/> |
|windspeed  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el valor de velocidad de energía numérico actual.  <br/> |Un valor del tipo xs:integer  <br/> |
   

