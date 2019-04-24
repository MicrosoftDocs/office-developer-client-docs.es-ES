---
title: CommentEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334947"
---
# <a name="commententrytype-complextype-visio-xml"></a>CommentEntry_Type complexType (' Visio XML ')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base de extensión** <br/> |xsd: String  <br/> |
   
## <a name="definition"></a>Definición

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|AutoCommentType  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|CommentID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|Fecha  <br/> |xsd: dateTime  <br/> |necesario  <br/> ||Valores del tipo xsd: dateTime.  <br/> |
|Done  <br/> |xsd: Boolean  <br/> |opcional  <br/> ||Valores del tipo xsd: Boolean.  <br/> |
|EditDate  <br/> |xsd: dateTime  <br/> |opcional  <br/> ||Valores del tipo xsd: dateTime.  <br/> |
|PageID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|ShapeID  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
   

