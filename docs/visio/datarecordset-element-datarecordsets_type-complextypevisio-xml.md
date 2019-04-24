---
title: Elemento DataRecordset (DataRecordSets_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.
ms.openlocfilehash: e2baaeed38318f35d4bd4ce4269f71b6304b148f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360371"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>Elemento DataRecordset (DataRecordSets_Type complexType) ("XML" de Visio)

Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos **DataRecordset** del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contiene XML que se ajusta al esquema XML clásico de ADO para un objeto Recordset de ADO y que describe los datos del conjunto de registros de datos.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Define una regla que compara una columna del elemento **DataRecordset** principal con un elemento de datos de formas de la última acción de vinculación automática correcta realizada en la interfaz de usuario.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Define cómo aparece una columna de datos en la ventana **datos externos** de la interfaz de usuario de Visio y califica los datos de la columna mediante la definición de su formato y tipo de datos.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos **DataColumn** de un conjunto de registros de datos.  <br/> |
|[ClavePrincipal](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifica una o más columnas de clave principal del conjunto de registros de datos.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indica una fila del conjunto de registros de datos vinculada a una forma que está en conflicto después de actualizar el conjunto de registros de datos.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Asigna una fila de un conjunto de registros de datos a una forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Suma de comprobación  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Un valor de suma de comprobación, generado por Visio y basado en las propiedades del conjunto de registros de datos. Establezca este attirbute en 0; Visio recalcula este valor en tiempo de ejecución.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Command  <br/> |xsd: String  <br/> |opcional  <br/> |La cadena de comando usada para consultar datos del origen de datos.  <br/> |Valores del tipo xsd: String.  <br/> |
|ConnectionID  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |IDENTIFICADOR de conexión del objeto **DataConnection** asociado. No existe para orígenes de datos XML.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR del conjunto de registros de datos, único dentro del documento.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre de la presentación (o "descriptiva") del conjunto de registros de datos.  <br/> |Valores del tipo xsd: String.  <br/> |
|NextRowID  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Siguiente identificador de fila de Visio disponible.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Opciones  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Opciones para aplicar al conjunto de registros de datos. Los valores posibles pueden ser cualquier combinación de uno o más de los que se muestran en la tabla siguiente.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|RefreshInterval  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Frecuencia (en minutos) que Visio actualiza automáticamente el conjunto de registros de datos. Este valor debe ser 1 o mayor.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Si la interfaz de usuario de conciliación de datos debe estar deshabilitada. True (1) para deshabilitar la interfaz de usuario (UI). False (0) para habilitar la interfaz de usuario.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|RefreshOverwriteAll  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Si se van a sobrescribir los cambios del usuario en los elementos de datos de formas de las formas vinculadas a los datos al actualizar el conjunto de registros de datos.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|ReplaceLinks  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Define cómo se tratan los vínculos de datos de formas cuando se copian o cortan formas. 1 para reemplazar los vínculos existentes en la forma de destino. 0 para mantener los vínculos existentes en la forma de destino.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|RowOrder  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Si se va a utilizar el orden de las filas del conjunto de registros de datos como clave principal. True (1) si los identificadores de fila se determinan por orden de fila. False (0) si los identificadores de fila se determinan por los valores de la columna o columnas de clave principal del conjunto de registros de datos.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|TimeRefreshed  <br/> |xsd: dateTime  <br/> |opcional  <br/> |Fecha y hora en que se actualizó el conjunto de registros de datos por última vez.  <br/> |Valores del tipo xsd: dateTime.  <br/> |
   

