---
title: elemento actual (complexType weatherType) (esquema de información de tiempo de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Especifica las condiciones meteorológicas actuales.
ms.openlocfilehash: ce92bdd49ee37f939748586c2d63d8a664f664d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351474"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>elemento actual (complexType weatherType) (esquema de información de tiempo de Outlook)

Especifica las condiciones meteorológicas actuales.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo. xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="current"      type="currentType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Boletín](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Especifica las condiciones meteorológicas de una ubicación.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|fecha  <br/> |XS: Date  <br/> |necesario  <br/> |Especifica la fecha de hoy.  <br/> |Un valor de tipo XS: Date  <br/> |
|cotidiano  <br/> |XS: String  <br/> |opcional  <br/> |Especifica un día para la previsión.  <br/> |Un valor de tipo XS: String  <br/> |
|feelslike  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica la temperatura del tiempo actual que parece.  <br/> |Un valor del tipo XS: Integer  <br/> |
|humedad  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica el valor de humedad numérica actual.  <br/> |Un valor del tipo XS: Integer  <br/> |
|observationpoint  <br/> |XS: String  <br/> |necesario  <br/> |Especifica dónde se observa la información meteorológica actual.  <br/> |Un valor de tipo XS: String  <br/> |
|observationtime  <br/> |XS: Time  <br/> |necesario  <br/> |Especifica cuándo se observa la información meteorológica actual en.  <br/> |Un valor del tipo XS: Time  <br/> |
|shortday  <br/> |XS: String  <br/> |opcional  <br/> |Especifica un día en forma abreviada.  <br/> |Un valor de tipo XS: String  <br/> |
|skycode  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica un código de número entero para las condiciones meteorológicas actuales.  <br/> |Un valor del tipo XS: Integer  <br/> |
|skytext  <br/> |XS: String  <br/> |necesario  <br/> |Especifica de una a dos palabras que describen las condiciones meteorológicas actuales.  <br/> |Un valor de tipo XS: String  <br/> |
|medidor  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica la temperatura actual de la ubicación.  <br/> |Un valor del tipo XS: Integer  <br/> |
|winddisplay  <br/> |XS: String  <br/> |necesario  <br/> |Una cadena que describe las condiciones de viento actuales.  <br/> |Un valor de tipo XS: String  <br/> |
|windspeed  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica el valor numérico de velocidad de viento actual.  <br/> |Un valor del tipo XS: Integer  <br/> |
   

