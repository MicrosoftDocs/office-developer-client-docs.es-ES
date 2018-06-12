---
title: Elemento PageSheet (Page_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica las propiedades de la página de dibujo asociada con la página de dibujo.
ms.openlocfilehash: ef926af0238b1a44bbaa5c2eae9c0f7c90dc0c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822722"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a>Elemento PageSheet (Page_Type complexType) ('XML de Visio')

Especifica las propiedades de la página de dibujo asociada con la página de dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Pages.Xml  <br/> |
   
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
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen una página del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos desde la que se heredan de formato de relleno. DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos desde la que se heredan de formato de línea. DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos desde la que se heredan de formato de texto. DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo XSD: String.  <br/> |
   

