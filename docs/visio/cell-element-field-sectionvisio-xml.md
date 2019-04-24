---
title: Elemento cell (sección campo) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.
ms.openlocfilehash: f6c3c724b210ad579012ff58b93333e28c2a8cf1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356241"
---
# <a name="cell-element-field-section-visio-xml"></a>Elemento cell (sección campo) ("XML" de Visio)

Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (sección campo)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |opcional  <br/> |Indica que la fórmula da como resultado un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd: String  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las siguientes cadenas:  <br/>  ' (alguna fórmula) ' si la fórmula existe localmente  <br/>  `No Formula`Si la fórmula se ha eliminado o bloqueado localmente  <br/>  `Inh`Si la fórmula es heredada.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd: String  <br/> |opcional  <br/> |Representa una unidad de medida el valor predeterminado es DL.  <br/> |Unidades de la celda.  <br/> |
|V  <br/> |xsd: String  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |El valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento de **celda** . 
  
|**Value**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|Calendar  <br/> |Determina el calendario que se usa para un campo de texto cuando el tipo de datos es fecha.  <br/> |[Celda Calendar (Sección de campos de texto)](calendar-cell-text-fields-section.md) <br/> |
|Formato  <br/> |Especifica el formato del campo de texto como una cadena, un número, una fecha u hora, una duración o una moneda.  <br/> |[Celda Format (Sección de campos de texto)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Indica el tipo de campo de texto.  <br/> |[Celda ObjectKind (Sección de campos de texto)](objectkind-cell-text-fields-section.md) <br/> |
|Tipo  <br/> |Especifica un tipo de datos para el valor del campo de texto.  <br/> |[Celda Type (Sección de campos de texto)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Determina la categoría de un campo insertado. Esta celda se utiliza en los cuadros de diálogo formato de campo y datos para determinar la información del campo y de la categoría.  <br/> |[Celda UICategory (Sección de campos de texto)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Determina el código de un campo insertado. Esta celda se utiliza en los cuadros de diálogo formato de campo y datos para determinar la información del campo y de la categoría.  <br/> |[Celda UICode (Sección de campos de texto)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Determina el formato de un campo insertado. Esta celda se utiliza en los cuadros de diálogo formato de campo y datos para determinar el campo y  <br/> |[Celda UIFormat (Sección de campos de texto)](uiformat-cell-text-fields-section.md) <br/> |
|Valor  <br/> |Contiene la función de un campo.  <br/> |[Celda Value (Sección de campos de texto)](value-cell-text-fields-section.md) <br/> |
   

