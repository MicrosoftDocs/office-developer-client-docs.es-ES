---
title: Elemento Cell (Sección de capa) (Visio XML)
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
# <a name="cell-element-layer-section-visio-xml"></a>Elemento Cell (Sección de capa) (Visio XML)

Especifica una propiedad para una capa o sus propiedades para una página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |masters.xml, pages.xml  <br/> |
   
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
|[Elemento Row (Sección de capa)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Especifica una propiedad para una capa o sus propiedades para una página.  <br/> |
   
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
|Activo  <br/> |Especifica si una capa está activa.  <br/> |Ninguno.  <br/> |
|Color  <br/> |Especifica una de las siguientes opciones: el índice del color de la tabla de colores usada para mostrar la capa o un valor RGB que especifica un color personalizado que no está en la tabla de colores.  <br/> |Ninguno.  <br/> |
|ColorTrans  <br/> |Determina el grado de transparencia del color de texto de una capa o forma, de 0 (completamente opaca) a 1 (completamente transparente).  <br/> |Ninguno.  <br/> |
|Glue  <br/> |Especifica si las formas que pertenecen a la capa se pueden pegar.  <br/> |Ninguno.  <br/> |
|Lock  <br/> |Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.  <br/> |Ninguno.  <br/> |
|Nombre  <br/> |Nombre de una capa.  <br/> |Ninguno.  <br/> |
|NameUniv  <br/> |Especifica el nombre universal de una capa.  <br/> |Ninguno.  <br/> |
|Imprimir  <br/> |Especifica si las formas que pertenecen a la capa se imprimen cuando se imprime el dibujo.  <br/> |Ninguno.  <br/> |
|Acoplar  <br/> |Especifica si otras formas pueden ajustarse a las formas asignadas a la capa.  <br/> |Ninguno.  <br/> |
|Estado  <br/> |Especifica si la capa es una capa válida para un documento.  <br/> |Ninguno.  <br/> |
|Visible  <br/> |Especifica si las formas de la capa son visibles en la página de dibujo.  <br/> |Ninguno.  <br/> |
   

