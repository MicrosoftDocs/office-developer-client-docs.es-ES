---
title: Elemento de forma (Shapes_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contiene elementos que definen una forma en un patrón, una página o un elemento de la forma de grupo.
ms.openlocfilehash: 6308b8dd21c92f6ced9ea7f03ec8aa85773fa2bb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399686"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Elemento de forma (Shapes_Type complexType) ('XML de Visio')

Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |página # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica una colección de formas.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica una colección de formas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad única.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contiene un valor de cadena arbitraria que se usa para proporcionar información adicional sobre una forma.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contiene un valor de cadena arbitraria que se usa para proporcionar información adicional sobre una forma.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contiene un valor de cadena arbitraria que se usa para proporcionar información adicional sobre una forma.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contiene un BLOB codificado MIME (Extensiones multipropósito de correo Internet) de datos de imagen, como metarchivo de Windows, mapa de bits o de datos OLE.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades relacionadas.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica una colección de formas.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contiene el texto de una forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPR  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Una marca que indica si el elemento se ha eliminado localmente.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||El identificador de la hoja de estilos desde la que esta forma hereda el formato de relleno.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Indica si el nombre se ha personalizado por el usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IsCustomNameU  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Indica si el nombre universal se ha personalizado por el usuario..  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||El identificador de la hoja de estilos de la que esta forma hereda el formato de línea.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador del patrón elemento desde el que la forma hereda sus datos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador del patrón elemento desde el que la forma hereda sus datos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre universal del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||El identificador de la hoja de estilos de la que esta forma hereda el formato de texto.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Tipo  <br/> |xsd:token  <br/> |opcional  <br/> |El tipo de una forma. Puede ser uno de los siguientes valores: grupo, forma, guía o externo.  <br/> |Valores del tipo xsd:token.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |Un GUID (identificador único global) asignado a la forma.  <br/> |Valores del tipo XSD: String.  <br/> |
   

