---
title: Elemento PageSheet (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Especifica las propiedades de la página de dibujo asociada al patrón.
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540619"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a>Elemento PageSheet (Master_Type complexType) (Visio XML)

Especifica las propiedades de la página de dibujo asociada al patrón.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |masters.xml  <br/> |
   
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
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Especifica un patrón en un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |especifica el identificador de la hoja de estilos desde la que se va a heredar el formato de relleno. Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de línea. Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de texto. Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> |El identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:string.  <br/> |
   

