---
title: Elemento de celda (sección de geometría) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Define las propiedades que determinan las propiedades de formato y el comportamiento con respecto a las líneas y arcos que constituyen la sección de geometría.
ms.openlocfilehash: ebfdb4dc7809f8883143fdda39f873a36f7bf896
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389312"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Elemento de celda (sección de geometría) ('XML de Visio')

Define las propiedades que determinan las propiedades de formato y el comportamiento con respecto a las líneas y arcos que constituyen la sección de geometría.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
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
|[Elemento de fila (geometría)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Define las propiedades que determinan las propiedades de formato y el comportamiento con respecto a las líneas y arcos que constituyen la sección de geometría.  <br/> |
   
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
|NoFill  <br/> |Indica si un trazado puede rellenarse.  <br/> |[Celda NoFill (Sección de Geometría)](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Determina si se dibuja una línea alrededor del límite del trazado.  <br/> |[Celda NoLine (Sección de Geometría)](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Determina si una forma se puede seleccionar o arrastrar cuando el usuario hace clic en el área con relleno definido por la sección de geometría.  <br/> |[Celda NoQuickDrag (sección Geometría)](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Indica si un trazado se muestra en la página de dibujo.  <br/> |[Celda NoShow (Sección de Geometría)](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Determina si otras formas se ajustan a un trazado.  <br/> |[Celda NoSnap (Sección de Geometría)](nosnap-cell-geometry-section.md) <br/> |
   

