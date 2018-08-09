---
title: Elemento de sección (Sheet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Especifica una colección de propiedades relacionadas.
ms.openlocfilehash: 7cb5e1c30960e69b252abc7af38e021607fd3502
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823119"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Elemento de sección (Sheet_Type complexType) ('XML de Visio')

Especifica una colección de propiedades relacionadas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.XML, masters.xml, maestra # .xml, pages.xml, página # .xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de un dibujo.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de una página en un dibujo.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[complexType Master_Type](master_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociadas con el patrón.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica una colección de las propiedades asociadas con una forma.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Especifica una colección de las propiedades asociadas con un estilo, dibujo, dibujo página o una forma.  <br/> |
|[Hoja de estilos](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Especifica una hoja de estilos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad única.  <br/> |
|[Row](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Especifica una colección de elementos de **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPR  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si se ha eliminado una colección que en caso contrario, ¿se heredan. DEBE ser igual a 0 o 1. Un valor de 1 especifica que la colección no se usa y que se debe omitir. Un valor de 0 especifica que la colección de propiedades es válida para la forma. Si el atributo **SUPR** no está presente, el valor es 0.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el índice de base cero del elemento. DEBE ser único entre todos los elementos de **Section_Type** con el mismo atributo **N** de la que contiene **Sheet_Type**. DEBE ser mayor que el atributo **IX** de cualquier elemento de **Section_Type** anterior con el mismo atributo **N** de la que contiene **Sheet_Type**.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el nombre independiente del idioma de la colección de propiedades. DEBE ser único entre todos los elementos **Section_Type** del elemento **Sheet_Type** que lo contiene, a menos que sea igual a "Geometría". DEBE ser igual que un subtítulo en **secciones**.  <br/> |Valores del tipo XSD: String.  <br/> |
   
### <a name="remarks"></a>Comentarios

El atributo **N** de este elemento de la **sección** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de **ShapeSheet** . Hacer referencia a la tabla siguiente para determinar los valores del atributo **N** permitidas para este elemento de **sección** . 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Actions  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula. DEBE tener un elemento primario **ShapeSheet_Type** o **PageSheet_Type** .  <br/> |[Sección de acciones](actions-section.md) <br/> |
|ActionTag  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula sólo. DEBE tener un elemento primario **ShapeSheet_Type** o **PageSheet_Type** .  <br/> |[Sección de la etiqueta de acción](action-tag-section.md) <br/> |
|Connections  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula sólo. DEBE tener un elemento primario de **ShapeSheet_Type** .  <br/> ||
|Controles  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula sólo. DEBE tener un elemento primario de **ShapeSheet_Type** .  <br/> |[Sección de controles](controls-section.md) <br/> |
|Hipervínculo  <br/> |Una colección de propiedades relacionadas que especifican los hipervínculos de la forma. DEBE tener un elemento primario de **ShapeSheet_Type** .  <br/> |[Sección de hipervínculos](hyperlinks-section.md) <br/> |
|Formas de datos  <br/> |Una colección de propiedades relacionadas que especifique los datos de formas. DEBE tener un elemento primario de **ShapeSheet_Type** .  <br/> |[Sección de datos de formas](shape-data-section.md) <br/> |
|User  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula. DEBE tener un elemento primario **DocumentSheet_Type**, **PageSheet_Type**o **ShapeSheet_Type** .  <br/> |[Sección de celdas definidas por el usuario](user-defined-cells-section.md) <br/> |
   
El atributo **IX** de este elemento de la **sección** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de **ShapeSheet** . Hacer referencia a la tabla siguiente para determinar los valores del atributo **IX** que están permitidos para este elemento de **sección** . 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Annotation  <br/> |Una colección de propiedades que contienen información sobre los comentarios insertados en una página de documento.  <br/> |[Sección de anotación](annotation-section.md) <br/> |
|Carácter  <br/> |Una colección de propiedades relacionadas que especifican las propiedades de carácter del texto de una forma. DEBE tener un elemento primario de **ShapeSheet_Type** o un elemento primario de **StyleSheet_Type** .  <br/> |[Sección de caracteres](character-section.md) <br/> |
|Connections  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula sólo. DEBE tener un elemento primario de **ShapeSheet_Type** .  <br/> |[Sección de puntos de conexión](connection-points-section.md) <br/> |
|Field  <br/> |Una colección de propiedades relacionadas que especifican los campos de texto de una forma. DEBE tener un elemento primario de **ShapeSheet_Type** .  <br/> |[Sección de campos de texto](text-fields-section.md) <br/> |
|FillGradient  <br/> |Una colección de propiedades que especifican el degradado de color de relleno de una forma. DEBE tener un elemento primario **ShapeSheet_Type** o **StyleSheet_Type** .  <br/> |[Sección Degradado de relleno](fill-gradient-section.md) <br/> |
|Geometría  <br/> |Una colección de propiedades relacionadas que especifican la visualización de geometría. DEBE tener un elemento primario de **ShapeSheet_Type** . El primer elemento secundario de **Row_Type** de este elemento debe ser del tipo MoveTo, RelMoveTo, Ellipse o InfiniteLine.  <br/> |[Sección de geometría](geometry-section.md) <br/> |
|Layers  <br/> |Una colección de propiedades que se muestran todas las capas definidas en una página de dibujo. DEBE ser el elemento secundario de un elemento **PageSheet_Type** .  <br/> |[Sección de capas](layers-section.md) <br/> |
|Línea degradado  <br/> |Una colección de propiedades relacionadas que especifican el degradado de color de línea de una forma. DEBE tener un elemento primario **ShapeSheet_Type** o **StyleSheet_Type** .  <br/> |[Sección Degradado de línea](line-gradient-section.md) <br/> |
|Paragraph  <br/> |Una colección de propiedades relacionadas que especifican las propiedades de párrafo del texto de una forma. DEBE tener un elemento primario de **ShapeSheet_Type** o un elemento primario de **StyleSheet_Type** .  <br/> |[Sección de párrafo](paragraph-section.md) <br/> |
|Reviewer  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula. DEBE tener un elemento primario de **DocumentSheet_Type** .  <br/> |[Sección de revisor](reviewer-section.md) <br/> |
|Principio  <br/> |Una colección de propiedades que se usan para la evaluación de la fórmula. DEBE tener un elemento primario **DocumentSheet_Type**, **PageSheet_Type**o **ShapeSheet_Type** .  <br/> |[Sección de borrador](scratch-section.md) <br/> |
|Pestañas  <br/> |Una colección de propiedades relacionadas que especifican las propiedades de las fichas del texto de una forma. DEBE tener un elemento primario de **ShapeSheet_Type** o un elemento primario de **StyleSheet_Type** .  <br/> |[Sección de tabulaciones](tabs-section.md) <br/> |
   

