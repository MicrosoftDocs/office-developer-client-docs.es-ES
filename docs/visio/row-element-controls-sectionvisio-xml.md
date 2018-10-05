---
title: Elemento Row (sección de controles) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Contiene las celdas de un controlador definido para una forma.
ms.openlocfilehash: aa690bf70078a711dffca3f01b6e7acc05507bdd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386771"
---
# <a name="row-element-controls-section-visio-xml"></a>Elemento Row (sección de controles) ('XML de Visio')

Contiene las celdas de un controlador definido para una forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contiene las celdas de un controlador definido para una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene una propiedad para un controlador definido para una forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPR  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador basado en uno de la fila. Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas. Sólo una fila puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único de dependen del idioma de la fila.  <br/> |Valores del tipo XSD: String.  <br/> |
|N  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag. Sólo una fila puede tener uno de los atributos IX o N.  <br/> |Valores del tipo XSD: String.  <br/> |
|T  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría. El atributo T solo se usa para la sección de geometría.  <br/> |Valores del tipo XSD: String.  <br/> |
   

