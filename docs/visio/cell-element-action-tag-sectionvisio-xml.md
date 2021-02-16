---
title: Elemento Cell (Sección de etiquetas de acción) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Define una propiedad para una etiqueta de acción en una forma o página.
ms.openlocfilehash: 3b43206838dae432df677a3ff8792c85328db53b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538805"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Elemento Cell (Sección de etiquetas de acción) (XML de Visio)

Define una propiedad para una etiqueta de acción en una forma o página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (Sección de ActionTag)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Define una etiqueta de acción en una forma o página.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que la fórmula se evalúa como un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las siguientes cadenas:  <br/>  '(alguna fórmula)' si la fórmula existe localmente  <br/>  `No Formula` si la fórmula se elimina o bloquea localmente  <br/>  `Inh` si la fórmula se hereda.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa una unidad de medida El valor predeterminado es DL.  <br/> |Las unidades de la celda.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |Valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a celdas ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este **elemento Cell.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|ButtonFace  <br/> |Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción.  <br/> |[Celda ButtonFace (sección de etiquetas de acción)](buttonface-cell-action-tags-section.md) <br/> |
|Description  <br/> |Contiene una cadena que describe la etiqueta de acción, que aparece como información sobre herramientas cuando los usuarios sitúan el puntero sobre la etiqueta.  <br/> |[Celda Description (sección de etiquetas de acción)](description-cell-action-tags-section.md) <br/> |
|Deshabilitado  <br/> |Indica si la etiqueta de acción aparece en la ventana de dibujo.  <br/> |[Celda Disabled (sección de etiquetas de acción)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o siempre.  <br/> |[Celda DisplayMode (sección de etiquetas de acción)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Nombre de la etiqueta de acción empleado como clave para asociarla con sus acciones.  <br/> |[Celda TagName (sección de etiquetas de acción)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |La posición de la coordenada x de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción.  <br/> |[Celda X (sección de etiquetas de acción)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Desplazamiento en x del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.  <br/> |[Celda X Justify (sección de etiquetas de acción)](x-justify-cell-action-tags-section.md) <br/> |
|v  <br/> |La posición de la coordenada y de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción.  <br/> |[Celda Y (sección de etiquetas de acción)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |El desplazamiento en y del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.  <br/> |[Celda Y Justify (sección de etiquetas de acción)](y-justify-cell-action-tags-section.md) <br/> |
   

