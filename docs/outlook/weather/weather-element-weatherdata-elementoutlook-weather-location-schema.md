---
title: elemento Weather (elemento datos) (esquema de ubicación de tiempo de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica la ubicación en la que se va a notificar el tiempo.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355212"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>elemento Weather (elemento datos) (esquema de ubicación de tiempo de Outlook)

Especifica la ubicación en la que se va a notificar el tiempo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherlocation. xsd  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[datos](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Define el elemento Weather.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |XS: String  <br/> |necesario  <br/> |Especifica un código que está asociado con la ubicación para distinguir varias ubicaciones con el mismo nombre.  <br/> |Un valor de tipo XS: String  <br/> |
|weatherlocationname  <br/> |XS: String  <br/> |necesario  <br/> |Especifica el nombre de la ubicación.  <br/> |Un valor de tipo XS: String  <br/> |
   

