---
title: currentType complexType (esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Define los parámetros sobre las condiciones meteorológicas actuales de una ubicación.
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338454"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (esquema de información meteorológica de Outlook)

Define los parámetros sobre las condiciones meteorológicas actuales de una ubicación.
  
## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo. xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
## <a name="definition"></a>Definición

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
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
   

