---
title: Proveedor de servicios remotos de Microsoft OLE DB (proveedor de servicios ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54ea659aa5392dd4404ffb591eba06f1f9c2910b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288907"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="7e015-102">Proveedor de comunicación remota de Microsoft OLE DB (proveedor de servicios ADO)</span><span class="sxs-lookup"><span data-stu-id="7e015-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="7e015-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e015-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e015-p101">El Proveedor de servicios remotos de Microsoft OLE DB permite a un usuario local de un equipo cliente llamar a proveedores de datos en un equipo remoto. Especifique los parámetros del proveedor de datos del equipo remoto del mismo modo que si fuera un usuario local del equipo remoto. A continuación, especifique los parámetros usados por el Proveedor de servicios remotos para obtener acceso al equipo remoto. El resultado es que podrá obtener acceso al equipo remoto como si fuera un usuario local.</span><span class="sxs-lookup"><span data-stu-id="7e015-p101">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine. Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine. Then specify the parameters used by the Remoting Provider to access the remote machine. The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="7e015-108">Palabra clave del proveedor</span><span class="sxs-lookup"><span data-stu-id="7e015-108">Provider Keyword</span></span>

<span data-ttu-id="7e015-p102">Para llamar al Proveedor de servicios remotos de OLE DB, especifique la siguiente palabra clave y el siguiente valor en la cadena de conexión. (Tenga en cuenta el espacio en blanco en el nombre del proveedor.)</span><span class="sxs-lookup"><span data-stu-id="7e015-p102">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string. (Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="7e015-111">Palabras clave adicionales</span><span class="sxs-lookup"><span data-stu-id="7e015-111">Additional Keywords</span></span>

<span data-ttu-id="7e015-112">Cuando se llama a este proveedor, también son importantes las siguientes palabras clave adicionales.</span><span class="sxs-lookup"><span data-stu-id="7e015-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e015-113">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="7e015-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="7e015-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e015-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e015-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-116">Especifica el nombre del origen de datos remoto.</span><span class="sxs-lookup"><span data-stu-id="7e015-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="7e015-117">Se pasa al Proveedor de servicios remotos de OLE DB para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="7e015-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="7e015-118">Esta palabra clave es equivalente a la propiedad <a href="connect-property-rds.md">Connect</a> del objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</span><span class="sxs-lookup"><span data-stu-id="7e015-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="7e015-119">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="7e015-119">Dynamic Properties</span></span>

<span data-ttu-id="7e015-120">Cuando se llama a este proveedor de servicios, se agregan las siguientes propiedades dinámicas a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7e015-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e015-121">Nombre de la propiedad dinámica</span><span class="sxs-lookup"><span data-stu-id="7e015-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="7e015-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e015-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e015-123"><strong>DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-124">Indica el modo DataFactory.</span><span class="sxs-lookup"><span data-stu-id="7e015-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="7e015-125">Una cadena que especifica la versión deseada del objeto <a href="datafactory-object-rdsserver.md">DataFactory</a> del servidor.</span><span class="sxs-lookup"><span data-stu-id="7e015-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="7e015-126">Establezca esta propiedad antes de establecer una conexión para solicitar una versión concreta del objeto <strong>DataFactory</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="7e015-127">Si la versión solicitada no está disponible, se intentará utilizar la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="7e015-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="7e015-128">Si no hay una versión anterior, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="7e015-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="7e015-129">Si <strong>DFMode</strong> es inferior a la versión disponible, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="7e015-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="7e015-130">Después de haber establecido la conexión, esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7e015-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="7e015-131">Puede ser uno de los siguientes valores de cadena válidos:</span><span class="sxs-lookup"><span data-stu-id="7e015-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="7e015-132">&quot;25: &quot; versión 2.5 (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="7e015-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="7e015-133">&quot;21: &quot; versión 2.1</span><span class="sxs-lookup"><span data-stu-id="7e015-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="7e015-134">&quot;20: &quot; versión 2.0</span><span class="sxs-lookup"><span data-stu-id="7e015-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="7e015-135">&quot;15: &quot; versión 1.5</span><span class="sxs-lookup"><span data-stu-id="7e015-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e015-136"><strong>Command Properties</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-p105">Indica los valores que se agregarán a la cadena de propiedades de comando (conjunto de filas) enviada al servidor por el proveedor MS Remote. El valor predeterminado de esta cadena es vt_empty.</span><span class="sxs-lookup"><span data-stu-id="7e015-p105">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider. The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e015-139"><strong>Current DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-140">Indica el número de versión real del objeto <strong>DataFactory</strong> del servidor.</span><span class="sxs-lookup"><span data-stu-id="7e015-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="7e015-141">Compruebe esta propiedad para ver si se ha aplicado la versión solicitada en la propiedad <strong>DFMode</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="7e015-142">Puede ser uno de los siguientes valores válidos de tipo entero largo:</span><span class="sxs-lookup"><span data-stu-id="7e015-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="7e015-143">25  — versión 2.5 (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="7e015-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="7e015-144">21  — versión 2.1</span><span class="sxs-lookup"><span data-stu-id="7e015-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="7e015-145">20  — versión 2.0</span><span class="sxs-lookup"><span data-stu-id="7e015-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="7e015-146">15  — versión 1.5</span><span class="sxs-lookup"><span data-stu-id="7e015-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="7e015-147">Agregar DFMode=20; a la cadena de conexión al usar el proveedor &quot; &quot; <strong>MSRemote</strong> puede mejorar el rendimiento del servidor al actualizar datos.</span><span class="sxs-lookup"><span data-stu-id="7e015-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="7e015-148">Con este valor, el objeto <strong>RDSServer.DataFactory</strong> del servidor utiliza un modo que emplea menos recursos.</span><span class="sxs-lookup"><span data-stu-id="7e015-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="7e015-149">No obstante, en esta configuración no están disponibles las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="7e015-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="7e015-150">Uso de consultas parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="7e015-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="7e015-151">Obtención de información de parámetros o columnas antes de llamar al método <strong>Execute</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="7e015-152">Establecimiento de <strong>Transact Updates</strong> en <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7e015-153">Obtención del estado de fila.</span><span class="sxs-lookup"><span data-stu-id="7e015-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="7e015-154">Llamada al método <strong>Resync</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="7e015-155">Actualización (de forma explícita o automática) mediante la propiedad <strong>Update Resync</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="7e015-156">Configuración de las propiedades <strong>Command</strong> o <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="7e015-157">Uso de <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e015-158"><strong>Controlador</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-159">Indica el nombre de un programa de personalización del lado servidor (o controlador) que amplía la funcionalidad de <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>y los parámetros usados por el controlador<em>,</em> todos separados por comas ( &quot; , &quot; ).</span><span class="sxs-lookup"><span data-stu-id="7e015-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="7e015-160">Un valor de tipo <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e015-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e015-161"><strong>Internet Timeout</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-p109">Indica el número máximo de milisegundos que se debe esperar para que una solicitud vaya hacia el servidor y vuelva. (El valor predeterminado es 5 minutos.)</span><span class="sxs-lookup"><span data-stu-id="7e015-p109">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server. (The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e015-164"><strong>Remote Provider</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-165">Indica el nombre del proveedor de datos que se va a utilizar en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="7e015-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e015-166"><strong>Remote Server</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-p110">Indica el nombre del servidor y el protocolo de comunicación que utilizará esta conexión. Esta propiedad es equivalente a la propiedad <a href="server-property-rds.md">Server</a> del objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</span><span class="sxs-lookup"><span data-stu-id="7e015-p110">Indicates the server name and communication protocol to be used by this connection. This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e015-169"><strong>Transact Updates</strong></span><span class="sxs-lookup"><span data-stu-id="7e015-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="7e015-p111">Cuando está establecida en True, este valor indica que cuando se realiza una <a href="updatebatch-method-ado.md">actualización por lotes</a> en el servidor, se hará dentro de una transacción. El valor predeterminado de esta propiedad dinámica booleana es False.</span><span class="sxs-lookup"><span data-stu-id="7e015-p111">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction. The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e015-p112">También es posible establecer propiedades dinámicas que se pueden escribir si se especifican sus nombres como palabras clave en la cadena de conexión. Por ejemplo, establezca la propiedad dinámica **Internet Timeout** en cinco segundos al especificar:</span><span class="sxs-lookup"><span data-stu-id="7e015-p112">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="7e015-p113">También es posible establecer o recuperar una propiedad dinámica al especificar su nombre como índice de la propiedad **Properties**. Por ejemplo, obtenga e imprima el valor actual de la propiedad dinámica **Internet Timeout** y, a continuación, establezca un nuevo valor como éste:</span><span class="sxs-lookup"><span data-stu-id="7e015-p113">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property. For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="7e015-176">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e015-176">Remarks</span></span>

<span data-ttu-id="7e015-p114">En ADO 2.0, solo se podría especificar el Proveedor de servicios remotos de OLE DB en el parámetro *ActiveConnection* del método **Open** del objeto [Recordset](recordset-object-ado.md). Con ADO 2.1, también se puede especificar el proveedor en el parámetro *ConnectionString* del método **Open** del objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7e015-p114">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method. Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="7e015-p115">El equivalente de la propiedad [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) del objeto **RDS.DataControl** no está disponible. En su lugar se usa el argumento *Source* del método **Open** del objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7e015-p115">The equivalent of the **RDS.DataControl** object [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property is not available. The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="7e015-181">La especificación de "...;Remote Provider=MS Remote;..." crearía un escenario de cuatro niveles. No se han probado los escenarios de más de tres niveles y no deberían ser necesarios.</span><span class="sxs-lookup"><span data-stu-id="7e015-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="7e015-182">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e015-182">Example</span></span>

<span data-ttu-id="7e015-p116">En este ejemplo se realiza una consulta en la tabla **authors** de la base de datos **pubs** de un servidor denominado *YourServer*. Los nombres del origen de datos remoto y del servidor remoto se proporcionan en el método [Open](open-method-ado-connection.md) del objeto [Connection](connection-object-ado.md) y la consulta SQL se especifica en el método [Open](open-method-ado-recordset.md) del objeto [Recordset](recordset-object-ado.md). Para actualizar el origen de datos se devuelve, modifica y usa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7e015-p116">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*. The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method. A **Recordset** object is returned, edited, and used to update the data source.</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
Dim cn as New ADODB.Connection 
cn.Open  "Provider=MS Remote;Data Source=pubs;" & _ 
         "Remote Server=https://YourServer" 
rs.Open "SELECT * FROM authors", cn 
...                'Edit the recordset 
rs.UpdateBatch     'Equivalent of RDS SubmitChanges 
... 
```

