---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539866"
---
# <a name="foreigndata_type-complextype-visio-xml"></a>ForeignData_Type complexType (Visio XML)

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
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

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |opcional  <br/> ||Valores del tipo xsd:double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |opcional  <br/> ||Valores del tipo xsd:token.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |opcional  <br/> ||Valores del tipo xsd:double.  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |opcional  <br/> ||Valores del tipo xsd:double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |necesario  <br/> ||Valores del tipo xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |opcional  <br/> ||Valores del tipo xsd:double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |opcional  <br/> ||Valores del tipo xsd:double.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores del tipo xsd:boolean.  <br/> |
   

