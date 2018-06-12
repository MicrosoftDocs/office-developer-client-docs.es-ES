---
title: Elemento DataColumn (DataColumns_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Define cómo aparece una columna de datos en la ventana datos externos en la interfaz de usuario de Visio y califica los datos en la columna mediante la definición de su tipo de datos y el formato.
ms.openlocfilehash: f74061b9f3b8f4b93d8aa0e97e4e7c1e45131cbd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821934"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>Elemento DataColumn (DataColumns_Type complexType) ('XML de Visio')

Define cómo aparece una columna de datos en la ventana **Datos externos** en la interfaz de usuario de Visio y califica los datos en la columna mediante la definición de su tipo de datos y el formato. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos de **DataColumn** de un conjunto de registros de datos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Calendar  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Identificador de calendario de la columna de datos.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd: String  <br/> |necesario  <br/> |Nombre externo de la columna de datos. Aparece en los encabezados en la ventana **Datos externos** y en las etiquetas de gráficos de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|Moneda  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |ID de moneda de la columna de datos.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|Tipo de datos  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Tipo de los datos de la columna de datos.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|Grado  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el grado (power) de las unidades, por ejemplo cuadrado o al cubo. El valor predeterminado (atributo absent) es 1.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|OrdenVisualización  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Define la posición de presentación de la columna de datos en la ventana **Datos externos** , en la columna más a la izquierda (0) para la columna del extremo derecho (valor más alto).  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Ancho de la columna de datos en la ventana **Datos externos** .  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Hipervínculo  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Si la columna de datos crea un hipervínculo en una forma cuando la forma está vinculada a los datos.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|Etiqueta  <br/> |xsd: String  <br/> |necesario  <br/> |Etiqueta de la columna de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador de idioma de la columna de datos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Asignadas  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si la columna está visible en la ventana **Datos externos** . True (1) para la columna esté visible; False (0) de la columna que no esté visible. Es el valor predeterminado (atributo absent) para que la columna esté visible.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |necesario  <br/> |Nombre interno de la columna de datos. Se utiliza como el nombre de la fila para el elemento de datos de formas (propiedad personalizada) se agregó a una forma cuando la forma está vinculada a una fila de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|OrigLabel  <br/> |xsd: String  <br/> |opcional  <br/> |Etiqueta de columna devuelto a Visio por la interfaz de ADO subyacente.  <br/> |Valores del tipo XSD: String.  <br/> |
|UnitType  <br/> |xsd: String  <br/> |opcional  <br/> |Tipo de unidad de los datos de la columna de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
   

