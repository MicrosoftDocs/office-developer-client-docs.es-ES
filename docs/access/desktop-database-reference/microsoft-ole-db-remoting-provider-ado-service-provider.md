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
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Proveedor de comunicación remota de Microsoft OLE DB (proveedor de servicios ADO)

**Se aplica a:** Access 2013, Office 2013

El Proveedor de servicios remotos de Microsoft OLE DB permite a un usuario local de un equipo cliente llamar a proveedores de datos en un equipo remoto. Especifique los parámetros del proveedor de datos del equipo remoto del mismo modo que si fuera un usuario local del equipo remoto. A continuación, especifique los parámetros usados por el Proveedor de servicios remotos para obtener acceso al equipo remoto. El resultado es que podrá obtener acceso al equipo remoto como si fuera un usuario local.

## <a name="provider-keyword"></a>Palabra clave del proveedor

Para llamar al Proveedor de servicios remotos de OLE DB, especifique la siguiente palabra clave y el siguiente valor en la cadena de conexión. (Tenga en cuenta el espacio en blanco en el nombre del proveedor.)

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>Palabras clave adicionales

Cuando se llama a este proveedor, también son importantes las siguientes palabras clave adicionales.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palabra clave</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Data Source</strong></p></td>
<td><p>Especifica el nombre del origen de datos remoto. Se pasa al Proveedor de servicios remotos de OLE DB para su procesamiento. Esta palabra clave es equivalente a la propiedad <a href="connect-property-rds.md">Connect</a> del objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Propiedades dinámicas

Cuando se llama a este proveedor de servicios, se agregan las siguientes propiedades dinámicas a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de la propiedad dinámica</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>Indica el modo DataFactory. Una cadena que especifica la versión deseada del objeto <a href="datafactory-object-rdsserver.md">DataFactory</a> del servidor. Establezca esta propiedad antes de establecer una conexión para solicitar una versión concreta del objeto <strong>DataFactory</strong>. Si la versión solicitada no está disponible, se intentará utilizar la versión anterior. Si no hay una versión anterior, se producirá un error. Si <strong>DFMode</strong> es inferior a la versión disponible, se producirá un error. Después de haber establecido la conexión, esta propiedad es de solo lectura. Puede ser uno de los siguientes valores de cadena válidos:</p>
<p></p>
<ul>
<li><p>&quot;25&quot; : versión 2,5 (predeterminado)</p></li>
<li><p>&quot;21&quot; : versión 2,1</p></li>
<li><p>&quot;20&quot; : versión 2,0</p></li>
<li><p>&quot;15&quot; , versión 1,5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Command Properties</strong></p></td>
<td><p>Indica los valores que se agregarán a la cadena de propiedades de comando (conjunto de filas) enviada al servidor por el proveedor MS Remote. El valor predeterminado de esta cadena es vt_empty.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Current DFMode</strong></p></td>
<td><p>Indica el número de versión real del objeto <strong>DataFactory</strong> del servidor. Compruebe esta propiedad para ver si se ha aplicado la versión solicitada en la propiedad <strong>DFMode</strong>. Puede ser uno de los siguientes valores válidos de tipo entero largo:</p>
<p></p>
<ul>
<li><p>25  — versión 2.5 (predeterminada)</p></li>
<li><p>21  — versión 2.1</p></li>
<li><p>20  — versión 2.0</p></li>
<li><p>15  — versión 1.5</p></li>
</ul>
<p></p>
<p>Adición &quot;de DFMode = 20; &quot; a la cadena de conexión cuando se usa el proveedor <strong>MSRemote</strong> puede mejorar el rendimiento del servidor al actualizar datos. Con este valor, el objeto <strong>RDSServer.DataFactory</strong> del servidor utiliza un modo que emplea menos recursos. No obstante, en esta configuración no están disponibles las siguientes características:</p>
<p></p>
<ul>
<li><p>Uso de consultas parametrizadas.</p></li>
<li><p>Obtención de información de parámetros o columnas antes de llamar al método <strong>Execute</strong>.</p></li>
<li><p>Establecimiento de <strong>Transact Updates</strong> en <strong>True</strong>.</p></li>
<li><p>Obtención del estado de fila.</p></li>
<li><p>Llamada al método <strong>Resync</strong>.</p></li>
<li><p>Actualización (de forma explícita o automática) mediante la propiedad <strong>Update Resync</strong>.</p></li>
<li><p>Configuración de las propiedades <strong>Command</strong> o <strong>Recordset</strong>.</p></li>
<li><p>Uso de <strong>adCmdTableDirect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Controlador</strong></p></td>
<td><p>Indica el nombre de un programa de personalización del servidor (o controlador) que amplía la funcionalidad de <a href="datafactory-object-rdsserver.md">RDSServer. DataFactory</a>y de cualquier parámetro utilizado por el controlador<em>,</em> todo separado por comas (&quot;,&quot;). Un valor de tipo <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Internet Timeout</strong></p></td>
<td><p>Indica el número máximo de milisegundos que se debe esperar para que una solicitud vaya hacia el servidor y vuelva. (El valor predeterminado es 5 minutos.)</p></td>
</tr>
<tr class="even">
<td><p><strong>Remote Provider</strong></p></td>
<td><p>Indica el nombre del proveedor de datos que se va a utilizar en el servidor remoto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Remote Server</strong></p></td>
<td><p>Indica el nombre del servidor y el protocolo de comunicación que utilizará esta conexión. Esta propiedad es equivalente a la propiedad <a href="server-property-rds.md">Server</a> del objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transact Updates</strong></p></td>
<td><p>Cuando está establecida en True, este valor indica que cuando se realiza una <a href="updatebatch-method-ado.md">actualización por lotes</a> en el servidor, se hará dentro de una transacción. El valor predeterminado de esta propiedad dinámica booleana es False.</p></td>
</tr>
</tbody>
</table>


También es posible establecer propiedades dinámicas que se pueden escribir si se especifican sus nombres como palabras clave en la cadena de conexión. Por ejemplo, establezca la propiedad dinámica **Internet Timeout** en cinco segundos al especificar:

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

También es posible establecer o recuperar una propiedad dinámica al especificar su nombre como índice de la propiedad **Properties**. Por ejemplo, obtenga e imprima el valor actual de la propiedad dinámica **Internet Timeout** y, a continuación, establezca un nuevo valor como éste:

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Comentarios

En ADO 2.0, solo se podría especificar el Proveedor de servicios remotos de OLE DB en el parámetro *ActiveConnection* del método **Open** del objeto [Recordset](recordset-object-ado.md). Con ADO 2.1, también se puede especificar el proveedor en el parámetro *ConnectionString* del método **Open** del objeto [Connection](connection-object-ado.md).

El equivalente de la propiedad [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) del objeto **RDS.DataControl** no está disponible. En su lugar se usa el argumento *Source* del método **Open** del objeto [Recordset](recordset-object-ado.md).

La especificación de "...;Remote Provider=MS Remote;..." crearía un escenario de cuatro niveles. No se han probado los escenarios de más de tres niveles y no deberían ser necesarios.

## <a name="example"></a>Ejemplo

En este ejemplo se realiza una consulta en la tabla **authors** de la base de datos **pubs** de un servidor denominado *YourServer*. Los nombres del origen de datos remoto y del servidor remoto se proporcionan en el método [Open](open-method-ado-connection.md) del objeto [Connection](connection-object-ado.md) y la consulta SQL se especifica en el método [Open](open-method-ado-recordset.md) del objeto [Recordset](recordset-object-ado.md). Para actualizar el origen de datos se devuelve, modifica y usa un objeto **Recordset**.

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

