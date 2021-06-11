---
title: Elemento Trigger (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Proporciona instrucciones a Microsoft Visio para volver a calcular una relación entre elementos de documento en un Visio archivo.
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542908"
---
# <a name="trigger-element-visio-xml"></a>Elemento Trigger (Visio XML)

Proporciona instrucciones a Microsoft Visio para volver a calcular una relación entre elementos de documento en un Visio archivo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica elementos de celda que proporcionan información para la definición de una forma.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Define la estructura DocumentSheet.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Representa un estilo definido en un documento.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociada al patrón.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociada a la página de dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página en el dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd:string  <br/> |necesario  <br/> |Nombre de la fórmula a la que se llamará cuando se active el desencadenador.  <br/> Consulte la sección Comentarios.  <br/> |Valores del tipo xsd:string.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Trigger** debe ser uno de un conjunto limitado de valores que corresponden a instrucciones de desencadenador. Consulte la tabla siguiente para determinar los valores del atributo **N** permitidos para este **elemento Trigger.** 
  
|**Valor**|**Elemento primario**|**Descripción**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante una **función HASCATEGORIES.**  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cuando existe una referencia entre partes con una **función BKGPAGENAME**  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página siempre que la página o cualquiera de sus formas contenidas usa una **función RGB.**  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia entre partes mediante una **función DOCCREATION.**  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante **una función DATA1.**  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante **una función DATA2.**  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante **una función DATA3.**  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia entre partes mediante una **función DOCLASTEDIT.**  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante una **función ID.**  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante una **función MASTERNAME.**  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante una **función NAME.**  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página si la página o cualquiera de sus formas que lo contienen tienen una **función NOW** o **RAND.**  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia entre partes mediante una **función PAGECOUNT.**  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante una **función PAGENAME.**  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cuando existe una referencia entre partes mediante una **función PAGENUMBER.**  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante una **función POINTALONGPATH**, **PATHLENGTH** o **PATHSEGMENT.**  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia entre partes con una **función DOCLASTPRINT.**  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia entre partes con una **función DOCLASTSAVE.**  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia entre partes mediante una función **CATEGORY**, **CREATOR**, **DESCRIPTION**, **KEYWORDS**, **SUBJECT** o **TITLE.**  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante **una función TYPE.**  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante **una función CONTAINERMEMBERCOUNT.**  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cuando existe una referencia entre partes mediante **una función CONTAINERSHEETREF.**  <br/> |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cuando existe una referencia entre partes mediante una **función POINTALONGPATH**, **PATHLENGTH** o **PATHSEGMENT.**  <br/> |
   

