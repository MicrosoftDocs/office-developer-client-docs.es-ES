---
title: Elemento DataRecordSet (DataRecordSets_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.
ms.openlocfilehash: 157213476214c736367b724dd6ca944060c53467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821924"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>Elemento DataRecordSet (DataRecordSets_Type complexType) ('XML de Visio')

Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos de **DataRecordset** en el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contiene el XML que se ajusta al esquema XML clásico ADO para un objeto recordset de ADO y que describe los datos en el conjunto de registros de datos.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Define una regla que se compara una columna en el elemento de **DataRecordset** primario con un elemento de datos de formas de la última correcta automática vinculación acción realizada en la interfaz de usuario.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Define cómo aparece una columna de datos en la ventana **Datos externos** en la interfaz de usuario de Visio y califica los datos en la columna mediante la definición de su tipo de datos y el formato.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos de **DataColumn** de un conjunto de registros de datos.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifica una o más columnas de clave principal en el conjunto de registros de datos.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indica una fila en el conjunto de registros de datos vinculada a una forma que está en conflicto después de actualiza el conjunto de registros de datos.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Asigna una fila del conjunto de registros de datos a una forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Suma de comprobación  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Un valor de suma de comprobación, generadas por Visio y en función de las propiedades del conjunto de registros de datos. Establezca este attirbute en 0; Visio vuelve a calcular este valor en tiempo de ejecución.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Comando  <br/> |xsd: String  <br/> |opcional  <br/> |La cadena de comando utilizada para consultar los datos del origen de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador de conexión para el objeto **DataConnection** asociado. No existe para orígenes de datos XML.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador de conjunto de registros de datos, único dentro del documento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Para mostrar (o "descriptivo") nombre del conjunto de registros de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El siguiente identificador de fila de Visio disponible  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Options  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Opciones que se debe aplicar al conjunto de registros de datos. Los valores posibles pueden ser cualquier combinación de uno o varios de los que se muestran en la siguiente tabla.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |¿Con qué frecuencia (en minutos) Visio actualiza automáticamente el conjunto de registros de datos. Este valor debe ser 1 o mayor.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Si se debe deshabilitar la interfaz de usuario de conciliación de datos. El valor True (1) para deshabilitar la interfaz de usuario (UI). False (0) para habilitar la interfaz de usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|RefreshOverwriteAll  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Si se debe sobrescribir los cambios del usuario a los elementos de datos de forma de las formas vinculadas a los datos cuando se actualiza el conjunto de registros de datos.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Define cómo se tratan los vínculos de datos de formas cuando se copian o cortan formas. 1 para reemplazar los vínculos existentes en la forma de destino. 0 para mantener los vínculos existentes en la forma de destino.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Si se utiliza el orden de las filas en el conjunto de registros de datos como la clave principal. El valor True (1) si los identificadores de fila se determinan mediante el orden de las filas. False (0) si los identificadores de fila vienen determinados por los valores en las columnas de clave principal del conjunto de registros de datos.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|TimeRefreshed  <br/> |xsd: DateTime  <br/> |opcional  <br/> |La fecha y la hora que se actualizó por última vez el conjunto de registros de datos.  <br/> |Valores del tipo XSD: DateTime.  <br/> |
   

