---
title: Elemento de celda (fila Hyperlink) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.
ms.openlocfilehash: b664f5e0ac7cfe27b7198dd59b1b8be1af276db7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821715"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Elemento de celda (fila Hyperlink) ('XML de Visio')

Contiene la información de un único hipervínculo asociado a una forma. Una forma contendrá una fila **Hyperlink** por cada hipervínculo. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Elemento Row (sección Hipervínculo)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Contiene la información de un único hipervínculo asociado a una forma. Una forma contendrá una fila **Hyperlink** por cada hipervínculo.  <br/> |
   
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
|Address  <br/> |Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.  <br/> |[Celda Address (Sección de hipervínculos)](address-cell-hyperlinks-section.md) <br/> |
|Default  <br/> |Determina el hipervínculo predeterminado de una forma o página.  <br/> |[Celda Default (Sección de hipervínculos)](default-cell-hyperlinks-section.md) <br/> |
|Descripción  <br/> |Representa una cadena de texto descriptivo para un hipervínculo.  <br/> |[Celda Description (Sección de hipervínculos)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Representa una cadena que pasa información que se usará en la resolución de una dirección URL, como las coordenadas de un mapa de imagen.  <br/> |[Celda ExtraInfo (Sección de hipervínculos)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |Representa el nombre de un marco de destino cuando la aplicación se abre como documento Active en una aplicación contenedora. El valor predeterminado es una cadena vacía.  <br/> |[Celda Frame (Sección de hipervínculos)](frame-cell-hyperlinks-section.md) <br/> |
|Invisible  <br/> |Indica si un hipervínculo aparece o no en el menú contextual de una forma o página.  <br/> |[Celda Invisible (Sección de hipervínculos)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Especifica si el hipervínculo se abre en una ventana nueva.  <br/> |[Celda NewWindow (Sección de hipervínculos)](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Un número que determina el orden de los hipervínculos que aparecen en un menú contextual.  <br/> |[Celda SortKey (Sección de hipervínculos)](sortkey-cell-hyperlinks-section.md) <br/> |
|Subdirección  <br/> |Especifica una ubicación del documento de destino con la que se establece el vínculo.  <br/> |[Celda SubAddress (Sección de hipervínculos)](subaddress-cell-hyperlinks-section.md) <br/> |
   

