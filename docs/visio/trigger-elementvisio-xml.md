---
title: Elemento Trigger ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre los elementos de documento en un archivo de Visio.
ms.openlocfilehash: a590ec1f9c19270f75d4d9e77804c0a7b45157b6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385441"
---
# <a name="trigger-element-visio-xml"></a>Elemento Trigger ('XML de Visio')

Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre los elementos de documento en un archivo de Visio.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica los elementos de celda que proporcionan información para la definición de una forma.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Define la estructura DocumentSheet.  <br/> |
|[Hoja de estilos](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Representa un estilo definido en un documento.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociadas con el patrón.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociada con la página de dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una página de referencia toa en el dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd: String  <br/> |necesario  <br/> |El nombre de la fórmula que se llama cuando se activa el desencadenador.  <br/> Vea la sección Comentarios.  <br/> |Valores del tipo XSD: String.  <br/> |
   
## <a name="remarks"></a>Comentarios

El atributo **N** de este elemento **Trigger** debe ser uno de un conjunto limitado de valores que corresponden a las instrucciones de desencadenador. Hacer referencia a la tabla siguiente para determinar los valores del atributo **N** permitidas para este elemento **Trigger** . 
  
|**Valor**|**Elemento primario**|**Descripción**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función **HASCATEGORIES** .  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una página cuando una referencia entre elementos mediante una **BKGPAGENAME** (función)  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Un desencadenador que aparece en una página cada vez que la página o cualquiera de sus formas contenidas usa una función **RGB** .  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en un documento cuando una referencia entre elementos mediante una función **DOCCREATION** .  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función de **DATA1** .  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función de **DATA2** .  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función de **DATA3** .  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en un documento cuando una referencia entre elementos mediante una **DOCLASTEDIT** (función).  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función de **identificador** .  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función **MASTERNAME** .  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función de **nombre** .  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Un desencadenador que aparece en una página si la página o cualquiera de sus formas que lo contiene tiene un **ahora** o una función **aleatorio** .  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en un documento cuando una referencia entre elementos mediante una función **PAGECOUNT** .  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función **PAGENAME** .  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una página cuando una referencia entre elementos mediante una función **PAGENUMBER** .  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función **POINTALONGPATH**, **PATHLENGTH**o **PATHSEGMENT** .  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en un documento cuando una referencia entre elementos mediante una función **DOCLASTPRINT** .  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en un documento cuando una referencia entre elementos mediante una función **DOCLASTSAVE** .  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en un documento cuando una referencia entre elementos mediante una función de **categoría**, **creador**, **Descripción**, **las palabras clave**, **asunto**o el **título** .  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos con una **tipo de** función.  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una forma cuando una referencia entre elementos mediante una función **CONTAINERMEMBERCOUNT** .  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una página cuando una referencia entre elementos mediante una función **CONTAINERSHEETREF** .  <br/> |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Existe un desencadenador que aparece en una página cuando una referencia entre elementos mediante una función **POINTALONGPATH**, **PATHLENGTH**o **PATHSEGMENT** .  <br/> |
   

