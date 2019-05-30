---
title: Elemento Row (sección de caracteres) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 764a8e77-5308-e6ce-8763-dc6e6090da9d
description: Muestra los atributos de formato de un segmento de texto de la forma, como la fuente, el color, el estilo de texto, el caso, la posición con respecto a la línea base y el tamaño en puntos.
ms.openlocfilehash: afff4dcb809bf73da6ada25045678711ade75b6b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541788"
---
# <a name="row-element-character-section-visio-xml"></a>Elemento Row (sección de caracteres) (XML de Visio)

Muestra los atributos de formato de un segmento de texto de la forma, como la fuente, el color, el estilo de texto, el caso, la posición con respecto a la línea base y el tamaño en puntos.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML, Master #. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="CharacterRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Muestra los atributos de formato de un segmento de texto de la forma, como la fuente, el color, el estilo de texto, el caso, la posición con respecto a la línea base y el tamaño en puntos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad única.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IX  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de base uno de la fila. Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs. Una fila sólo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único dependiente del idioma de la fila.  <br/> |Valores del tipo xsd: String.  <br/> |
|N  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag. Una fila sólo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd: String.  <br/> |
|T  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría. El atributo T solo se usa para la sección Geometry.  <br/> |Valores del tipo xsd: String.  <br/> |
   

