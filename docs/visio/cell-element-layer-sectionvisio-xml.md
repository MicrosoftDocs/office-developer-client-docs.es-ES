---
title: Elemento de celda (sección de capas) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Especifica una propiedad de una capa o sus propiedades de una página.
ms.openlocfilehash: 92be29321ba637bb694c0cf5d3cddcb888618c1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821744"
---
# <a name="cell-element-layer-section-visio-xml"></a>Elemento de celda (sección de capas) ('XML de Visio')

Especifica una propiedad de una capa o sus propiedades de una página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Masters.XML, pages.xml  <br/> |
   
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
|[Elemento Row (sección Capa)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una capa o sus propiedades de una página.  <br/> |
   
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
|Activo  <br/> |Especifica si una capa está activa.  <br/> |Ninguno.  <br/> |
|Color  <br/> |Especifica uno de los siguientes: el índice del color en la tabla de color utilizado para mostrar la capa o un valor RGB que especifica un color personalizado no está en la tabla de colores.  <br/> |Ninguno.  <br/> |
|ColorTrans  <br/> |Determina el grado de transparencia de una capa o el color del texto de la forma, de 0 (completamente opaco) a 1 (completamente transparente).  <br/> |Ninguno.  <br/> |
|Pegado  <br/> |Especifica si las formas que pertenecen a la capa pueden pegarse a.  <br/> |Ninguno.  <br/> |
|Lock  <br/> |Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.  <br/> |Ninguno.  <br/> |
|Nombre  <br/> |El nombre de una capa.  <br/> |Ninguno.  <br/> |
|NameUniv  <br/> |Especifica el nombre universal de una capa.  <br/> |Ninguno.  <br/> |
|Imprimir  <br/> |Especifica si las formas que pertenecen a la capa se imprimen cuando se imprime el dibujo.  <br/> |Ninguno.  <br/> |
|Complemento  <br/> |Especifica si otras formas se pueden ajustar a formas asignadas a la capa.  <br/> |Ninguno.  <br/> |
|Status  <br/> |Especifica si la capa es una capa válida para un documento.  <br/> |Ninguno.  <br/> |
|Visible  <br/> |Especifica si las formas de la capa son visibles en la página de dibujo.  <br/> |Ninguno.  <br/> |
   

