---
title: elemento actual (weatherType complexType) (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Especifica las condiciones del tiempo actual.
ms.openlocfilehash: 12265c463f0f1bba15c9bf1723cbbea6c505dba9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821221"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>elemento actual (weatherType complexType) (esquema de información de meteorología de Outlook)

Especifica las condiciones del tiempo actual.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="current"      type="currentType">
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
|date  <br/> |xs: Date  <br/> |necesario  <br/> |Especifica la fecha de hoy.  <br/> |Un valor de tipo de xs: Date  <br/> |
|día  <br/> |xs:string  <br/> |opcional  <br/> |Especifica un día para la previsión.  <br/> |Un valor del tipo xs: String  <br/> |
|feelslike  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura de cómo se siente la meteorología actual como.  <br/> |Un valor del tipo xs: Integer  <br/> |
|humedad  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el valor numérico humedad actual.  <br/> |Un valor del tipo xs: Integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |necesario  <br/> |Especifica dónde se observa la información meteorológica actual desde.  <br/> |Un valor del tipo xs: String  <br/> |
|observationtime  <br/> |xs: Time  <br/> |necesario  <br/> |Especifica cuándo se observa la información meteorológica actual en.  <br/> |Un valor del tipo de xs: Time  <br/> |
|shortday  <br/> |xs:string  <br/> |opcional  <br/> |Especifica un día de forma abreviada.  <br/> |Un valor del tipo xs: String  <br/> |
|skycode  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica un código de número entero para las condiciones del tiempo actual.  <br/> |Un valor del tipo xs: Integer  <br/> |
|skytext  <br/> |xs:string  <br/> |necesario  <br/> |Especifica las palabras de uno o dos que describa las condiciones de tiempo actual.  <br/> |Un valor del tipo xs: String  <br/> |
|temperatura  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica la temperatura de la ubicación actual.  <br/> |Un valor del tipo xs: Integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |necesario  <br/> |Una cadena que describe las condiciones de aire actual.  <br/> |Un valor del tipo xs: String  <br/> |
|velocidad del viento  <br/> |xs:integer  <br/> |necesario  <br/> |Especifica el valor actual de la velocidad de aire numéricos.  <br/> |Un valor del tipo xs: Integer  <br/> |
   

