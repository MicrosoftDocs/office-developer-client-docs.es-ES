---
title: HeaderFooterFont_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822262"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>HeaderFooterFont_Type complexType ('XML de Visio')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base de extensión** <br/> |Ninguna  <br/> |
   
## <a name="definition"></a>Definición

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Juego de caracteres  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|Escape  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo XSD: int.  <br/> |
|Nombre de fuente  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
|Alto  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo XSD: int.  <br/> |
|Cursiva  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|Orientation  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo XSD: int.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|Calidad  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|Tachado  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|Subrayado  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedByte.  <br/> |
|Grosor  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo XSD: int.  <br/> |
|Ancho  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo XSD: int.  <br/> |
   

