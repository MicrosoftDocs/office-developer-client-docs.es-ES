---
title: Elemento PageSheet (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica las propiedades de la página de dibujo asociada a la página de dibujo.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540626"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a>Elemento PageSheet (Page_Type complexType) (Visio XML)

Especifica las propiedades de la página de dibujo asociada a la página de dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen una página en el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos desde la que se heredará el formato de relleno. Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de línea. Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de texto. Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> |El identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:string.  <br/> |
   

