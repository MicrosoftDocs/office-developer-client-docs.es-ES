---
title: Elemento Text (ShapeSheet_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contiene el texto de una forma.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332374"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a>Elemento Text (ShapeSheet_Type complexType) ("XML" de Visio)

Contiene el texto de una forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Página #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen una forma en un elemento de forma de grupo, **página**o **patrón**.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[cruzada](cp-element-text_type-complextypevisio-xml.md) <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |Marca el principio de una ejecución de propiedades de carácter que tiene un formato conforme al elemento char correspondiente.  <br/> |
|[FLD](fld-element-text_type-complextypevisio-xml.md) <br/> |[fld_Type](fld_type-complextypevisio-xml.md) <br/> |Indica un punto de inserción de campo de texto para el elemento Field correspondiente.  <br/> |
|[VP](pp-element-text_type-complextypevisio-xml.md) <br/> |[pp_Type](pp_type-complextypevisio-xml.md) <br/> |Especifica el principio de un párrafo ejecutar propiedades.  <br/> |
|[PAM](tp-element-text_type-complextypevisio-xml.md) <br/> |[tp_Type](tp_type-complextypevisio-xml.md) <br/> |Especifica el principio de una ejecución de propiedades de tabulaciones.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

