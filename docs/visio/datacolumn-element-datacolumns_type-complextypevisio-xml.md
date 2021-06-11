---
title: Elemento DataColumn (DataColumns_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Define cómo aparece una columna de datos en la ventana Datos externos de la interfaz de usuario de Visio y clasifica los datos de la columna definiendo su tipo de datos y su formato.
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541228"
---
# <a name="datacolumn-element-datacolumns_type-complextype-visio-xml"></a>Elemento DataColumn (DataColumns_Type complexType) (Visio XML)

Define cómo aparece una  columna de datos en la ventana Datos externos de la interfaz de usuario de Visio y clasifica los datos de la columna definiendo su tipo de datos y formato. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contiene todos los **elementos DataColumn** de un conjunto de registros de datos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Calendar  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Identificador de calendario de la columna de datos.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |necesario  <br/> |Nombre externo de la columna de datos. Aparece en los encabezados de la ventana **Datos** externos y en las etiquetas de los gráficos de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|Moneda  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Identificador de moneda de la columna de datos.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Tipo de datos en la columna de datos.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el grado (potencia) de las unidades, por ejemplo al cuadrado o al cubo. El valor predeterminado (atributo ausente) es 1.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Define la posición para mostrar  de la columna de datos en la ventana Datos externos, desde la columna más izquierda (0) hasta la columna más a la derecha (valor más grande).  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Ancho de la columna de datos en la **ventana Datos** externos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |opcional  <br/> |Si la columna de datos crea un hipervínculo en una forma cuando la forma está vinculada a datos.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|Etiqueta  <br/> |xsd:string  <br/> |necesario  <br/> |Etiqueta de la columna de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador de idioma de la columna de datos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Asignado  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica si la columna está visible en la **ventana Datos** externos. True (1) para que la columna esté visible; False (0) para que la columna no esté visible. El valor predeterminado (atributo ausente) es que la columna esté visible.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|Nombre  <br/> |xsd:string  <br/> |necesario  <br/> |Nombre interno de la columna de datos. Se usa como el nombre de fila del elemento shape-data (propiedad personalizada) agregado a una forma cuando la forma está vinculada a una fila de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |opcional  <br/> |Etiqueta de columna devuelta a Visio por la interfaz de ADO subyacente.  <br/> |Valores del tipo xsd:string.  <br/> |
|UnitType  <br/> |xsd:string  <br/> |opcional  <br/> |Tipo de unidad de los datos de la columna de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
   

