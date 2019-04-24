---
title: ForeignData_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346014"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type complexType (' Visio XML ')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
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

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[REL](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo xsd: Double.  <br/> |
|CompressionType  <br/> |xsd: token  <br/> |opcional  <br/> ||Valores del tipo xsd: token.  <br/> |
|ExtentX  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo xsd: Double.  <br/> |
|Extensión  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo xsd: Double.  <br/> |
|ForeignType  <br/> |xsd: token  <br/> |necesario  <br/> ||Valores del tipo xsd: token.  <br/> |
|Absolute  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo xsd: Double.  <br/> |
|ObjectType  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores del tipo xsd: Double.  <br/> |
|ShowAsIcon  <br/> |xsd: Boolean  <br/> |opcional  <br/> ||Valores del tipo xsd: Boolean.  <br/> |
   

