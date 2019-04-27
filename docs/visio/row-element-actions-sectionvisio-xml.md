---
title: Elemento Row (sección acciones) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2019
ms.locfileid: "32356423"
---
# <a name="row-element-actions-section-visio-xml"></a>Elemento Row (sección acciones) ("XML" de Visio)

Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Masters. XML, Master #. XML, Pages. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contiene filas que describen los elementos de menú en un menú contextual o de etiqueta de acción para una forma o página.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una acción asociada con un comando personalizado en un menú contextual o de etiquetas de acción.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IX  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de base uno de la fila. Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paraGraph, Reviewer, Scratch y Tabs. Una fila sólo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único dependiente del idioma de la fila.  <br/> |Valores del tipo xsd: String.  <br/> |
|N  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag. Una fila sólo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd: String.  <br/> |
|T  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría. El atributo T solo se usa para la sección Geometry.  <br/> |Valores del tipo xsd: String.  <br/> |
   

