---
title: Elemento Row (sección Controls) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Contiene las celdas de un controlador de control determinado definido para una forma.
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541746"
---
# <a name="row-element-controls-section-visio-xml"></a>Elemento Row (sección Controls) (Visio XML)

Contiene las celdas de un controlador de control determinado definido para una forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contiene las celdas de un controlador de control determinado definido para una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene una propiedad para un controlador de control determinado definido para una forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que se heredaría de una forma maestra.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador único de la fila. Debe ser unqiue y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs. Una fila solo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el nombre único dependiente del idioma de la fila.  <br/> |Valores del tipo xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag. Una fila solo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría. El atributo T solo se usa para la sección Geometría.  <br/> |Valores del tipo xsd:string.  <br/> |
   

