---
title: Elemento cell (sección carácter) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Especifica un atributo de formato para la ejecución de texto de una forma, como la fuente, el color, el estilo, el caso, la posición relativa a la línea base o el tamaño en puntos.
ms.openlocfilehash: 6dd895b33353944d27abb0d64a6a6df64ca19896
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356087"
---
# <a name="cell-element-character-section-visio-xml"></a>Elemento cell (sección carácter) ("XML" de Visio)

Especifica un atributo de formato para la ejecución de texto de una forma, como la fuente, el color, el estilo, el caso, la posición relativa a la línea base o el tamaño en puntos.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML, Master #. XML, página #. XML  <br/> |
   
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
|[Elemento Row (sección de caracteres)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato para la ejecución de texto de una forma, como la fuente, el color, el estilo, el caso, la posición relativa a la línea base o el tamaño en puntos.  <br/> |
   
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
   
## <a name="remarks"></a>Comentarios

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento de **celda** . 
  
|**Value**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|AsianFont  <br/> |Contiene la enumeración de la fuente que se utiliza para dar formato a un segmento de texto que contiene caracteres asiáticos.  <br/> |[Celda AsianFont (Sección de caracteres)](asianfont-cell-character-section.md) <br/> |
|Case  <br/> |Determina el caso del segmento de texto de una forma.  <br/> |[Celda Case (Sección de caracteres)](case-cell-character-section.md) <br/> |
|Color  <br/> |Determina el color utilizado para la ejecución de texto de una forma.  <br/> |[Celda Color (Sección de caracteres)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Determina el grado de transparencia del color de ejecución del texto de una capa o una forma, de 0 (completamente opaco) a 1 (completamente transparente).  <br/> |Ninguno.  <br/> |
|ComplexScriptFont  <br/> |Contiene el número de la fuente que se utiliza para dar formato a un segmento de texto compuesto de caracteres de una secuencia de comandos compleja.  <br/> |[Celda ComplexScriptFont (Sección de caracteres)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Tamaño de la fuente que se utiliza para dar formato a un segmento de texto compuesto de caracteres de alfabeto complejo.  <br/> |[Celda ComplexScriptSize (Sección de caracteres)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Determina si el intervalo de una ejecución de texto tiene doble subrayado.  <br/> |[Celda DoubleULine (Sección de caracteres)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Determina si una ejecución de texto tiene formato de doble tachado.  <br/> |[Celda DoubleStrikethrough (Sección de caracteres)](doublestrikethrough-cell-character-section.md) <br/> |
|Fuente  <br/> |Representa el número de la fuente que se utiliza para dar formato a un segmento de texto.  <br/> |[Celda Font (Sección de caracteres)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Especifica el ancho de la fuente.  <br/> |Ninguno.  <br/> |
|Idioma  <br/> |Indica el idioma en el que se ha escrito una ejecución de texto.  <br/> |[Celda LangID (Sección de caracteres)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Especifica la cantidad de espacio entre dos o más caracteres. El espacio puede aumentar o disminuir en incrementos de 1/20 de punto.  <br/> |Ninguno.  <br/> |
|Overline  <br/> |Determina si una ejecución de texto tiene una línea encima.  <br/> |[Celda Overline (Sección de caracteres)](overline-cell-character-section.md) <br/> |
|Solamente  <br/> |Determina la posición del segmento de texto de una forma con respecto a la línea base.  <br/> |[Celda Pos (Sección de caracteres)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Determina el tamaño de un segmento de texto en el bloque de texto de la forma.  <br/> |[Celda Size (Sección de caracteres)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Determina si una ejecución de texto tiene el formato de tachado.  <br/> |[Celda Strikethru (Sección de caracteres)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Muestra el formato de carácter aplicado a un rango de un segmento de texto en el bloque de texto de la forma.  <br/> |[Celda Style (Sección de caracteres)](style-cell-character-section.md) <br/> |
   

