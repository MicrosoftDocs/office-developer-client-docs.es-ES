---
title: Elemento Trigger (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre las partes de documento de un archivo de Visio.
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542908"
---
# <a name="trigger-element-visio-xml"></a>Elemento Trigger (XML de Visio)

Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre las partes de documento de un archivo de Visio.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica los elementos de celda que proporcionan información para la definición de una forma.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Define la estructura DocumentSheet.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Representa un estilo definido en un documento.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociada al patrón.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de la página de dibujo asociada a la página de dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una página de referencia de Toa en el dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Nombre de la fórmula a la que se llamará cuando se active el desencadenador.  <br/> Vea la sección Comentarios.  <br/> |Valores del tipo xsd: String.  <br/> |
   
## <a name="remarks"></a>Observaciones

El atributo **N** de este elemento **Trigger** debe ser uno de un conjunto limitado de valores que corresponden a las instrucciones desencadenadoras. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento **Trigger** . 
  
|**Value**|**Elemento primario**|**Descripción**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función **HASCATEGORIES** .  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Un desencadenador que aparece en una página cuando existe una referencia entre partes mediante una función **BKGPAGENAME**  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cada vez que la página o cualquiera de las formas contenidas utiliza una función **RGB** .  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia cruzada de una parte mediante una función **DOCCREATION** .  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte con una función **data1** .  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función **DATA2** .  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función **DATA3** .  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia cruzada de una parte mediante una función **DOCLASTEDIT** .  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función **ID** .  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función **MASTERNAME** .  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Un desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte con una función **Name** .  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página si la página o cualquiera de las formas que lo contienen tienen una función **ahora** o **Rand** .  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Un desencadenador que aparece en un documento cuando existe una referencia cruzada de una parte mediante una función **PAGECOUNT** .  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia entre partes mediante una función **pagename** .  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cuando existe una referencia cruzada de una parte mediante una función **PageNumber** .  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Un desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función **POINTALONGPATH**, **PATHLENGTH**o **PATHSEGMENT** .  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia cruzada de una parte mediante una función **DOCLASTPRINT** .  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia cruzada de una parte mediante una función **DOCLASTSAVE** .  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en un documento cuando existe una referencia cruzada que usa una **** función Category, **Creator**, **** Description, Keywords, Subject o **title** . **** ****  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función de **tipo** .  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una forma cuando existe una referencia cruzada de una parte mediante una función **CONTAINERMEMBERCOUNT** .  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cuando existe una referencia entre partes mediante una función **CONTAINERSHEETREF** .  <br/> |
|Ruta de acceso  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Desencadenador que aparece en una página cuando existe una referencia cruzada de una parte mediante una función **POINTALONGPATH**, **PATHLENGTH**o **PATHSEGMENT** .  <br/> |
   

