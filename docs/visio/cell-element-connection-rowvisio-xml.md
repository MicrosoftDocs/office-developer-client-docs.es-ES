---
title: Elemento de celda (fila de conexión) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contiene las coordenadas x o y, dirección horizontal o vertical o tipo para un único punto de conexión en una forma.
ms.openlocfilehash: 52328e50b185a96ebb06634248b93a4332ac35c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821705"
---
# <a name="cell-element-connection-row-visio-xml"></a>Elemento de celda (fila de conexión) ('XML de Visio')

Contiene las coordenadas x o y, dirección horizontal o vertical o tipo para un único punto de conexión en una forma.
  
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
|[Elemento Row (sección Conexión)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x e y, dirección horizontal y vertical y tipo para un único punto de conexión en una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, dirección horizontal y vertical y tipo para un único punto de conexión en una forma.  <br/> |
   
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
|AutoGen  <br/> |Especifica si el punto de conexión se genera automáticamente. Un valor de 1 indica que el punto de conexión se genera automáticamente.  <br/> |Ninguno.  <br/> |
|DirX  <br/> |Determina el componente x para el vector de alineación necesario de un punto de conexión coincidente.  <br/> |[Celda DirX / A (Sección de puntos de conexión)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Determina el componente y para el vector de alineación necesario de un punto de conexión coincidente.  <br/> |[Celda DirY / B (Sección de puntos de conexión)](diryb-cell-connection-points-section.md) <br/> |
|Prompt  <br/> |Este atributo está reservado para uso futuro.  <br/> |Ninguno.  <br/> |
|Tipo  <br/> |Determina el tipo de punto de conexión.  <br/> |[Celda Type / C (Sección de puntos de conexión)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Representa la coordenada x de un punto de conexión en coordenadas locales.  <br/> |[Celda X (Sección de puntos de conexión)](x-cell-connection-points-section.md) <br/> |
|v  <br/> |Determina la coordenada y de un punto de conexión en coordenadas locales.  <br/> |[Celda Y (Sección de puntos de conexión)](y-cell-connection-points-section.md) <br/> |
   

