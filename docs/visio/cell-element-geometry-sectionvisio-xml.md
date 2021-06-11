---
title: Elemento Cell (sección Geometry) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Define las propiedades que determinan las propiedades de formato y comportamiento con respecto a las líneas y arcos que integran la Sección de geometría.
ms.openlocfilehash: 93cc7e204d97a813fea2db4b84c36dedf19cf5f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539810"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Elemento Cell (sección Geometry) (Visio XML)

Define las propiedades que determinan las propiedades de formato y comportamiento con respecto a las líneas y arcos que integran la Sección de geometría.
  
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

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Define las propiedades que determinan las propiedades de formato y comportamiento con respecto a las líneas y arcos que integran la Sección de geometría.  <br/> |
   
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
|NoFill  <br/> |Indica si un trazado puede rellenarse.  <br/> |[Celda NoFill (Sección de Geometría)](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Determina si se dibuja una línea alrededor del límite del trazado.  <br/> |[Celda NoLine (Sección de Geometría)](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Determina si se puede seleccionar o arrastrar una forma cuando el usuario hace clic en el área rellenada definida por la sección Geometría.  <br/> |[Celda NoQuickDrag (sección Geometría)](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Indica si un trazado se muestra en la página de dibujo.  <br/> |[Celda NoShow (Sección de Geometría)](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Determina si otras formas se ajustan a un trazado.  <br/> |[Celda NoSnap (Sección de Geometría)](nosnap-cell-geometry-section.md) <br/> |
   

