---
title: Elemento AuthorList (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Especifica los autores de los comentarios de un dibujo.
ms.openlocfilehash: c6e94c985d2728ba704a9159ec9bf3c4a2a72e95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537860"
---
# <a name="authorlist-element-comments_type-complextype-visio-xml"></a>Elemento AuthorList (Comments_Type complexType) (Visio XML)

Especifica los autores de los comentarios de un dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Comments](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |Especifica los comentarios de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AuthorEntry](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |Especifica las propiedades que identifican al autor de un comentario en un dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

