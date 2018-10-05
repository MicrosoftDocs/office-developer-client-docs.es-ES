---
title: Elemento ForeignData (ShapeSheet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contiene un BLOB codificado MIME (Extensiones multipropósito de correo Internet) de datos de imagen, como metarchivo de Windows, mapa de bits o de datos OLE.
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382684"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>Elemento ForeignData (ShapeSheet_Type complexType) ('XML de Visio')

Contiene un BLOB codificado MIME (Extensiones multipropósito de correo Internet) de datos de imagen, como metarchivo de Windows, mapa de bits o de datos OLE.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |página # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica una relación con un elemento que contiene los datos de imagen.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica el nivel de compresión aplicada al archivo. Este atributo sólo es significativa si los datos externa están un objeto externo en función de la trama, como un archivo DIB, JPG, PNG, TIFF o GIF.  <br/> |Valores del tipo XSD: Double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |opcional  <br/> |Especifica el tipo de compresión aplicada al archivo. Este atributo sólo es significativa si los datos externa están un objeto externo en función de la trama, como un archivo DIB, JPG, PNG, TIFF o GIF  <br/> |Valores del tipo xsd:token.  <br/> |
|ExtentX  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica la medida horizontal del metarchivo. Este atributo sólo es significativa si los datos externa están un metarchivo.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ExtentY  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica la extensión vertical del metarchivo. Este atributo sólo es significativa si los datos externa están un metarchivo.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |necesario  <br/> |Indica el tipo de metarchivo, EnhMetaFile, mapa de bits, el objeto o la entrada de lápiz.  <br/> |Valores del tipo xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica el modo de asignación de metarchivo. Este atributo sólo es significativa si los datos externa están un metarchivo.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica el alto del objeto en unidades de página. Este atributo sólo es significativa si los datos externa están un objeto incrustado OLE2.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Un indicador de número entero de tipo de objeto. Se usa cuando tipo externa es object.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica el ancho del objeto en unidades de página. Este atributo sólo es significativa si los datos externa están un objeto incrustado OLE2.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ShowAsIcon  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Indica si se debe mostrar o no mostrar datos incrustados como un icono.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
   

