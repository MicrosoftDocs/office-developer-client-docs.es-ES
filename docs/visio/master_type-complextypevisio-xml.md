---
title: Master_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538070"
---
# <a name="master_type-complextype-visio-xml"></a>Master_Type complexType (Visio XML)

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
## <a name="definition"></a>Definición

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> ||
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-master_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|BaseID  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores del tipo xsd:string.  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores del tipo xsd:boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores del tipo xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores del tipo xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores del tipo xsd:boolean.  <br/> |
|MasterType  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores del tipo xsd:boolean.  <br/> |
|Nombre  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores del tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores del tipo xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores del tipo xsd:string.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores del tipo xsd:string.  <br/> |
   

