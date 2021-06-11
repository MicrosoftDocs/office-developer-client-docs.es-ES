---
title: elemento weather (elemento weatherdata) (Outlook esquema de ubicación meteorológica)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica la ubicación en la que se debe informar del tiempo.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539015"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>elemento weather (elemento weatherdata) (Outlook esquema de ubicación meteorológica)

Especifica la ubicación en la que se debe informar del tiempo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Define el elemento weather.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |necesario  <br/> |Especifica un código asociado a la ubicación para distinguir varias ubicaciones con el mismo nombre.  <br/> |Valor del tipo xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el nombre de la ubicación.  <br/> |Valor del tipo xs:string  <br/> |
   

