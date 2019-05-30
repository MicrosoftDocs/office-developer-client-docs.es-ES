---
title: forecastType complexType (esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Define los parámetros sobre las condiciones meteorológicas de previsión de una ubicación.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540955"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (esquema de información meteorológica de Outlook)

Define los parámetros sobre las condiciones meteorológicas de previsión de una ubicación.
  
## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo. xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
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

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |XS: Date  <br/> |necesario  <br/> |Especifica la fecha de la previsión.  <br/> |Un valor de tipo XS: Date  <br/> |
|cotidiano  <br/> |XS: String  <br/> |necesario  <br/> |Especifica un día para la previsión.  <br/> |Un valor de tipo XS: String  <br/> |
|mayor  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica la temperatura más alta prevista.  <br/> |Un valor del tipo XS: Integer  <br/> |
|baja  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica la temperatura más baja prevista.  <br/> |Un valor del tipo XS: Integer  <br/> |
|precip  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica el porcentaje de probabilidad de precipitación.  <br/> |Un valor del tipo XS: Integer  <br/> |
|shortday  <br/> |XS: String  <br/> |necesario  <br/> |Especifica un día en forma abreviada.  <br/> |Un valor de tipo XS: String  <br/> |
|skycodeday  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica un código para las condiciones de previsión.  <br/> |Un valor del tipo XS: Integer  <br/> |
|skytextday  <br/> |XS: String  <br/> |necesario  <br/> |Especifica de una a dos palabras que describen las condiciones de previsión.  <br/> |Un valor de tipo XS: String  <br/> |
   

