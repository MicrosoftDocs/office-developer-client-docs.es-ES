---
title: Elemento DataColumn (DataColumns_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Define cómo aparece una columna de datos en la ventana datos externos de la interfaz de usuario de Visio y califica los datos de la columna mediante la definición de su formato y tipo de datos.
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541228"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>Elemento DataColumn (DataColumns_Type complexType) (XML de Visio)

Define cómo aparece una columna de datos en la ventana **datos externos** de la interfaz de usuario de Visio y califica los datos de la columna mediante la definición de su formato y tipo de datos. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos **DataColumn** de un conjunto de registros de datos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Calendario  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |IDENTIFICADOR de calendario de la columna de datos.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd: String  <br/> |necesario  <br/> |Nombre externo de la columna de datos. Aparece en los encabezados de la ventana **datos externos** y en etiquetas en los gráficos de datos.  <br/> |Valores del tipo xsd: String.  <br/> |
|Moneda  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |IDENTIFICADOR de moneda de la columna de datos.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|DataType  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |Tipo de datos de la columna de datos.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|Degree  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el grado (la potencia) de las unidades, por ejemplo, cuadradas o con cubos. El valor predeterminado (atributo ausente) es 1.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Define la posición de presentación de la columna de datos en la ventana **datos externos** , desde la columna situada más a la izquierda (0) hasta la columna situada más a la derecha (valor mayor).  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Ancho de la columna de datos en la ventana **datos externos** .  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Hipervínculo  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Si la columna de datos crea un hipervínculo en una forma cuando la forma está vinculada a datos.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|Label  <br/> |xsd: String  <br/> |necesario  <br/> |Etiqueta de la columna de datos.  <br/> |Valores del tipo xsd: String.  <br/> |
|Idioma  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |IDENTIFICADOR de idioma de la columna de datos.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Asignación  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si la columna es visible en la ventana **datos externos** . True (1) para que la columna sea visible; False (0) para que la columna no sea visible. El valor predeterminado (atributo ausente) es para que la columna sea visible.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |necesario  <br/> |Nombre interno de la columna de datos. Se usa como el nombre de fila para el elemento de datos de formas (propiedad personalizada) agregado a una forma cuando la forma está vinculada a una fila de datos.  <br/> |Valores del tipo xsd: String.  <br/> |
|OrigLabel  <br/> |xsd: String  <br/> |opcional  <br/> |La etiqueta de columna se devuelve a Visio mediante la interfaz ADO subyacente.  <br/> |Valores del tipo xsd: String.  <br/> |
|UnitType  <br/> |xsd: String  <br/> |opcional  <br/> |Tipo de unidad de los datos de la columna de datos.  <br/> |Valores del tipo xsd: String.  <br/> |
   

