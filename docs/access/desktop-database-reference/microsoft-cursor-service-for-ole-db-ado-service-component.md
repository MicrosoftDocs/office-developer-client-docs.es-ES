---
title: Servicio de cursores para OLE DB de Microsoft (componente de servicios ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f164e2671fb27a8e8a8721010bdad518f2d199e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879058"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="95ed1-102">Servicio de cursores para OLE DB de Microsoft (componente de servicios ADO)</span><span class="sxs-lookup"><span data-stu-id="95ed1-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="95ed1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95ed1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95ed1-p101">El Servicio de cursores para OLE DB de Microsoft complementa a las funciones de compatibilidad de cursor de los proveedores de datos. Como resultado, el usuario percibe una funcionalidad relativamente uniforme en todos los proveedores de datos.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p101">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers. As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="95ed1-p102">El Servicio de cursores hace que las propiedades dinámicas estén disponibles y mejora el comportamiento de algunos métodos. Por ejemplo, la propiedad dinámica [Optimize](optimize-property-dynamic-ado.md) habilita la creación de índices temporales para facilitar algunas operaciones, como el método [Find](find-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="95ed1-p102">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods. For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="95ed1-p103">El Servicio de cursores habilita la compatibilidad con la actualización por lotes en todos los casos. También simula tipos de cursor más eficaces, como los cursores dinámicos, cuando un proveedor de datos sólo puede proporcionar cursores menos eficaces, como los estáticos.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="95ed1-110">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="95ed1-110">Keyword</span></span>

<span data-ttu-id="95ed1-111">Para llamar a este componente de servicios, establezca la propiedad [CursorLocation](recordset-object-ado.md) de los objetos [Recordset](connection-object-ado.md) o [Connection](cursorlocation-property-ado.md) en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="95ed1-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="95ed1-112">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="95ed1-112">Dynamic Properties</span></span>

<span data-ttu-id="95ed1-p104">Cuando se llama al Servicio de cursores para OLE DB, se agregan las siguientes propiedades dinámicas a la colección **Properties** del objeto [Recordset](properties-collection-ado.md). La lista completa de propiedades dinámicas de los objetos **Connection** y **Recordset** se puede consultar en el [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md). Los nombres de las propiedades de OLE DB asociadas se incluyen, cuando resulta adecuado, entre paréntesis tras el nombre de la propiedad ADO.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p104">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection. The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md). The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="95ed1-116">Los cambios realizados en algunas propiedades dinámicas no son visibles para el origen de datos subyacente una vez que se ha llamado al Servicio de cursores.</span><span class="sxs-lookup"><span data-stu-id="95ed1-116">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</span></span> <span data-ttu-id="95ed1-117">Por ejemplo, el establecimiento de la propiedad *Command Time out* en un **objeto Recordset** no estará visible para el proveedor de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="95ed1-117">For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

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

<span data-ttu-id="95ed1-p106">Si la aplicación necesita el Servicio de cursores pero usted necesita establecer propiedades dinámicas en el proveedor subyacente, establezca las propiedades antes de llamar al Servicio de cursores. La configuración de la propiedad del objeto Command siempre pasa al proveedor de datos subyacente independientemente de la ubicación del cursor. Por lo tanto, se puede utilizar un objeto Command para establecer las propiedades en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p106">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service. Command object property settings are always passed to the underlying data provider regardless of cursor location. Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="95ed1-121">La propiedad dinámica DBPROP_SERVERDATAONINSERT no es admitida por el Servicio de cursores, aun cuando sea admitida por el proveedor de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="95ed1-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95ed1-122">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="95ed1-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="95ed1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="95ed1-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-124">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="95ed1-124">Auto Recalc</span></span><br />
<span data-ttu-id="95ed1-125">(DBPROP_ADC_AUTORECALC)</span><span class="sxs-lookup"><span data-stu-id="95ed1-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="95ed1-p107">En los conjuntos de registros creados mediante el Servicio de forma de datos, este valor indica la frecuencia con que se calculan las columnas calculadas y de agregado. El valor predeterminado (=1) es volver a calcular siempre que el Servicio de forma de datos determina que los valores han cambiado. Si el valor es 0, las columnas calculadas o de agregado sólo se calculan cuando se elabora inicialmente la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p107">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated. The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed. If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ed1-129">Batch Size</span><span class="sxs-lookup"><span data-stu-id="95ed1-129">Batch Size</span></span><br />
<span data-ttu-id="95ed1-130">(DBPROP_ADC_BATCHSIZE)</span><span class="sxs-lookup"><span data-stu-id="95ed1-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="95ed1-p108">Indica el número de instrucciones de actualización que se pueden reunir en lotes antes de enviarse al almacén de datos. Cuantas más instrucciones haya en un lote, menos viajes se necesitarán al almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p108">Indicates the number of update statements that can be batched before being sent to the data store. The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-133">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="95ed1-133">Cache Child Rows</span></span><br />
<span data-ttu-id="95ed1-134">(DBPROP_ADC_CACHECHILDROWS)</span><span class="sxs-lookup"><span data-stu-id="95ed1-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="95ed1-135">En los conjuntos de registros creados mediante el Servicio de forma de datos, este valor indica si los conjuntos de registros secundarios se han almacenado en una memoria caché para ser utilizados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="95ed1-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ed1-136">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="95ed1-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="95ed1-137">(DBPROP_ADC_CEVER)</span><span class="sxs-lookup"><span data-stu-id="95ed1-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="95ed1-138">Indica la versión del Servicio de cursores que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="95ed1-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-139">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="95ed1-139">Maintain Change Status</span></span><br />
<span data-ttu-id="95ed1-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span><span class="sxs-lookup"><span data-stu-id="95ed1-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="95ed1-141">Indica el texto del comando utilizado para volver a sincronizar una o más filas de una combinación de varias tablas.</span><span class="sxs-lookup"><span data-stu-id="95ed1-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ed1-142"><a href="optimize-property-dynamic-ado.md">Optimizar</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-p109">Indica si se debe crear un índice. Cuando está establecida en <strong>True</strong>, autoriza la creación temporal de índices para mejorar la ejecución de algunas operaciones.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p109">Indicates whether an index should be created. When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-p110">Indica el nombre del objeto <strong>Recordset</strong>. Se puede hacer referencia a ella en los comandos de forma de datos actuales o siguientes.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p110">Indicates the name of the <strong>Recordset</strong>. May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ed1-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-149">Indica una cadena de comando utilizada por el método <a href="resync-method-ado.md">Resync</a> cuando la propiedad <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> está activada.</span><span class="sxs-lookup"><span data-stu-id="95ed1-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-151">Indica el nombre de la base de datos que contiene la tabla a la que se hace referencia en la propiedad <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="95ed1-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ed1-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-153">Indica el nombre del propietario de la tabla a la que se hace referencia en la propiedad <strong> Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="95ed1-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-155">Indica el nombre de la única tabla de un objeto <strong>Recordset</strong> creado a partir de varias tablas que se pueden modificar mediante inserciones, actualizaciones o eliminaciones.</span><span class="sxs-lookup"><span data-stu-id="95ed1-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ed1-156">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="95ed1-156">Update Criteria</span></span><br />
<span data-ttu-id="95ed1-157">(DBPROP_ADC_UPDATECRITERIA)</span><span class="sxs-lookup"><span data-stu-id="95ed1-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="95ed1-158">Indica qué campos de la cláusula <strong>WHERE</strong> se utilizan para controlar conflictos producidos durante una actualización.</span><span class="sxs-lookup"><span data-stu-id="95ed1-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span><span class="sxs-lookup"><span data-stu-id="95ed1-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="95ed1-160">Indica si se llama al método <strong>Resync</strong> de forma implícita después de llamar al método <a href="updatebatch-method-ado.md">UpdateBatch</a> (y su comportamiento) cuando la propiedad <strong>Unique Table</strong> está activada.</span><span class="sxs-lookup"><span data-stu-id="95ed1-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95ed1-p111">También es posible establecer o recuperar una propiedad dinámica al especificar su nombre como índice de la colección **Properties**. Por ejemplo, obtenga e imprima el valor actual de la propiedad dinámica [Optimize](optimize-property-dynamic-ado.md) y a continuación establezca un nuevo valor como éste:</span><span class="sxs-lookup"><span data-stu-id="95ed1-p111">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection. For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="95ed1-163">Comportamiento de las propiedades integradas</span><span class="sxs-lookup"><span data-stu-id="95ed1-163">Built-in Property Behavior</span></span>

<span data-ttu-id="95ed1-164">El Servicio de cursores para OLE DB también afecta al comportamiento de algunas propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="95ed1-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95ed1-165">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="95ed1-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="95ed1-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="95ed1-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-168">Complementa a los tipos de cursores disponibles para un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="95ed1-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ed1-169"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-p112">Complementa a los tipos de bloqueos disponibles para un objeto <strong>Recordset</strong>. Habilita las actualizaciones por lotes.</span><span class="sxs-lookup"><span data-stu-id="95ed1-p112">Supplements the types of locks available for a <strong>Recordset</strong>. Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ed1-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="95ed1-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="95ed1-173">Especifica uno o más nombres de campo por los que está ordenado el objeto <strong>Recordset</strong> y si cada campo está ordenado de forma ascendente o descendente.</span><span class="sxs-lookup"><span data-stu-id="95ed1-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="95ed1-174">Comportamiento de los métodos</span><span class="sxs-lookup"><span data-stu-id="95ed1-174">Method Behavior</span></span>

<span data-ttu-id="95ed1-175">El Servicio de cursores para OLE DB habilita o afecta al comportamiento del método [Append](field-object-ado.md) del objeto [Field](append-method-ado.md) y a los métodos **Open**, [Resync](open-method-ado-recordset.md), [UpdateBatch](resync-method-ado.md) y [Save](updatebatch-method-ado.md) del objeto [Recordset](save-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="95ed1-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

