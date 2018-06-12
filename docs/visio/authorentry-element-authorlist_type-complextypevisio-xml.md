---
title: Elemento de AuthorEntry (AuthorList_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica propiedades que se usan para identificar al autor de un comentario en un dibujo.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821543"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>Elemento de AuthorEntry (AuthorList_Type complexType) ('XML de Visio')

Especifica propiedades que se usan para identificar al autor de un comentario en un dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Comments.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Especifica a los autores de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|id.  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Un valor basado en uno que identifica al autor.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Iniciales  <br/> |xsd: String  <br/> |opcional  <br/> |Las iniciales del autor.  <br/> |Valores del tipo XSD: String.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre del autor.  <br/> |Valores del tipo XSD: String.  <br/> |
|ResolutionID  <br/> |xsd: String  <br/> |opcional  <br/> |Un identificador único para el autor.  <br/> |Valores del tipo XSD: String.  <br/> |
   

