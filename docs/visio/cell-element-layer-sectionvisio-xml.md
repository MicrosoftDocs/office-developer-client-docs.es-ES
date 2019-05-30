---
title: Elemento cell (sección capa) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Especifica una propiedad para una capa o sus propiedades para una página.
ms.openlocfilehash: 119c82f84c76f735a5d9b73b4bea8beda0a7e476
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539760"
---
# <a name="cell-element-layer-section-visio-xml"></a>Elemento cell (sección capa) (XML de Visio)

Especifica una propiedad para una capa o sus propiedades para una página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Masters. XML, Pages. XML  <br/> |
   
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
|[Elemento Row (sección capa)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Especifica una propiedad para una capa o sus propiedades para una página.  <br/> |
   
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
   
## <a name="remarks"></a>Observaciones

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento de **celda** . 
  
|**Value**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Activo  <br/> |Especifica si una capa está activa.  <br/> |Ninguno.  <br/> |
|Color  <br/> |Especifica una de las siguientes opciones: índice del color de la tabla de colores que se usa para mostrar la capa o un valor RGB que especifica un color personalizado que no se encuentra en la tabla de colores.  <br/> |Ninguno.  <br/> |
|ColorTrans  <br/> |Determina el grado de transparencia del color del texto de una capa o una forma, de 0 (completamente opaco) a 1 (completamente transparente).  <br/> |Ninguno.  <br/> |
|Permanezca  <br/> |Especifica si las formas que pertenecen a la capa pueden pegarse.  <br/> |Ninguno.  <br/> |
|Lock  <br/> |Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.  <br/> |Ninguno.  <br/> |
|Nombre  <br/> |Nombre de una capa.  <br/> |Ninguno.  <br/> |
|NameUniv  <br/> |Especifica el nombre universal de una capa.  <br/> |Ninguno.  <br/> |
|Print  <br/> |Especifica si las formas que pertenecen a la capa se imprimen al imprimir el dibujo.  <br/> |Ninguno.  <br/> |
|Complemento  <br/> |Especifica si se pueden ajustar otras formas a las formas asignadas a la capa.  <br/> |Ninguno.  <br/> |
|Estado  <br/> |Especifica si la capa es una capa válida para un documento.  <br/> |Ninguno.  <br/> |
|Visible  <br/> |Especifica si las formas de la capa son visibles en la página de dibujo.  <br/> |Ninguno.  <br/> |
   

