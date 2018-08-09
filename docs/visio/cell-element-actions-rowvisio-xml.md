---
title: Elemento de celda (fila de acciones) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Especifica una propiedad de una acción asociada con un comando personalizado en un menú contextual o de acción de la etiqueta.
ms.openlocfilehash: d0f103e6f241a7982bcc2663752d9338cf4c3eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821686"
---
# <a name="cell-element-actions-row-visio-xml"></a>Elemento de celda (fila de acciones) ('XML de Visio')

Especifica una propiedad de una acción asociada con un comando personalizado en un menú contextual o de acción de la etiqueta.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Elemento Row (sección Acciones)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una acción asociada con un comando personalizado en un menú contextual o de acción de la etiqueta.  <br/> |
   
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
|Acción  <br/> |Contiene la fórmula que se va a ejecutar cuando un usuario elige un comando en un menú contextual o de etiquetas de acción.  <br/> |[Celda Action (sección de acciones)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Indica si se inserta un separador en el menú encima de esta acción.  <br/> |[Celda BeginGroup (Sección de acciones)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.  <br/> |[Celda ButtonFace (sección de acciones)](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Indica si un elemento aparece activado en el menú contextual o de etiquetas de acción.  <br/> |[Celda Checked (sección de acciones)](checked-cell-actions-section.md) <br/> |
|Deshabilitado  <br/> |Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.  <br/> |[Celda Disabled (sección de acciones)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente.  <br/> |[Celda FlyoutChild (sección Acciones)](flyoutchild-cell-actions-section.md) <br/> |
|Invisible  <br/> |Indica si la acción está visible en el menú contextual o de etiqueta de acción.  <br/> |[Celda Invisible (sección de acciones)](invisible-cell-actions-section.md) <br/> |
|Menú  <br/> |Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página.  <br/> |[Celda Menu (sección de acciones)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Controla si la acción de un menú contextual o de etiqueta de acción es de sólo lectura.  <br/> |[Celda ReadOnly (sección de acciones)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Un número que determina el orden de las acciones que aparecen en un menú contextual o de etiqueta de acción.  <br/> |[Celda de la celda SortKey (sección de acciones) SortKey (sección de acciones)](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Contiene el nombre de la etiqueta de acción a la que está asociada esta acción.  <br/> |[Celda TagName (sección de acciones)](tagname-cell-actions-section.md) <br/> |
   

