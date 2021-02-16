---
title: Elemento Cell (fila Actions) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Especifica una propiedad de una acción asociada a un comando personalizado en un menú contextual o de etiqueta de acción.
ms.openlocfilehash: 8cce85bdfb7d0ce54d968e00cda56e4e6c2455bc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538784"
---
# <a name="cell-element-actions-row-visio-xml"></a>Elemento Cell (fila Actions) (XML de Visio)

Especifica una propiedad de una acción asociada a un comando personalizado en un menú contextual o de etiqueta de acción.
  
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

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (Sección de acciones)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una acción asociada a un comando personalizado en un menú contextual o de etiqueta de acción.  <br/> |
   
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

El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este **elemento Cell.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Action  <br/> |Contiene la fórmula que se va a ejecutar cuando un usuario elige un comando en un menú contextual o de etiquetas de acción.  <br/> |[Celda Action (sección de acciones)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Indica si se inserta un separador en el menú encima de esta acción.  <br/> |[Celda BeginGroup (Sección de acciones)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.  <br/> |[Celda ButtonFace (sección de acciones)](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Indica si un elemento aparece activado en el menú contextual o de etiquetas de acción.  <br/> |[Celda Checked (sección de acciones)](checked-cell-actions-section.md) <br/> |
|Deshabilitado  <br/> |Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.  <br/> |[Celda Disabled (sección de acciones)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente.  <br/> |[Celda FlyoutChild (Sección de acciones)](flyoutchild-cell-actions-section.md) <br/> |
|Invisible  <br/> |Indica si la acción está visible en el menú contextual o de etiqueta de acción.  <br/> |[Celda Invisible (sección de acciones)](invisible-cell-actions-section.md) <br/> |
|Menú  <br/> |Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página.  <br/> |[Celda Menu (sección de acciones)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Controla si la acción de un menú contextual o de etiqueta de acción es de sólo lectura.  <br/> |[Celda ReadOnly (sección de acciones)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Un número que determina el orden de las acciones que aparecen en un menú contextual o de etiqueta de acción.  <br/> |[Celda SortKey (Sección de acciones) Celda SortKey (Sección de acciones)](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Contiene el nombre de la etiqueta de acción a la que está asociada esta acción.  <br/> |[Celda TagName (sección de acciones)](tagname-cell-actions-section.md) <br/> |
   

