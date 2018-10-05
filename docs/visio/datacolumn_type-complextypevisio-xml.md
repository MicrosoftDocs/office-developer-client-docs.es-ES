---
title: DataColumn_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388661"
---
# <a name="datacolumntype-complextype-visio-xml"></a>DataColumn_Type complexType ('XML de Visio')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base de extensión** <br/> |Ninguna  <br/> |
   
## <a name="definition"></a>Definición

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
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
|Calendario  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo XSD: String.  <br/> |
|Moneda  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|OrdenVisualización  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|Hipervínculo  <br/> |Boolean con tipo  <br/> |opcional  <br/> ||Valores del tipo Boolean con tipo.  <br/> |
|Etiqueta  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo XSD: String.  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|Asignadas  <br/> |Boolean con tipo  <br/> |opcional  <br/> ||Valores del tipo Boolean con tipo.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo XSD: String.  <br/> |
|OrigLabel  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
|UnitType  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
   

