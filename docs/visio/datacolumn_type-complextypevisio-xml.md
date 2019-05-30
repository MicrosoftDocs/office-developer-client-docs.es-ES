---
title: ComplexType DataColumn_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541214"
---
# <a name="datacolumntype-complextype-visio-xml"></a>ComplexType DataColumn_Type (XML de Visio)

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
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

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Calendario  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo xsd: String.  <br/> |
|Moneda  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedShort.  <br/> |
|DataType  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedShort.  <br/> |
|Degree  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|Hipervínculo  <br/> |xsd: Boolean  <br/> |opcional  <br/> ||Valores del tipo xsd: Boolean.  <br/> |
|Label  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo xsd: String.  <br/> |
|Idioma  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|Asignación  <br/> |xsd: Boolean  <br/> |opcional  <br/> ||Valores del tipo xsd: Boolean.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo xsd: String.  <br/> |
|OrigLabel  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
|UnitType  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
   

