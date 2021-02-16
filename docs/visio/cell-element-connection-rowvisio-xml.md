---
title: Elemento Cell (fila Connection) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contiene las coordenadas x o y, dirección horizontal o vertical, o el tipo de un único punto de conexión en una forma.
ms.openlocfilehash: 0c8177767d5c85d505ba8a2a430946fd29cf44aa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541879"
---
# <a name="cell-element-connection-row-visio-xml"></a>Elemento Cell (fila Connection) (XML de Visio)

Contiene las coordenadas x o y, dirección horizontal o vertical, o el tipo de un único punto de conexión en una forma.
  
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
|[Elemento Row (Sección de conexión)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x e y, la dirección horizontal y vertical, y el tipo de un punto de conexión de una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, la dirección horizontal y vertical, y el tipo de un único punto de conexión en una forma.  <br/> |
   
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
|AutoGen  <br/> |Especifica si el punto de conexión se genera automáticamente. Un valor de 1 indica que el punto de conexión se genera automáticamente.  <br/> |Ninguno.  <br/> |
|DirX  <br/> |Determina el componente x del vector de alineación necesario de un punto de conexión coincidente.  <br/> |[Celda DirX / A (Sección de puntos de conexión)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Determina el componente y del vector de alineación necesario de un punto de conexión coincidente.  <br/> |[Celda DirY / B (Sección de puntos de conexión)](diryb-cell-connection-points-section.md) <br/> |
|Prompt  <br/> |Este atributo se reserva para usarlo en el futuro.  <br/> |Ninguno.  <br/> |
|Tipo  <br/> |Determina el tipo de punto de conexión.  <br/> |[Celda Type / C (Sección de puntos de conexión)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Representa la coordenada x de un punto de conexión en coordenadas locales.  <br/> |[Celda X (Sección de puntos de conexión)](x-cell-connection-points-section.md) <br/> |
|v  <br/> |Determina la coordenada y de un punto de conexión en coordenadas locales.  <br/> |[Celda Y (Sección de puntos de conexión)](y-cell-connection-points-section.md) <br/> |
   

