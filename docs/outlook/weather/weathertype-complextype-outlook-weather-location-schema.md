---
title: weatherType complexType (esquema de ubicación de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Define los parámetros acerca de las condiciones del tiempo de una ubicación.
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387716"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (esquema de ubicación de meteorología de Outlook)

Define los parámetros acerca de las condiciones del tiempo de una ubicación.
  
## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Archivo de esquema** <br/> |getweatherlocation.xsd  <br/> |
|**Base de extensión** <br/> |Ninguna  <br/> |
   
## <a name="definition"></a>Definición

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |necesario  <br/> |Especifica un código que está asociado a la ubicación para distinguir varias ubicaciones con el mismo nombre.  <br/> |Un valor del tipo xs: String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |necesario  <br/> |Especifica el nombre de la ubicación.  <br/> |Un valor del tipo xs: String  <br/> |
   

