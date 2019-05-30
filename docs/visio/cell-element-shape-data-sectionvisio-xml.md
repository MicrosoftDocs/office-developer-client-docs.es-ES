---
title: Elemento cell (sección datos de formas) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Especifica una propiedad de los datos de formas.
ms.openlocfilehash: 3a6238f19f27d001d3c9eebcbcec720822a0ed40
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539379"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Elemento cell (sección datos de formas) (XML de Visio)

Especifica una propiedad de los datos de formas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (sección datos de formas)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Forma Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Especifica una entrada de datos de formas para asociar datos a una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |opcional  <br/> |Indica que la fórmula da como resultado un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd: String  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las siguientes cadenas:  <br/>  ' (alguna fórmula) ' si la fórmula existe localmente  <br/>  `No Formula`Si la fórmula se ha eliminado o bloqueado localmente  <br/>  `Inh`Si la fórmula es heredada.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd: String  <br/> |opcional  <br/> |Representa una unidad de medida el valor predeterminado es DL.  <br/> |Unidades de la celda.  <br/> |
|V  <br/> |xsd: String  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |El valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Observaciones

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento de **celda** . 
  
|**Value**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Calendario  <br/> |Especifica el tipo de calendario utilizado cuando el tipo de un elemento de datos de formas es Fecha.  <br/> |[Celda Calendar (Sección de datos de formas)](calendar-cell-shape-data-section.md) <br/> |
|Enlazado a un vínculo  <br/> |Indica si la fila de datos de la forma está actualmente vinculada a un campo de un conjunto de registros de datos.  <br/> ||
|Formato  <br/> |Especifica el formato de un elemento de datos de formas que puede ser una cadena, una lista fija, un número, una lista variable, una fecha u hora, una duración o una moneda.  <br/> |[Celda Format (Sección de datos de formas)](format-cell-shape-data-section.md) <br/> |
|Invisible  <br/> |Especifica si el elemento de datos de formas es visible en la ventana Datos de formas.  <br/> |[Celda Invisible (Sección de datos de formas)](invisible-cell-shape-data-section.md) <br/> |
|Label  <br/> |Especifica la etiqueta que se muestra a los usuarios en la ventana Datos de formas. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_).  <br/> |[Celda Label (Sección de datos de formas)](label-cell-shape-data-section.md) <br/> |
|Idioma  <br/> |Indica el idioma del valor de los datos de formas.  <br/> |[Celda LangID (Sección de datos de formas)](langid-cell-shape-data-section.md) <br/> |
|Prompt  <br/> |Especifica un texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana Datos de formas.  <br/> |[Celda Prompt (Sección de datos de formas)](prompt-cell-shape-data-section.md) <br/> |
|Criterio  <br/> |Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana Datos de formas.  <br/> |[Celda SortKey (Sección de datos de formas)](sortkey-cell-shape-data-section.md) <br/> |
|Tipo  <br/> |Especifica un tipo de datos para el valor de los datos de formas.  <br/> |[Celda Type (Sección de datos de formas)](type-cell-shape-data-section.md) <br/> |
|Valor  <br/> |Contiene el valor del elemento de datos de formas tal como se especificó en el cuadro de diálogo Definir datos de formas.  <br/> |[Celda Value (Sección de datos de formas)](value-cell-shape-data-section.md) <br/> |
|Comprueba  <br/> |Especifica si se le pide al usuario que escriba información de propiedad personalizada de una forma cuando se crea una instancia o se duplica o copia la forma.  <br/> |Ninguno.  <br/> |
   

