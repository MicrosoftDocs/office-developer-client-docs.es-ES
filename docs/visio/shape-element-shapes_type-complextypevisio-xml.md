---
title: Elemento Shape (complexType Shapes_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contiene elementos que definen una forma en un elemento de forma de grupo, página o patrón.
ms.openlocfilehash: aa7ffa539c9f82adc486bd0848dda66798bac165
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542075"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Elemento Shape (complexType Shapes_Type) (XML de Visio)

Contiene elementos que definen una forma en un elemento de forma de grupo, **página**o **patrón**.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Página #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica una colección de formas.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica una colección de formas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad única.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contiene un valor de cadena arbitrario que se usa para proporcionar información adicional acerca de una forma.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contiene un valor de cadena arbitrario que se usa para proporcionar información adicional acerca de una forma.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contiene un valor de cadena arbitrario que se usa para proporcionar información adicional acerca de una forma.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contiene un BLOB codificado de MIME (Extensiones multipropósito de correo Internet) de datos de imagen, como metarchivo de Windows, mapa de bits o datos OLE.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades relacionadas.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica una colección de formas.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contiene el texto de una forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Marca que indica si el elemento se elimina de forma local.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|FillStyle  <br/> |xsd: unsignedInt  <br/> ||IDENTIFICADOR de la hoja de estilos de la que esta forma hereda el formato de relleno.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Indica si el usuario ha personalizado el nombre.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Indica si el usuario ha personalizado el nombre universal..  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|LineStyle  <br/> |xsd: unsignedInt  <br/> ||IDENTIFICADOR de la hoja de estilos de la que esta forma hereda el formato de línea.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Master  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |IDENTIFICADOR del elemento Master desde el que la forma hereda sus datos.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|MasterShape  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |IDENTIFICADOR del elemento Master desde el que la forma hereda sus datos.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre universal del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|TextStyle  <br/> |xsd: unsignedInt  <br/> ||IDENTIFICADOR de la hoja de estilos desde la que esta forma hereda el formato del texto.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Tipo  <br/> |xsd: token  <br/> |opcional  <br/> |El tipo de una forma. Puede ser uno de los siguientes valores: Group, Shape, Guide o Foreign.  <br/> |Valores del tipo xsd: token.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |GUID (identificador único global) asignado a la forma.  <br/> |Valores del tipo xsd: String.  <br/> |
   

