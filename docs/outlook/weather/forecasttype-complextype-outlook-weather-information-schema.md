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
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361148"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (esquema de información meteorológica de Outlook)

Define los parámetros sobre las condiciones meteorológicas de previsión de una ubicación.
  
## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
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
|fecha  <br/> |XS: Date  <br/> |necesario  <br/> |Especifica la fecha de la previsión.  <br/> |Un valor de tipo XS: Date  <br/> |
|cotidiano  <br/> |XS: String  <br/> |necesario  <br/> |Especifica un día para la previsión.  <br/> |Un valor de tipo XS: String  <br/> |
|mayor  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica la temperatura más alta prevista.  <br/> |Un valor del tipo XS: Integer  <br/> |
|baja  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica la temperatura más baja prevista.  <br/> |Un valor del tipo XS: Integer  <br/> |
|Precip  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica el porcentaje de probabilidad de precipitación.  <br/> |Un valor del tipo XS: Integer  <br/> |
|shortday  <br/> |XS: String  <br/> |necesario  <br/> |Especifica un día en forma abreviada.  <br/> |Un valor de tipo XS: String  <br/> |
|skycodeday  <br/> |XS: Integer  <br/> |necesario  <br/> |Especifica un código para las condiciones de previsión.  <br/> |Un valor del tipo XS: Integer  <br/> |
|skytextday  <br/> |XS: String  <br/> |necesario  <br/> |Especifica de una a dos palabras que describen las condiciones de previsión.  <br/> |Un valor de tipo XS: String  <br/> |
   

