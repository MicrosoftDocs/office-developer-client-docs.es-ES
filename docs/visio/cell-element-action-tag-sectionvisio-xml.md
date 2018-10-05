---
title: Elemento de celda (sección de etiqueta de acción) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Define una propiedad para una etiqueta de acción en una forma o página.
ms.openlocfilehash: 61fad8575532adde0106ef6db2888fe38f3ae4b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392504"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Elemento de celda (sección de etiqueta de acción) ('XML de Visio')

Define una propiedad para una etiqueta de acción en una forma o página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Masters.XML, maestra # .xml, pages.xml, página # .xml  <br/> |
   
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
|[Elemento Row (sección ActionTag)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Define una etiqueta de acción en una forma o página.  <br/> |
   
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
|ButtonFace  <br/> |Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción.  <br/> |[Celda ButtonFace (sección de etiquetas de acción)](buttonface-cell-action-tags-section.md) <br/> |
|Descripción  <br/> |Contiene una cadena que describe la etiqueta de acción, que aparece como información sobre herramientas cuando los usuarios sitúan el puntero sobre la etiqueta.  <br/> |[Celda Description (sección de etiquetas de acción)](description-cell-action-tags-section.md) <br/> |
|Deshabilitado  <br/> |Indica si la etiqueta de acción aparece en la ventana de dibujo.  <br/> |[Celda Disabled (sección de etiquetas de acción)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o todo el tiempo.  <br/> |[Celda DisplayMode (sección de etiquetas de acción)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Nombre de la etiqueta de acción empleado como clave para asociarla con sus acciones.  <br/> |[Celda TagName (sección de etiquetas de acción)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |La posición de la coordenada x de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción.  <br/> |[Celda X (sección de etiquetas de acción)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Desplazamiento en x del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.  <br/> |[Celda X Justify (sección de etiquetas de acción)](x-justify-cell-action-tags-section.md) <br/> |
|v  <br/> |La posición de la coordenada y de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción.  <br/> |[Celda Y (sección de etiquetas de acción)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |El desplazamiento en y del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.  <br/> |[Celda Y Justify (sección de etiquetas de acción)](y-justify-cell-action-tags-section.md) <br/> |
   

