---
title: Elemento PageSheet (Master_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Especifica las propiedades de la página de dibujo asociadas con el patrón.
ms.openlocfilehash: ab20cfe4561cd5fd0eeb6edad0b3a608428b0e8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822762"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>Elemento PageSheet (Master_Type complexType) ('XML de Visio')

Especifica las propiedades de la página de dibujo asociadas con el patrón.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Masters.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Especifica a un patrón en un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos desde la que se heredan de formato de relleno. DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos desde la que se heredan de formato de línea. DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos desde la que se heredan de formato de texto. DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo XSD: String.  <br/> |
   

