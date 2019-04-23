---
title: Servicio de cursores para OLE DB de Microsoft (componente de servicios ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d79d060922c6e7f28209242ebe82821c2ba97bfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288991"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a>Servicio de cursores de Microsoft para OLE DB (componente de servicio ADO)


**Se aplica a:** Access 2013, Office 2013

El Servicio de cursores para OLE DB de Microsoft complementa a las funciones de compatibilidad de cursor de los proveedores de datos. Como resultado, el usuario percibe una funcionalidad relativamente uniforme en todos los proveedores de datos.

El Servicio de cursores hace que las propiedades dinámicas estén disponibles y mejora el comportamiento de algunos métodos. Por ejemplo, la propiedad dinámica [Optimize](optimize-property-dynamic-ado.md) habilita la creación de índices temporales para facilitar algunas operaciones, como el método [Find](find-method-ado.md).

El Servicio de cursores habilita la compatibilidad con la actualización por lotes en todos los casos. También simula tipos de cursor más eficaces, como los cursores dinámicos, cuando un proveedor de datos sólo puede proporcionar cursores menos eficaces, como los estáticos.

## <a name="keyword"></a>Palabra clave

Para llamar a este componente de servicios, establezca la propiedad [CursorLocation](cursorlocation-property-ado.md) de los objetos [Recordset](recordset-object-ado.md) o [Connection](connection-object-ado.md) en **adUseClient**.

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Propiedades dinámicas

Cuando se llama al Servicio de cursores para OLE DB, se agregan las siguientes propiedades dinámicas a la colección [Properties](properties-collection-ado.md) del objeto **Recordset**. La lista completa de propiedades dinámicas de los objetos **Connection** y **Recordset** se puede consultar en el [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md). Los nombres de las propiedades de OLE DB asociadas se incluyen, cuando resulta adecuado, entre paréntesis tras el nombre de la propiedad ADO.

Los cambios realizados en algunas propiedades dinámicas no son visibles para el origen de datos subyacente una vez que se ha llamado al Servicio de cursores. Por ejemplo, el establecimiento de la propiedad *Command Time out* en un objeto **Recordset** no será visible para el proveedor de datos subyacente.

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

Si la aplicación necesita el Servicio de cursores pero usted necesita establecer propiedades dinámicas en el proveedor subyacente, establezca las propiedades antes de llamar al Servicio de cursores. La configuración de la propiedad del objeto Command siempre pasa al proveedor de datos subyacente independientemente de la ubicación del cursor. Por lo tanto, se puede utilizar un objeto Command para establecer las propiedades en cualquier momento.

> [!NOTE]
> [!NOTA] La propiedad dinámica DBPROP_SERVERDATAONINSERT no es admitida por el Servicio de cursores, aun cuando sea admitida por el proveedor de datos subyacente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Auto Recalc<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>En los conjuntos de registros creados mediante el Servicio de forma de datos, este valor indica la frecuencia con que se calculan las columnas calculadas y de agregado. El valor predeterminado (=1) es volver a calcular siempre que el Servicio de forma de datos determina que los valores han cambiado. Si el valor es 0, las columnas calculadas o de agregado sólo se calculan cuando se elabora inicialmente la jerarquía.</p></td>
</tr>
<tr class="even">
<td><p>Batch Size<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>Indica el número de instrucciones de actualización que se pueden reunir en lotes antes de enviarse al almacén de datos. Cuantas más instrucciones haya en un lote, menos viajes se necesitarán al almacén de datos.</p></td>
</tr>
<tr class="odd">
<td><p>Cache Child Rows<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>En los conjuntos de registros creados mediante el Servicio de forma de datos, este valor indica si los conjuntos de registros secundarios se han almacenado en una memoria caché para ser utilizados posteriormente.</p></td>
</tr>
<tr class="even">
<td><p>Cursor Engine Version<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>Indica la versión del Servicio de cursores que se utiliza.</p></td>
</tr>
<tr class="odd">
<td><p>Maintain Change Status<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>Indica el texto del comando utilizado para volver a sincronizar una o más filas de una combinación de varias tablas.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Optimizar</a></p></td>
<td><p>Indica si se debe crear un índice. Cuando está establecida en <strong>True</strong>, autoriza la creación temporal de índices para mejorar la ejecución de algunas operaciones.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Indica el nombre del objeto <strong>Recordset</strong>. Se puede hacer referencia a ella en los comandos de forma de datos actuales o siguientes.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Indica una cadena de comando utilizada por el método <a href="resync-method-ado.md">Resync</a> cuando la propiedad <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> está activada.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></p></td>
<td><p>Indica el nombre de la base de datos que contiene la tabla a la que se hace referencia en la propiedad <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></p></td>
<td><p>Indica el nombre del propietario de la tabla a la que se hace referencia en la propiedad <strong> Unique Table</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></p></td>
<td><p>Indica el nombre de la única tabla de un objeto <strong>Recordset</strong> creado a partir de varias tablas que se pueden modificar mediante inserciones, actualizaciones o eliminaciones.</p></td>
</tr>
<tr class="even">
<td><p>Update Criteria<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>Indica qué campos de la cláusula <strong>WHERE</strong> se utilizan para controlar conflictos producidos durante una actualización.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p>Indica si se llama al método <strong>Resync</strong> de forma implícita después de llamar al método <a href="updatebatch-method-ado.md">UpdateBatch</a> (y su comportamiento) cuando la propiedad <strong>Unique Table</strong> está activada.</p></td>
</tr>
</tbody>
</table>


También es posible establecer o recuperar una propiedad dinámica al especificar su nombre como índice de la colección **Properties**. Por ejemplo, obtenga e imprima el valor actual de la propiedad dinámica [Optimize](optimize-property-dynamic-ado.md) y a continuación establezca un nuevo valor como éste:

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Comportamiento de las propiedades integradas

El Servicio de cursores para OLE DB también afecta al comportamiento de algunas propiedades integradas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Complementa a los tipos de cursores disponibles para un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Complementa a los tipos de bloqueos disponibles para un objeto <strong>Recordset</strong>. Habilita las actualizaciones por lotes.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Especifica uno o más nombres de campo por los que está ordenado el objeto <strong>Recordset</strong> y si cada campo está ordenado de forma ascendente o descendente.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Comportamiento de los métodos

El Servicio de cursores para OLE DB habilita o afecta al comportamiento del método [Append](append-method-ado.md) del objeto [Field](field-object-ado.md) y a los métodos [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) y [Save](save-method-ado.md) del objeto **Recordset**.

