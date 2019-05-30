---
title: ComplexType HeaderFooterFont_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541074"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>ComplexType HeaderFooterFont_Type (XML de Visio)

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
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

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|Escape  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo xsd: int.  <br/> |
|FaceName  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
|Height  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo xsd: int.  <br/> |
|Italic  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|Orientation  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo xsd: int.  <br/> |
|Deprecision  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|Quality  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|Tacha  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|Underline  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedByte.  <br/> |
|Peso  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo xsd: int.  <br/> |
|Width  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo xsd: int.  <br/> |
   

