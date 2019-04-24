---
title: Elemento cell (sección geometría) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Define las propiedades que determinan el formato y las propiedades de comportamiento con respecto a las líneas y los arcos que componen la sección de geometría.
ms.openlocfilehash: ebfdb4dc7809f8883143fdda39f873a36f7bf896
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356059"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Elemento cell (sección geometría) ("XML" de Visio)

Define las propiedades que determinan el formato y las propiedades de comportamiento con respecto a las líneas y los arcos que componen la sección de geometría.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML, página #. XML  <br/> |
   
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
|[Elemento Row (geometría)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Define las propiedades que determinan el formato y las propiedades de comportamiento con respecto a las líneas y los arcos que componen la sección de geometría.  <br/> |
   
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
|NoFill  <br/> |Indica si un trazado puede rellenarse.  <br/> |[Celda NoFill (Sección de Geometría)](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Determina si se dibuja una línea alrededor del límite del trazado.  <br/> |[Celda NoLine (Sección de Geometría)](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Determina si una forma se puede seleccionar o arrastrar cuando el usuario hace clic en el área rellena definida por la sección Geometry.  <br/> |[Celda NoQuickDrag (sección de geometría)](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Indica si un trazado se muestra en la página de dibujo.  <br/> |[Celda NoShow (Sección de Geometría)](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Determina si otras formas se ajustan a un trazado.  <br/> |[Celda NoSnap (Sección de Geometría)](nosnap-cell-geometry-section.md) <br/> |
   

