---
title: Elemento de celda (fila de controles) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Contiene una propiedad para un controlador definido para una forma.
ms.openlocfilehash: ff9bd2111b0f5a6544638fb7b33a1a9b797ede7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821717"
---
# <a name="cell-element-controls-row-visio-xml"></a>Elemento de celda (fila de controles) ('XML de Visio')

Contiene una propiedad para un controlador definido para una forma.
  
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
|[Elemento Row (sección Controles)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Contiene una propiedad para un controlador definido para una forma.  <br/> |
   
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
|CanGlue  <br/> |Determina si un controlador puede pegarse a otras formas.  <br/> |[Celda Can Glue (Sección de controles)](can-glue-cell-controls-section.md) <br/> |
|Prompt  <br/> |Representa una cadena de texto descriptivo que aparece como información de herramientas cuando el usuario deja el puntero sobre el controlador de una forma.  <br/> |[Celda Tip (Sección de controles)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Representa la coordenada x que indica la ubicación del controlador de una forma, en coordenadas locales.  <br/> |[Celda X (Sección de controles)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Especifica el tipo de comportamiento de la coordenada x del controlador presenta después de mover el controlador.  <br/> |Ninguno.  <br/> |
|xDyn  <br/> |Representa la coordenada x de un punto de anclaje del controlador en coordenadas locales.  <br/> |[Celda X Dynamics (Sección de controles)](x-dynamics-cell-controls-section.md) <br/> |
|v  <br/> |Representa la coordenada y que indica la ubicación del controlador de una forma, en coordenadas locales.  <br/> |[Celda Y (Sección de controles)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Especifica el tipo de comportamiento de que la coordenada y del controlador cuando éste se mueve.  <br/> |Ninguno.  <br/> |
|YDyn  <br/> |Representa la coordenada y de un punto de anclaje del controlador en coordenadas locales.  <br/> |[Celda Y Dynamics (Sección de controles)](y-dynamics-cell-controls-section.md) <br/> |
   

