---
title: ForeignData_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384160"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type complexType ('XML de Visio')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base de extensión** <br/> |Ninguna  <br/> |
   
## <a name="definition"></a>Definición

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo XSD: Double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |opcional  <br/> ||Valores del tipo xsd:token.  <br/> |
|ExtentX  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo XSD: Double.  <br/> |
|ExtentY  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo XSD: Double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |necesario  <br/> ||Valores del tipo xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo XSD: Double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo XSD: Double.  <br/> |
|ShowAsIcon  <br/> |Boolean con tipo  <br/> |opcional  <br/> ||Valores del tipo Boolean con tipo.  <br/> |
   

