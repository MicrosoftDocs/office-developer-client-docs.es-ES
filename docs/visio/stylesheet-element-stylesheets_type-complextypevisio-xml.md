---
title: Elemento de hoja de estilos (StyleSheets_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Representa un estilo definido en un documento.
ms.openlocfilehash: 2513c7421dc8f890b7ba63f19cf3d31d23ce65ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823348"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a>Elemento de hoja de estilos (StyleSheets_Type complexType) ('XML de Visio')

Representa un estilo definido en un documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Contiene una colección de elementos de la **hoja de estilos** para el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad única.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades relacionadas.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador del elemento de hoja de estilos desde la que hereda este estilo de formato de relleno.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Indica si el nombre se ha personalizado por el usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IsCustomNameU  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Indica si el nombre universal se ha personalizado por el usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador del elemento de hoja de estilos desde la que hereda este estilo de formato de línea.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre universal del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador del elemento de hoja de estilos desde la que hereda este estilo de formato de texto.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

