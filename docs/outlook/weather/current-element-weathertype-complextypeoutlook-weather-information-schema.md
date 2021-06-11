---
title: elemento current (weatherType complexType) (Outlook Weather Information Schema)
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
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>elemento current (weatherType complexType) (Outlook Weather Information Schema)

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
|date  <br/> |xs:date  <br/> |necesario  <br/> |Especifica la fecha de hoy.  <br/> |Valor del tipo xs:date  <br/> |
|día  <br/> |xs:string  <br/> |opcional  <br/> |Especifica un día para la previsión.  <br/> |Valor del tipo xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura de cómo se siente el tiempo actual.  <br/> |Valor del tipo xs:integer  <br/> |
|humedad  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el valor de humedad numérica actual.  <br/> |Valor del tipo xs:integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |necesario  <br/> |Especifica desde dónde se observa la información meteorológica actual.  <br/> |Valor del tipo xs:string  <br/> |
|tiempo de observación  <br/> |xs:time  <br/> |necesario  <br/> |Especifica cuándo se observa la información meteorológica actual en.  <br/> |Valor del tipo xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |opcional  <br/> |Especifica un día en forma abreviada.  <br/> |Valor del tipo xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica un código entero para las condiciones meteorológicas actuales.  <br/> |Valor del tipo xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |necesario  <br/> |Especifica de una a dos palabras que describen las condiciones meteorológicas actuales.  <br/> |Valor del tipo xs:string  <br/> |
|temperatura  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura actual de la ubicación.  <br/> |Valor del tipo xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |necesario  <br/> |Cadena que describe las condiciones de viento actuales.  <br/> |Valor del tipo xs:string  <br/> |
|windspeed  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el valor de velocidad de viento numérico actual.  <br/> |Valor del tipo xs:integer  <br/> |
   

