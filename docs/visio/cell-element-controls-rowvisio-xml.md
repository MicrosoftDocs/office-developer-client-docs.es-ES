---
title: Elemento Cell (fila Controls) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Contiene una propiedad para un controlador determinado definido para una forma.
ms.openlocfilehash: 662dfe730c92ae25b3d243364bf1fa22a5eb8605
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541839"
---
# <a name="cell-element-controls-row-visio-xml"></a>Elemento Cell (fila Controls) (XML de Visio)

Contiene una propiedad para un controlador determinado definido para una forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Elemento Row (Sección de controles)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Contiene una propiedad para un controlador determinado definido para una forma.  <br/> |
   
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
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa una unidad de medida El valor predeterminado es DL.  <br/> |Unidades de la celda.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |Valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este **elemento Cell.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|CanGlue  <br/> |Determina si un controlador puede pegarse a otras formas.  <br/> |[Celda Can Glue (Sección de controles)](can-glue-cell-controls-section.md) <br/> |
|Prompt  <br/> |Representa una cadena de texto descriptivo que aparece como información de herramientas cuando el usuario deja el puntero sobre el controlador de una forma.  <br/> |[Celda Tip (Sección de controles)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Representa la coordenada x que indica la ubicación del controlador de una forma, en coordenadas locales.  <br/> |[Celda X (Sección de controles)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Especifica el tipo de comportamiento que muestra la coordenada x del controlador después de mover el controlador.  <br/> |Ninguno.  <br/> |
|xDyn  <br/> |Representa la coordenada x de un punto de anclaje del controlador en coordenadas locales.  <br/> |[Celda X Dynamics (Sección de controles)](x-dynamics-cell-controls-section.md) <br/> |
|v  <br/> |Representa la coordenada y que indica la ubicación del controlador de una forma, en coordenadas locales.  <br/> |[Celda Y (Sección de controles)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Especifica el tipo de comportamiento que mostrará la coordenada y del controlador después de mover el controlador.  <br/> |Ninguno.  <br/> |
|YDyn  <br/> |Representa la coordenada y de un punto de anclaje del controlador en coordenadas locales.  <br/> |[Celda Y Dynamics (Sección de controles)](y-dynamics-cell-controls-section.md) <br/> |
   

