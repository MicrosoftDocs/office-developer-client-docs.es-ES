---
title: weatherType complexType (esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Especifica las condiciones meteorológicas de una ubicación.
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355044"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>weatherType complexType (esquema de información meteorológica de Outlook)

Especifica las condiciones meteorológicas de una ubicación.
  
## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherinfo. xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
## <a name="definition"></a>Definición

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
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
   

