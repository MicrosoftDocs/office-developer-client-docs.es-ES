---
title: Elemento Cell (fila Hyperlink) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.
ms.openlocfilehash: f9526b3e4bb7dc9216a0b72c0a816e136c6e89bf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539796"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Elemento Cell (fila Hyperlink) (XML de Visio)

Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila **Hyperlink** para cada hipervínculo. 
  
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
|[Elemento Row (Sección de hipervínculo)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila **Hyperlink** para cada hipervínculo.  <br/> |
   
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
|Address  <br/> |Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.  <br/> |[Celda Address (Sección de hipervínculos)](address-cell-hyperlinks-section.md) <br/> |
|Predeterminado  <br/> |Determina el hipervínculo predeterminado de una forma o página.  <br/> |[Celda Default (Sección de hipervínculos)](default-cell-hyperlinks-section.md) <br/> |
|Description  <br/> |Representa una cadena de texto descriptivo para un hipervínculo.  <br/> |[Celda Description (Sección de hipervínculos)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Representa una cadena que pasa información que se utiliza en una dirección URL, como las coordenadas de un mapa de imagen.  <br/> |[Celda ExtraInfo (Sección de hipervínculos)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |Representa el nombre de un marco de destino cuando la aplicación se abre como documento Active en una aplicación contenedora. El valor predeterminado es una cadena vacía.  <br/> |[Celda Frame (Sección de hipervínculos)](frame-cell-hyperlinks-section.md) <br/> |
|Invisible  <br/> |Indica si un hipervínculo aparece o no en el menú contextual de una forma o página.  <br/> |[Celda Invisible (Sección de hipervínculos)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Especifica si el hipervínculo se abre en una ventana nueva.  <br/> |[Celda NewWindow (Sección de hipervínculos)](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Un número que determina el orden de los hipervínculos que aparecen en un menú contextual.  <br/> |[Celda SortKey (Sección de hipervínculos)](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |Especifica una ubicación del documento de destino con la que se establece el vínculo.  <br/> |[Celda SubAddress (Sección de hipervínculos)](subaddress-cell-hyperlinks-section.md) <br/> |
   

