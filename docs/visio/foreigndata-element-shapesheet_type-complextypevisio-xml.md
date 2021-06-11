---
title: Elemento ForeignData (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contiene un BLOB codificado mime (extensiones multipropósito de correo de Internet) de datos de imagen, como Windows metarchivo, mapa de bits o datos OLE.
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539845"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>Elemento ForeignData (ShapeSheet_Type complexType) (Visio XML)

Contiene un BLOB codificado mime (extensiones multipropósito de correo de Internet) de datos de imagen, como Windows metarchivo, mapa de bits o datos OLE.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen una forma en un **elemento Master**, **Page** o forma de grupo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica una relación con una parte que contiene los datos de la imagen.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica el nivel de compresión aplicado al archivo. Este atributo solo es significativo si los datos externos son un objeto externo basado en trama, como un archivo DIB, JPG, PNG, TIFF o GIF.  <br/> |Valores del tipo xsd:double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |opcional  <br/> |Especifica el tipo de compresión aplicada al archivo. Este atributo solo es significativo si los datos externos son un objeto externo basado en trama, como un archivo DIB, JPG, PNG, TIFF o GIF  <br/> |Valores del tipo xsd:token.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica la extensión horizontal del metarchivo. Este atributo solo es significativo si los datos externos son un metarchivo.  <br/> |Valores del tipo xsd:double.  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica la extensión vertical del metarchivo. Este atributo solo es significativo si los datos externos son un metarchivo.  <br/> |Valores del tipo xsd:double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |necesario  <br/> |Indica el tipo de metarchivo, EnhMetaFile, Bitmap, Object o Ink.  <br/> |Valores del tipo xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica el modo de asignación de metarchivo. Este atributo solo es significativo si los datos externos son un metarchivo.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica el alto del objeto en las unidades de página. Este atributo solo es significativo si los datos externos son un objeto incrustado OLE2.  <br/> |Valores del tipo xsd:double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Un indicador entero del tipo de objeto. Se usa cuando tipo externo es objeto.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica el ancho del objeto en las unidades de página. Este atributo solo es significativo si los datos externos son un objeto incrustado OLE2.  <br/> |Valores del tipo xsd:double.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica si se muestran o no los datos incrustados como un icono.  <br/> |Valores del tipo xsd:boolean.  <br/> |
   

