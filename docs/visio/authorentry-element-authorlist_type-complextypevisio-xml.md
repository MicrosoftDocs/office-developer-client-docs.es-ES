---
title: Elemento AuthorEntry (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica las propiedades usadas para identificar al autor de un comentario en un dibujo.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537909"
---
# <a name="authorentry-element-authorlist_type-complextype-visio-xml"></a>Elemento AuthorEntry (AuthorList_Type complexType) (Visio XML)

Especifica las propiedades usadas para identificar al autor de un comentario en un dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Especifica los autores de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Valor único que identifica al autor.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Initials  <br/> |xsd:string  <br/> |opcional  <br/> |Las iniciales del autor.  <br/> |Valores del tipo xsd:string.  <br/> |
|Nombre  <br/> |xsd:string  <br/> |opcional  <br/> |Nombre del autor.  <br/> |Valores del tipo xsd:string.  <br/> |
|ResolutionID  <br/> |xsd:string  <br/> |opcional  <br/> |Un identificador único para el autor.  <br/> |Valores del tipo xsd:string.  <br/> |
   

