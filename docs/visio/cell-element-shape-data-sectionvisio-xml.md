---
title: Elemento de celda (sección de datos de formas) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Especifica una propiedad de los datos de formas.
ms.openlocfilehash: 5e0c79d9439fb3800a277e039143060eec708b11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390649"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Elemento de celda (sección de datos de formas) ('XML de Visio')

Especifica una propiedad de los datos de formas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (sección Datos de forma)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Forma Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Especifica una entrada de datos de formas para asociar datos con una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |opcional  <br/> |Indica que la fórmula da como resultado un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd: String  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener uno de las siguientes cadenas:  <br/>  '(algunos fórmula)' Si la fórmula existe localmente  <br/>  `No Formula`Si la fórmula se ha eliminado localmente o bloqueada  <br/>  `Inh`Si la fórmula es heredada.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |El nombre de la celda ShapeSheet.  <br/> Vea la sección comentarios que aparece a continuación.  <br/> |
|U  <br/> |xsd: String  <br/> |opcional  <br/> |Representa una unidad de medida, el valor predeterminado es DL.  <br/> |Las unidades de la celda.  <br/> |
|V  <br/> |xsd: String  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |El valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet. Hacer referencia a la tabla siguiente para determinar los valores del atributo **N** permitidas para este elemento de **celda** . 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Calendario  <br/> |Especifica el tipo de calendario utilizado cuando el tipo de un elemento de datos de formas es Fecha.  <br/> |[Celda Calendar (Sección de datos de formas)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Indica si la fila de datos de formas está vinculada a un campo en un conjunto de registros de datos.  <br/> ||
|Formato  <br/> |Especifica el formato de un elemento de datos de formas que puede ser una cadena, una lista fija, un número, una lista variable, una fecha u hora, una duración o una moneda.  <br/> |[Celda Format (Sección de datos de formas)](format-cell-shape-data-section.md) <br/> |
|Invisible  <br/> |Especifica si el elemento de datos de formas es visible en la ventana Datos de formas.  <br/> |[Celda Invisible (Sección de datos de formas)](invisible-cell-shape-data-section.md) <br/> |
|Etiqueta  <br/> |Especifica la etiqueta que se muestra a los usuarios en la ventana Datos de formas. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_).  <br/> |[Celda Label (Sección de datos de formas)](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Indica el idioma del valor de los datos de formas.  <br/> |[Celda LangID (Sección de datos de formas)](langid-cell-shape-data-section.md) <br/> |
|Prompt  <br/> |Especifica un texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana Datos de formas.  <br/> |[Celda Prompt (Sección de datos de formas)](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana Datos de formas.  <br/> |[Celda SortKey (Sección de datos de formas)](sortkey-cell-shape-data-section.md) <br/> |
|Tipo  <br/> |Especifica un tipo de datos para el valor de los datos de formas.  <br/> |[Celda Type (Sección de datos de formas)](type-cell-shape-data-section.md) <br/> |
|Valor  <br/> |Contiene el valor del elemento de datos de formas tal como se especificó en el cuadro de diálogo Definir datos de formas.  <br/> |[Celda Value (Sección de datos de formas)](value-cell-shape-data-section.md) <br/> |
|Comprobar  <br/> |Especifica si el usuario se le pide que escriba la información de propiedad personalizada de una forma cuando se crea una instancia o se duplica o copia la forma.  <br/> |Ninguno.  <br/> |
   

