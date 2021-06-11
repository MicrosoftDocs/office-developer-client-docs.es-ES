---
title: Elemento Cell (fila SplineStart) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 021536b9-6724-4b8a-35c2-966e456e5232
description: Contiene coordenadas x o y para el segundo punto de control de una spline, su segundo nudo, su primer nudo, el último nudo o el grado de la spline.
ms.openlocfilehash: e3a99818d897af21e3064e0fc92d9d56ffcf5a15
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539358"
---
# <a name="cell-element-splinestart-row-visio-xml"></a>Elemento Cell (fila SplineStart) (Visio XML)

Contiene coordenadas x o y para el segundo punto de control de una spline, su segundo nudo, su primer nudo, el último nudo o el grado de la spline.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[SplineStart_Type](splinestart_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y para el segundo punto de control de una spline, su segundo nudo, su primer nudo, el último nudo o el grado de la spline.  <br/> |
   
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
|X  <br/> |Coordenada x del segundo punto de control de una spline.  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del segundo punto de control de una spline.  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
|A  <br/> |Segundo nodo de la spline.  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
|B  <br/> |Primer nodo de una spline.  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
|C  <br/> |Último nodo de una spline.  <br/> |[Fila RelEllipticalArcTo (sección Geometría)](splinestart-row-geometry-section.md) <br/> |
|D  <br/> |Grado de la spline (un número entero entre 1 y 25).  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
   

