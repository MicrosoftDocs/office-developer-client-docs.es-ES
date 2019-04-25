---
title: Elemento Section (Sheet_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Especifica una colección de propiedades relacionadas.
ms.openlocfilehash: e20d076d4e1958cce29554d728b64385c2f8adef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2019
ms.locfileid: "32326085"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Elemento Section (Sheet_Type complexType) ("XML" de Visio)

Especifica una colección de propiedades relacionadas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML, Masters. XML, Master #. XML, Pages. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de un dibujo.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de una página en un dibujo.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[complexType Master_Type](master_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociada al patrón.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades asociadas con una forma.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades asociadas a un estilo, dibujo, página de dibujo o forma.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Especifica una hoja de estilos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad única.  <br/> |
|[Fila](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Especifica una colección de elementos **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si se ha eliminado una colección que, de otro modo, se heredaría. DEBE ser igual a 0 o 1. Un valor de 1 especifica que la colección no está en uso y se debe omitir. Un valor de 0 especifica que la colección de propiedades es válida para la forma. Si el atributo **del** no está presente, el valor es 0.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IX  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el índice de base cero del elemento. DEBE ser único entre todos los elementos **Section_Type** con el mismo **N** atributo de la **Sheet_Type**contenedora. DEBE ser mayor que el atributo **IX** de todos los elementos **Section_Type** anteriores con el mismo atributo **N** del **Sheet_Type**contenedor.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el nombre independiente del lenguaje de la colección de propiedades. DEBE ser único entre todos los elementos **Section_Type** del elemento **Sheet_Type** contenedor, a menos que sea igual a "Geometry". DEBE ser igual a un subtítulo en las **secciones**.  <br/> |Valores del tipo xsd: String.  <br/> |
   
### <a name="remarks"></a>Comentarios

El atributo **N** de este elemento de **sección** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de **ShapeSheet** . Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento **section** . 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Acciones  <br/> |Una colección de propiedades que se usan para la evaluación de fórmulas. DEBE tener un elemento primario **ShapeSheet_Type** o **PageSheet_Type** .  <br/> |[Sección de acciones](actions-section.md) <br/> |
|ActionTag  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento primario **ShapeSheet_Type** o **PageSheet_Type** .  <br/> |[Sección de la etiqueta de acción](action-tag-section.md) <br/> |
|Connections  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento primario **ShapeSheet_Type** .  <br/> ||
|Controles  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento primario **ShapeSheet_Type** .  <br/> |[Sección de controles](controls-section.md) <br/> |
|Hipervínculo  <br/> |Colección de propiedades relacionadas que especifican los hipervínculos de formas. DEBE tener un elemento primario **ShapeSheet_Type** .  <br/> |[Sección de hipervínculos](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Colección de propiedades relacionadas que especifican los datos de formas. DEBE tener un elemento primario **ShapeSheet_Type** .  <br/> |[Sección de datos de formas](shape-data-section.md) <br/> |
|User  <br/> |Una colección de propiedades que se usan para la evaluación de fórmulas. DEBE tener un elemento primario **DocumentSheet_Type**, **PageSheet_Type**o **ShapeSheet_Type** .  <br/> |[Sección de celdas definidas por el usuario](user-defined-cells-section.md) <br/> |
   
El atributo **IX** de este elemento **section** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de **ShapeSheet** . Consulte la tabla siguiente para determinar los valores del atributo **IX** que se permiten para este elemento **section** . 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Anotación  <br/> |Una colección de propiedades que contienen información sobre los comentarios insertados en una página de documento.  <br/> |[Sección de anotación](annotation-section.md) <br/> |
|Carácter  <br/> |Colección de propiedades relacionadas que especifican las propiedades de carácter del texto de una forma. DEBE tener un elemento primario **ShapeSheet_Type** o un elemento primario **StyleSheet_Type** .  <br/> |[Sección de caracteres](character-section.md) <br/> |
|Connections  <br/> |Una colección de propiedades que se usan solo para la evaluación de fórmulas. DEBE tener un elemento primario **ShapeSheet_Type** .  <br/> |[Sección de puntos de conexión](connection-points-section.md) <br/> |
|Field  <br/> |Colección de propiedades relacionadas que especifican los campos de texto de una forma. DEBE tener un elemento primario **ShapeSheet_Type** .  <br/> |[Sección de campos de texto](text-fields-section.md) <br/> |
|FillGradient  <br/> |Una colección de propiedades que especifican el degradado de color de relleno de una forma. DEBE tener un elemento primario **ShapeSheet_Type** o **StyleSheet_Type** .  <br/> |[Sección degradado de relleno](fill-gradient-section.md) <br/> |
|Construcción  <br/> |Colección de propiedades relacionadas que especifican la visualización de la geometría. DEBE tener un elemento primario **ShapeSheet_Type** . El primer elemento secundario **Row_Type** de este elemento debe ser de tipo moveTo, RelMoveTo, Ellipse o InfiniteLine.  <br/> |[Sección de geometría](geometry-section.md) <br/> |
|Layers  <br/> |Una colección de propiedades que muestra todas las capas definidas en una página de dibujo. DEBE ser el elemento secundario de un elemento **PageSheet_Type** .  <br/> |[Sección de capas](layers-section.md) <br/> |
|Degradado de línea  <br/> |Colección de propiedades relacionadas que especifican el degradado de color de línea de una forma. DEBE tener un elemento primario **ShapeSheet_Type** o **StyleSheet_Type** .  <br/> |[Sección degradado de línea](line-gradient-section.md) <br/> |
|Paragraph  <br/> |Colección de propiedades relacionadas que especifican las propiedades de párrafo del texto de una forma. DEBE tener un elemento primario **ShapeSheet_Type** o un elemento primario **StyleSheet_Type** .  <br/> |[Sección de párrafo](paragraph-section.md) <br/> |
|Reviewer  <br/> |Una colección de propiedades que se usan para la evaluación de fórmulas. DEBE tener un elemento primario **DocumentSheet_Type** .  <br/> |[Sección de revisor](reviewer-section.md) <br/> |
|Roza  <br/> |Una colección de propiedades que se usan para la evaluación de fórmulas. DEBE tener un elemento primario **DocumentSheet_Type**, **PageSheet_Type**o **ShapeSheet_Type** .  <br/> |[Sección de borrador](scratch-section.md) <br/> |
|Pestañas  <br/> |Colección de propiedades relacionadas que especifican las propiedades Tabs del texto de una forma. DEBE tener un elemento primario **ShapeSheet_Type** o un elemento primario **StyleSheet_Type** .  <br/> |[Sección de tabulaciones](tabs-section.md) <br/> |
   

