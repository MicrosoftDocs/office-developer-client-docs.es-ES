---
title: Elemento Section (Sheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Especifica una colección de propiedades relacionadas.
ms.openlocfilehash: 2862d2ccf10d235996c2a6fb26691d498bdfdbcf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539036"
---
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Elemento Section (Sheet_Type complexType) (Visio XML)

Especifica una colección de propiedades relacionadas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de un dibujo.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de una página de un dibujo.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[complexType Master_Type](master_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociada al patrón.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades asociadas a una forma.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades asociadas a un estilo, dibujo, página de dibujo o forma.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Especifica una hoja de estilos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una sola propiedad.  <br/> |
|[Fila](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Especifica una colección de **Cell_Type** elementos.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica si se ha eliminado una colección que, de lo contrario, se heredaría. Debe ser igual a 0 o 1. Un valor de 1 especifica que la colección no se usa y debe omitirse. Un valor de 0 especifica que la colección de propiedades es válida para la forma. Si el **atributo Del** no está presente, el valor es 0.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el índice basado en cero del elemento. DEBE ser único entre todos los elementos **Section_Type** con el mismo atributo **N** de la Sheet_Type **.** DEBE ser mayor que el atributo  **IX** de cualquier elemento Section_Type anterior con el mismo atributo **N** de la Sheet_Type **.**  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|N  <br/> |xsd:string  <br/> |necesario  <br/> |Especifica el nombre independiente del idioma de la colección de propiedades. Debe ser único entre todos los elementos Section_Type **del** elemento que **lo Sheet_Type, a** menos que sea igual a "Geometría". Debe ser igual a una subpartida en **secciones**.  <br/> |Valores del tipo xsd:string.  <br/> |
   
### <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Section** debe ser uno de un conjunto limitado de valores que corresponden a **celdas ShapeSheet.** Consulte la tabla siguiente para determinar los valores del atributo **N** permitidos para este **elemento Section.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Acciones  <br/> |Colección de propiedades que se usan para la evaluación de fórmulas. DEBE tener un elemento **ShapeSheet_Type** o **PageSheet_Type** elemento primario.  <br/> |[Sección de acciones](actions-section.md) <br/> |
|ActionTag  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento **ShapeSheet_Type** o **PageSheet_Type** elemento primario.  <br/> |[Sección de la etiqueta de acción](action-tag-section.md) <br/> |
|Conexiones  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento **ShapeSheet_Type** primario.  <br/> ||
|Controles  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento **ShapeSheet_Type** primario.  <br/> |[Sección de controles](controls-section.md) <br/> |
|Hyperlink  <br/> |Colección de propiedades relacionadas que especifican los hipervínculos de formas. DEBE tener un elemento **ShapeSheet_Type** primario.  <br/> |[Sección de hipervínculos](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Colección de propiedades relacionadas que especifican los datos de formas. DEBE tener un elemento **ShapeSheet_Type** primario.  <br/> |[Sección de datos de formas](shape-data-section.md) <br/> |
|Usuario  <br/> |Colección de propiedades que se usan para la evaluación de fórmulas. Debe tener un elemento **DocumentSheet_Type**, **PageSheet_Type** o **ShapeSheet_Type** elemento primario.  <br/> |[Sección de celdas definidas por el usuario](user-defined-cells-section.md) <br/> |
   
El **atributo IX** de este elemento **Section** debe ser uno de un conjunto limitado de valores que corresponden a **celdas ShapeSheet.** Consulte la tabla siguiente para determinar los valores del atributo **IX** permitidos para este **elemento Section.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Annotation  <br/> |Una colección de propiedades que contienen información sobre los comentarios insertados en una página de documento.  <br/> |[Sección de anotación](annotation-section.md) <br/> |
|Carácter  <br/> |Colección de propiedades relacionadas que especifican las propiedades de carácter del texto de una forma. DEBE tener un elemento **ShapeSheet_Type** primario o un **elemento StyleSheet_Type** primario.  <br/> |[Sección de caracteres](character-section.md) <br/> |
|Conexiones  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento **ShapeSheet_Type** primario.  <br/> |[Sección de puntos de conexión](connection-points-section.md) <br/> |
|Campo  <br/> |Colección de propiedades relacionadas que especifican los campos de texto de una forma. DEBE tener un elemento **ShapeSheet_Type** primario.  <br/> |[Sección de campos de texto](text-fields-section.md) <br/> |
|FillGradient  <br/> |Colección de propiedades que especifican el degradado de color de relleno de una forma. DEBE tener un elemento **ShapeSheet_Type** o **StyleSheet_Type** elemento primario.  <br/> |[Sección Degradado de relleno](fill-gradient-section.md) <br/> |
|Geometría  <br/> |Colección de propiedades relacionadas que especifican la visualización de geometría. DEBE tener un elemento **ShapeSheet_Type** primario. El primer **Row_Type** elemento secundario de este elemento DEBE ser de tipo MoveTo, RelMoveTo, Ellipse o InfiniteLine.  <br/> |[Sección de geometría](geometry-section.md) <br/> |
|Layers  <br/> |Colección de propiedades que muestran todas las capas definidas en una página de dibujo. DEBE ser el elemento secundario de un **PageSheet_Type** elemento.  <br/> |[Sección de capas](layers-section.md) <br/> |
|Degradado de línea  <br/> |Colección de propiedades relacionadas que especifican el degradado de color de línea de una forma. DEBE tener un elemento **ShapeSheet_Type** o **StyleSheet_Type** elemento primario.  <br/> |[Sección degradado de línea](line-gradient-section.md) <br/> |
|Párrafo  <br/> |Colección de propiedades relacionadas que especifican las propiedades de párrafo del texto de una forma. DEBE tener un elemento **ShapeSheet_Type** primario o un **elemento StyleSheet_Type** primario.  <br/> |[Sección de párrafo](paragraph-section.md) <br/> |
|Reviewer  <br/> |Colección de propiedades que se usan para la evaluación de fórmulas. DEBE tener un elemento **DocumentSheet_Type** primario.  <br/> |[Sección de revisor](reviewer-section.md) <br/> |
|Scratch  <br/> |Colección de propiedades que se usan para la evaluación de fórmulas. Debe tener un elemento **DocumentSheet_Type**, **PageSheet_Type** o **ShapeSheet_Type** elemento primario.  <br/> |[Sección de borrador](scratch-section.md) <br/> |
|Pestañas  <br/> |Colección de propiedades relacionadas que especifican las propiedades de pestañas del texto de una forma. DEBE tener un elemento **ShapeSheet_Type** primario o un **elemento StyleSheet_Type** primario.  <br/> |[Sección de tabulaciones](tabs-section.md) <br/> |
   

