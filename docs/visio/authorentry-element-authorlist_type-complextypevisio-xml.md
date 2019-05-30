---
title: Elemento AuthorEntry (complexType AuthorList_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica las propiedades que se usan para identificar al autor de un Comentario en un dibujo.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537909"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>Elemento AuthorEntry (complexType AuthorList_Type) (XML de Visio)

Especifica las propiedades que se usan para identificar al autor de un Comentario en un dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |comments. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Especifica los autores de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |Un valor basado en uno que identifica al autor.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Iniciales  <br/> |xsd: String  <br/> |opcional  <br/> |Las iniciales del autor.  <br/> |Valores del tipo xsd: String.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre del autor.  <br/> |Valores del tipo xsd: String.  <br/> |
|ResolutionID  <br/> |xsd: String  <br/> |opcional  <br/> |Un identificador único para el autor.  <br/> |Valores del tipo xsd: String.  <br/> |
   

