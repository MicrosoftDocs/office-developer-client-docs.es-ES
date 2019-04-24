---
title: DataColumn_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344705"
---
# <a name="datacolumntype-complextype-visio-xml"></a>DataColumn_Type complexType (' Visio XML ')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
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
|Calendar  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo xsd: String.  <br/> |
|Moneda  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedShort.  <br/> |
|DataType  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedShort.  <br/> |
|Degree  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|Hyperlink  <br/> |xsd: Boolean  <br/> |opcional  <br/> ||Valores del tipo xsd: Boolean.  <br/> |
|Label  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo xsd: String.  <br/> |
|Idioma  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|Asignación  <br/> |xsd: Boolean  <br/> |opcional  <br/> ||Valores del tipo xsd: Boolean.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo xsd: String.  <br/> |
|OrigLabel  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
|UnitType  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
   

