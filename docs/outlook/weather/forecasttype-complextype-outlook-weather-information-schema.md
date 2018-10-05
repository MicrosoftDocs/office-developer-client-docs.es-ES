---
title: forecastType complexType (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Define los parámetros acerca de las condiciones de previsión meteorológica de una ubicación.
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390628"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (esquema de información de meteorología de Outlook)

Define los parámetros acerca de las condiciones de previsión meteorológica de una ubicación.
  
## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
|**Base de extensión** <br/> |Ninguna  <br/> |
   
## <a name="definition"></a>Definición

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
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
   

