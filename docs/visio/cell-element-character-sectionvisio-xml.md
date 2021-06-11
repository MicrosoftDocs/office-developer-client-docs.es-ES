---
title: Elemento Cell (Sección de caracteres) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, caso, posición relativa a la línea base o tamaño de punto.
ms.openlocfilehash: a7d67aa3c53f3a4c673151afc991202904f0557b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540087"
---
# <a name="cell-element-character-section-visio-xml"></a>Elemento Cell (Sección de caracteres) (Visio XML)

Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, caso, posición relativa a la línea base o tamaño de punto.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (Sección de caracteres)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, caso, posición relativa a la línea base o tamaño de punto.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que la fórmula se evalúa como un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las cadenas siguientes:  <br/>  '(alguna fórmula)' si la fórmula existe localmente  <br/>  `No Formula` si la fórmula se elimina o bloquea localmente  <br/>  `Inh` si la fórmula se hereda.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa una unidad de medida El valor predeterminado es DL.  <br/> |Las unidades de la celda.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |Valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a celdas ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** permitidos para este **elemento Cell.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|AsianFont  <br/> |Contiene la enumeración de la fuente usada para dar formato a una ejecución de texto que contiene caracteres asiáticos.  <br/> |[Celda AsianFont (Sección de caracteres)](asianfont-cell-character-section.md) <br/> |
|Case  <br/> |Determina el caso de la ejecución de texto de una forma.  <br/> |[Celda Case (Sección de caracteres)](case-cell-character-section.md) <br/> |
|Color  <br/> |Determina el color usado para la ejecución de texto de una forma.  <br/> |[Celda Color (Sección de caracteres)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Determina el grado de transparencia del color de ejecución de texto de una capa o forma, de 0 (completamente opaca) a 1 (completamente transparente).  <br/> |Ninguno.  <br/> |
|ComplexScriptFont  <br/> |Contiene el número de fuente usada para dar formato a una ejecución de texto compuesta de caracteres de script complejos.  <br/> |[Celda ComplexScriptFont (Sección de caracteres)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Tamaño de la fuente usada para dar formato a una ejecución de texto compuesta de caracteres de script complejos.  <br/> |[Celda ComplexScriptSize (Sección de caracteres)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Determina si el intervalo de una ejecución de texto tiene un subrayado doble debajo.  <br/> |[Celda DoubleULine (Sección de caracteres)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Determina si una ejecución de texto tiene el formato de tachado doble.  <br/> |[Celda DoubleStrikethrough (Sección de caracteres)](doublestrikethrough-cell-character-section.md) <br/> |
|Fuente  <br/> |Representa el número de fuente usada para dar formato a una ejecución de texto.  <br/> |[Celda Font (Sección de caracteres)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Especifica el ancho de fuente.  <br/> |Ninguno.  <br/> |
|LangID  <br/> |Indica el idioma en el que se ha escrito una ejecución de texto.  <br/> |[Celda LangID (Sección de caracteres)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Especifica la cantidad de espacio entre dos o más caracteres. El espacio puede aumentar o disminuir en incrementos de 1/20 de punto.  <br/> |Ninguno.  <br/> |
|Overline  <br/> |Determina si una ejecución de texto tiene una línea encima.  <br/> |[Celda Overline (Sección de caracteres)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Determina la posición de la ejecución de texto de una forma con relación a la línea base.  <br/> |[Celda Pos (Sección de caracteres)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Determina el tamaño de un texto ejecutado en el bloque de texto de la forma.  <br/> |[Celda Size (Sección de caracteres)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Determina si una ejecución de texto tiene el formato tachado.  <br/> |[Celda Strikethru (Sección de caracteres)](strikethru-cell-character-section.md) <br/> |
|Estilo  <br/> |Muestra el formato de carácter aplicado a un intervalo de un texto ejecutado en el bloque de texto de la forma.  <br/> |[Celda Style (Sección de caracteres)](style-cell-character-section.md) <br/> |
   

