---
title: Elemento Cell (sección Field) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.
ms.openlocfilehash: b3bae89d20a4defed591e95ce0155f70d806e6f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540059"
---
# <a name="cell-element-field-section-visio-xml"></a>Elemento Cell (sección Field) (Visio XML)

Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (sección Field)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que la fórmula se evalúa como un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las cadenas siguientes:  <br/>  '(alguna fórmula)' si la fórmula existe localmente  <br/>  `No Formula` si la fórmula se elimina o bloquea localmente  <br/>  `Inh` si la fórmula se hereda.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa una unidad de medida El valor predeterminado es DL.  <br/> |Las unidades de la celda.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |Valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a celdas ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** permitidos para este **elemento Cell.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Calendar  <br/> |Determina el calendario que se usa para un campo de texto cuando el tipo de datos es Date.  <br/> |[Celda Calendar (Sección de campos de texto)](calendar-cell-text-fields-section.md) <br/> |
|Formato  <br/> |Especifica el formato del campo de texto como una cadena, un número, una fecha u hora, una duración o una moneda.  <br/> |[Celda Format (Sección de campos de texto)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Indica el tipo de campo de texto.  <br/> |[Celda ObjectKind (Sección de campos de texto)](objectkind-cell-text-fields-section.md) <br/> |
|Tipo  <br/> |Especifica un tipo de datos para el valor del campo de texto.  <br/> |[Celda Type (Sección de campos de texto)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Determina la categoría de un campo insertado. Los cuadros de diálogo Campo y Formato de datos usan esta celda para determinar la información de campo y categoría.  <br/> |[Celda UICategory (Sección de campos de texto)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Determina el código de un campo insertado. Los cuadros de diálogo Campo y Formato de datos usan esta celda para determinar la información de campo y categoría.  <br/> |[Celda UICode (Sección de campos de texto)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Determina el formato de un campo insertado. Los cuadros de diálogo Campo y Formato de datos usan esta celda para determinar el campo y  <br/> |[Celda UIFormat (Sección de campos de texto)](uiformat-cell-text-fields-section.md) <br/> |
|Valor  <br/> |Contiene la función de un campo.  <br/> |[Celda Value (Sección de campos de texto)](value-cell-text-fields-section.md) <br/> |
   

