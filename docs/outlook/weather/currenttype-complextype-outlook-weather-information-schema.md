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
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540990"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (esquema de información meteorológica de Outlook)

Define los parámetros sobre las condiciones meteorológicas actuales de una ubicación.
  
## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
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

Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
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
   

