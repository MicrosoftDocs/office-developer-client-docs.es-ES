---
title: Elemento de celda (sección Paragraph) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Especifica un atributo para el texto de la forma, como sangrías, espaciado de líneas, viñetas o alineación horizontal de los párrafos de formato de párrafo.
ms.openlocfilehash: 38309d3d1158b02084af6686c483547b28b8995f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821726"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Elemento de celda (sección Paragraph) ('XML de Visio')

Especifica un atributo para el texto de la forma, como sangrías, espaciado de líneas, viñetas o alineación horizontal de los párrafos de formato de párrafo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Elemento Row (sección de párrafo)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |Especifica un atributo para el texto de la forma, como sangrías, espaciado de líneas, viñetas o alineación horizontal de los párrafos de formato de párrafo.  <br/> |
   
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
   
## <a name="remarks"></a>Notas

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet. Hacer referencia a la tabla siguiente para determinar los valores del atributo **N** permitidas para este elemento de **celda** . 
  
|**Valor**|**Descripción**|**Obtener más información**|
|:-----|:-----|:-----|
|Bullet  <br/> |Determina el estilo de viñetas.  <br/> |[Celda Bullet (Sección de párrafo)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |Representa el número de la fuente empleada para dar formato al texto cuando se especifica una cadena de viñeta personalizada y el valor de la celda Bullet no es cero.  <br/> |[Celda BulletFont (Sección de párrafo)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |Especifica el tamaño de una viñeta.  <br/> |[Celda BulletSize (Sección de párrafo)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |Permite crear un estilo de viñeta personalizado.  <br/> |[Celda BulletString (Sección de párrafo)](bulletstring-cell-paragraph-section.md) <br/> |
|Marcas  <br/> |Indica si el texto se lee de izquierda a derecha o al revés.  <br/> |[Celda Flags (Sección de párrafo)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |Determina la alineación horizontal de los caracteres del bloque de texto de una forma.  <br/> |[Celda HAlign (Sección de párrafo)](halign-cell-paragraph-section.md) <br/> |
|IndFirst  <br/> |Representa la distancia de separación que existe entre la primera línea de cada párrafo en el bloque de texto y la sangría izquierda del párrafo. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría de la primera línea permanece igual.  <br/> |[Celda IndFirst (Sección de párrafo)](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen izquierdo del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría izquierda permanece igual.  <br/> |[Celda IndLeft (Sección de párrafo)](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen derecho del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría derecha permanece igual.  <br/> |[Celda IndRight (Sección de párrafo)](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |Determina el espacio insertado después de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del último párrafo de un bloque de texto, la celda BottomMargin.  <br/> |[Celda SpAfter (Sección de párrafo)](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |Determina el espacio insertado antes de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del primer párrafo de un bloque de texto, la celda TopMargin.  <br/> |[Celda SpBefore (Sección de párrafo)](spbefore-cell-paragraph-section.md) <br/> |
|SpLine  <br/> |Determina la distancia entre una línea de texto y la siguiente, expresada como un porcentaje, donde 100% es el alto de una línea de texto.  <br/> |[Celda SpLine (Sección de párrafo)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |Representa la distancia entra la primera línea del párrafo y la viñeta.  <br/> |[Celda TextPosAfterBullet (Sección de párrafo)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

