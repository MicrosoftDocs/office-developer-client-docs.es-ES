---
title: Elemento CommentEntry (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica las propiedades usadas para identificar un comentario en un dibujo.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540115"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a>Elemento CommentEntry (CommentList_Type complexType) (Visio XML)

Especifica las propiedades usadas para identificar un comentario en un dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Especifica los comentarios de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Valor único que identifica al autor.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Valor único que identifica el comentario en una página de dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Fecha  <br/> |xsd:dateTime  <br/> |necesario  <br/> |Especifica cuándo se creó un comentario.  <br/> |Valores del tipo xsd:dateTime.  <br/> |
|Hecho  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica el estado actual del comentario.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |opcional  <br/> |Especifica cuándo se cambió por última vez un comentario.  <br/> |Valores del tipo xsd:dateTime.  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Valor que identifica la página de dibujo en la que se encuentra el comentario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Valor que identifica la forma en la que está el comentario. Si no se especifica Ningún ShapeID, el comentario hace referencia a la página de dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

