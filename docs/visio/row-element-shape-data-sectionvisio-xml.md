---
title: Elemento Row (sección de datos de formas) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Especifica una entrada de datos de formas para asociar datos con una forma.
ms.openlocfilehash: 19dc4fe4759e7546f56160e41100d73721f9f6e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823048"
---
# <a name="row-element-shape-data-section-visio-xml"></a>Elemento Row (sección de datos de formas) ('XML de Visio')

Especifica una entrada de datos de formas para asociar datos con una forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Forma Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica una entrada de datos de formas para asociar datos con una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de los datos de formas.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPR  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador basado en uno de la fila. Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas. Sólo una fila puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único de dependen del idioma de la fila.  <br/> |Valores del tipo XSD: String.  <br/> |
|N  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag. Sólo una fila puede tener uno de los atributos IX o N.  <br/> |Valores del tipo XSD: String.  <br/> |
|T  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría. El atributo T solo se usa para la sección de geometría.  <br/> |Valores del tipo XSD: String.  <br/> |
   

