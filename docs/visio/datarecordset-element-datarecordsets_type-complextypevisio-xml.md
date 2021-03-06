---
title: Elemento DataRecordSet (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.
ms.openlocfilehash: e478593f370968db5fe9a65329cb1928c0f7c6ea
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539680"
---
# <a name="datarecordset-element-datarecordsets_type-complextype-visio-xml"></a>Elemento DataRecordSet (DataRecordSets_Type complexType) (Visio XML)

Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contiene todos los **elementos DataRecordset** del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contiene XML que se ajusta al esquema XML clásico de ADO para un conjunto de registros de ADO y que describe los datos del conjunto de registros de datos.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Define una regla que compara una columna del elemento **DataRecordset** primario con un elemento de datos de formas de la última acción de vinculación automática realizada correctamente en la interfaz de usuario.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Define cómo aparece una  columna de datos en la ventana Datos externos de la interfaz de usuario de Visio y clasifica los datos de la columna definiendo su tipo de datos y formato.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contiene todos los **elementos DataColumn** de un conjunto de registros de datos.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifica una o más columnas de clave principal en el conjunto de registros de datos.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indica una fila del conjunto de registros de datos vinculada a una forma que está en conflicto después de actualizar el conjunto de registros de datos.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Mapas una fila de conjunto de registros de datos a una forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Suma de comprobación  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Valor de suma de comprobación, generado por Visio y basado en propiedades del conjunto de registros de datos. Establezca este attirbute en 0; Visio actualiza este valor en tiempo de ejecución.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Comando  <br/> |xsd:string  <br/> |opcional  <br/> |Cadena de comandos usada para consultar datos desde el origen de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de conexión del objeto **DataConnection** asociado. No existe para orígenes de datos XML.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador del conjunto de registros de datos, único en el documento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Nombre  <br/> |xsd:string  <br/> |opcional  <br/> |Nombre para mostrar (o "descriptivo") del conjunto de registros de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El siguiente identificador Visio fila disponible.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Opciones  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Opciones que se aplican al conjunto de registros de datos. Los valores posibles pueden ser cualquier combinación de uno o varios de los que se muestran en la tabla siguiente.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |La frecuencia (en minutos) Visio actualiza automáticamente el conjunto de registros de datos. Este valor debe ser 1 o mayor.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |opcional  <br/> |Si la interfaz de usuario de conciliación de datos debe deshabilitarse. True (1) para deshabilitar la interfaz de usuario (UI). False (0) para habilitar la interfaz de usuario.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |opcional  <br/> |Si se sobrescribirán los cambios de usuario en elementos de datos de formas vinculadas a datos cuando se actualice el conjunto de registros de datos.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Define cómo se tratan los vínculos de datos de formas cuando se copian o cortan formas. 1 para reemplazar los vínculos existentes en la forma de destino. 0 para mantener vínculos existentes en la forma de destino.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |opcional  <br/> |Si se va a usar el orden de las filas del conjunto de registros de datos como clave principal. True (1) si los ID de fila están determinados por el orden de fila. False (0) si los id. de fila están determinados por los valores de las columnas clave principales del conjunto de registros de datos.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |opcional  <br/> |La fecha y hora en que se actualizó por última vez el conjunto de registros de datos.  <br/> |Valores del tipo xsd:dateTime.  <br/> |
   

