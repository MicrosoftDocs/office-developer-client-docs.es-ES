---
title: Elemento de celda (sección Character) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, caso, posición relativa a la línea base o tamaño en puntos.
ms.openlocfilehash: 6dd895b33353944d27abb0d64a6a6df64ca19896
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384251"
---
# <a name="cell-element-character-section-visio-xml"></a>Elemento de celda (sección Character) ('XML de Visio')

Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, caso, posición relativa a la línea base o tamaño en puntos.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.XML, master # .xml, # .xml de página  <br/> |
   
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
|[Elemento Row (sección Carácter)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, caso, posición relativa a la línea base o tamaño en puntos.  <br/> |
   
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
|AsianFont  <br/> |Contiene la enumeración de la fuente empleada para dar formato a un segmento que contiene caracteres asiáticos de texto.  <br/> |[Celda AsianFont (Sección de caracteres)](asianfont-cell-character-section.md) <br/> |
|Case  <br/> |Determina el caso de ejecución de texto de una forma.  <br/> |[Celda Case (Sección de caracteres)](case-cell-character-section.md) <br/> |
|Color  <br/> |Determina el color utilizado para la ejecución de texto de una forma.  <br/> |[Celda Color (Sección de caracteres)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Determina el grado de transparencia de una capa o texto de la forma que se ejecute el color, desde 0 (completamente opaco) a 1 (completamente transparente).  <br/> |Ninguna.  <br/> |
|ComplexScriptFont  <br/> |Contiene el número de la fuente empleada para dar formato a un texto ejecutar compuesta por caracteres de un alfabeto complejo.  <br/> |[Celda ComplexScriptFont (Sección de caracteres)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |El tamaño de la fuente empleada para dar formato a un texto ejecute compuesta por caracteres de un alfabeto complejo.  <br/> |[Celda ComplexScriptSize (Sección de caracteres)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Determina si el intervalo de un segmento de texto tiene doble subrayado.  <br/> |[Celda DoubleULine (Sección de caracteres)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Determina si un segmento de texto tiene el formato de tachado doble.  <br/> |[Celda DoubleStrikethrough (Sección de caracteres)](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Representa el número de la fuente empleada para dar formato a un segmento de texto.  <br/> |[Celda Font (Sección de caracteres)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Especifica el ancho de la fuente.  <br/> |Ninguna.  <br/> |
|LangID  <br/> |Indica el idioma en el que se ha escrito una ejecución de texto.  <br/> |[Celda LangID (Sección de caracteres)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Especifica la cantidad de espacio entre dos o más caracteres. Espacio puede sumar o restar en incrementos de 1/20 de punto.  <br/> |Ninguna.  <br/> |
|Overline  <br/> |Determina si un segmento de texto tiene una línea encima.  <br/> |[Celda Overline (Sección de caracteres)](overline-cell-character-section.md) <br/> |
|POS  <br/> |Determina la posición del texto de una forma ejecutar con respecto a la línea base.  <br/> |[Celda Pos (Sección de caracteres)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Determina el tamaño de un segmento de bloque de texto de la forma de texto.  <br/> |[Celda Size (Sección de caracteres)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Determina si un segmento de texto tiene el formato tachado.  <br/> |[Celda Strikethru (Sección de caracteres)](strikethru-cell-character-section.md) <br/> |
|Estilo  <br/> |Muestra que el formato de carácter aplicado a un intervalo de texto se ejecute en el bloque de texto de la forma.  <br/> |[Celda Style (Sección de caracteres)](style-cell-character-section.md) <br/> |
   

