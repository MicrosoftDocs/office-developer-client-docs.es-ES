---
title: Elemento HeaderFooterFont (complexType HeaderFooter_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Especifica la fuente utilizada para el texto del encabezado y del pie de página.
ms.openlocfilehash: b87ba96d551bf943dd330aa428f2c943c9d29269
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541088"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>Elemento HeaderFooterFont (complexType HeaderFooter_Type) (XML de Visio)

Especifica la fuente utilizada para el texto del encabezado y del pie de página.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contiene los elementos del encabezado y pie de página de un documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica el juego de caracteres de la fuente. Equivalente al campo LOGFONTlfCharSet de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica la precisión de recorte de la fuente. Equivalente al campo LOGFONTlfClipPrecision de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|Escape  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica el atributo de escape de la fuente. Equivalente al campo LOGFONTlfEscapement de GDI.  <br/> |Valores del tipo xsd: int.  <br/> |
|FaceName  <br/> |xsd: String  <br/> |opcional  <br/> |Contiene información acerca de una fuente.  <br/> |Valores del tipo xsd: String.  <br/> |
|Height  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica el alto de la forma en las unidades de dibujo.  <br/> |Valores del tipo xsd: int.  <br/> |
|Italic  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica si la fuente está en cursiva. Equivalente al campo LOGFONTlfItalic de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|Orientation  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica la orientación de la fuente. Equivalente al campo LOGFONTlfOrientation de GDI.  <br/> |Valores del tipo xsd: int.  <br/> |
|Deprecision  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica el atributo de precisión de salida de la fuente. Equivalente al campo LOGFONTlfOutPrecision de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica el tono y la familia de la fuente. Equivalente al campo LOGFONTlfPitchAndFamily de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|Quality  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica la calidad de salida de la fuente. Equivalente al campo LOGFONTlfQuality de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|Tacha  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica si la fuente es de tachado. Equivalente al campo LOGFONTlfStrikeOut de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|Underline  <br/> |xsd: unsignedByte  <br/> |opcional  <br/> |Especifica si la fuente está subrayada. Equivalente al campo LOGFONTlfUnderline de GDI.  <br/> |Valores del tipo xsd: unsignedByte.  <br/> |
|Peso  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica el peso de la fuente. Equivalente al campo LOGFONTlfWeight de GDI.  <br/> |Valores del tipo xsd: int.  <br/> |
|Width  <br/> |xsd: int  <br/> |opcional  <br/> |Contiene el ancho de la forma asociada en las unidades de dibujo.  <br/> |Valores del tipo xsd: int.  <br/> |
   

