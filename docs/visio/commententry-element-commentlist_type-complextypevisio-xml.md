---
title: Elemento de CommentEntry (CommentList_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica las propiedades que se usa para identificar un comentario en un dibujo.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397047"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>Elemento de CommentEntry (CommentList_Type complexType) ('XML de Visio')

Especifica las propiedades que se usa para identificar un comentario en un dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Comments.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Especifica los comentarios de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Un valor basado en uno que identifica al autor.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Un valor único que identifica el comentario en una página de dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Fecha  <br/> |xsd: DateTime  <br/> |necesario  <br/> |Especifica cuándo se creó un comentario.  <br/> |Valores del tipo XSD: DateTime.  <br/> |
|Terminado  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica el estado actual del comentario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|EditDate  <br/> |xsd: DateTime  <br/> |opcional  <br/> |Especifica cuándo se modificó por última vez un comentario.  <br/> |Valores del tipo XSD: DateTime.  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Un valor que identifica la página de dibujo el comentario está en.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Un valor que identifica la forma el comentario está en. Si no se especifica ningún ShapeID, el comentario hace referencia a la página de dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

