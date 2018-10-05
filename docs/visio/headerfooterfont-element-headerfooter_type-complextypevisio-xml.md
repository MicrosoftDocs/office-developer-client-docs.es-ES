---
title: Elemento HeaderFooterFont (HeaderFooter_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Especifica la fuente utilizada para el texto de encabezado y pie de página.
ms.openlocfilehash: f14d973caddc77394881d1b1dfd62a43f10cd7bb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385973"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>Elemento HeaderFooterFont (HeaderFooter_Type complexType) ('XML de Visio')

Especifica la fuente utilizada para el texto de encabezado y pie de página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contiene elementos de encabezado y pie de página de un documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Juego de caracteres  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica el juego de caracteres de la fuente. Equivale al campo LOGFONTlfCharSet de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica la precisión de recorte de la fuente. Equivale al campo LOGFONTlfClipPrecision de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|Escape  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica el atributo de escape de la fuente. Equivale al campo LOGFONTlfEscapement de GDI.  <br/> |Valores del tipo XSD: int.  <br/> |
|Nombre de fuente  <br/> |xsd: String  <br/> |opcional  <br/> |Contiene información acerca de una fuente.  <br/> |Valores del tipo XSD: String.  <br/> |
|Alto  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica el alto de la forma en unidades de dibujo.  <br/> |Valores del tipo XSD: int.  <br/> |
|Cursiva  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica si la fuente está en cursiva. Equivale al campo LOGFONTlfItalic de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|Orientation  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica la orientación de la fuente. Equivale al campo LOGFONTlfOrientation de GDI.  <br/> |Valores del tipo XSD: int.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica el atributo de precisión de salida de la fuente. Equivale al campo LOGFONTlfOutPrecision de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica la inclinación y la familia de la fuente. Equivale al campo LOGFONTlfPitchAndFamily de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|Calidad  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica la calidad de salida de la fuente. Equivale al campo LOGFONTlfQuality de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|Tachado  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica si la fuente es una fuente de tachado. Equivale al campo LOGFONTlfStrikeOut de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|Subrayado  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica si la fuente está subrayada. Equivale al campo LOGFONTlfUnderline de GDI.  <br/> |Valores del tipo xsd:unsignedByte.  <br/> |
|Grosor  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica el grosor de la fuente. Equivale al campo LOGFONTlfWeight de GDI.  <br/> |Valores del tipo XSD: int.  <br/> |
|Ancho  <br/> |xsd: int  <br/> |opcional  <br/> |Contiene el ancho de la forma asociada en unidades de dibujo.  <br/> |Valores del tipo XSD: int.  <br/> |
   

