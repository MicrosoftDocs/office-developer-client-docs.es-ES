---
title: Proveedor de Microsoft OLE DB para Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4f1c46b390e1f059e57f3b7a70fc667da4b09b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712844"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a>Proveedor de Microsoft OLE DB para Microsoft Jet

**Se aplica a**: Access 2013, Office 2013

El Proveedor OLE DB para Microsoft Jet permite que ADO obtenga acceso a bases de datos de Microsoft Jet.

## <a name="connection-string-parameters"></a>Parámetros de la cadena de conexión

Para conectar con este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.

## <a name="typical-connection-string"></a>Cadena de conexión típica

Una típica cadena de conexión de este proveedor es:

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

La cadena consta de estas palabras clave:

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
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica el Proveedor OLE DB para Microsoft Jet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Especifica el nombre de archivo y la ruta de acceso a la base de datos (por ejemplo, c:\Northwind.mdb).</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>Especifica el nombre de usuario. Si no se especifica esta palabra clave, la cadena &quot;administración&quot;, se usa de forma predeterminada.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica la contraseña de usuario. Si no se especifica esta palabra clave, una cadena vacía (&quot;&quot;), se usa de forma predeterminada.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Parámetros de conexión específicos del proveedor

El Proveedor OLE DB para Microsoft Jet admite varias propiedades dinámicas específicas del proveedor además de las definidas por ADO. Al igual que ocurre con el resto de parámetros **Connection**, se pueden establecer mediante la colección **Properties** del objeto **Connection** o como parte de la cadena de conexión.

En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Cantidad de espacio recuperado de Jet OLEDB<br />
(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</p></td>
<td><p>Indica una estimación de la cantidad de espacio, en bytes, que se puede recuperar al compactar la base de datos. Este valor sólo es válido después de haber establecido una conexión de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Connection Control<br />
(DBPROP_JETOLEDB_CONNECTIONCONTROL)</p></td>
<td><p>Indica si los usuarios se pueden conectar a la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: crear base de datos del sistema<br />
(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</p></td>
<td><p>Indica si se debe crear una base de datos del sistema al crear un nuevo origen de datos.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Database Locking Mode<br />
(DBPROP_JETOLEDB_DATABASELOCKMODE)</p></td>
<td><p>Indica el modo de bloqueo de esta base de datos. El primer usuario que la abre determina el modo que se utilizará mientras la base de datos esté abierta.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Database Password<br />
(DBPROP_JETOLEDB_DATABASEPASSWORD)</p></td>
<td><p>Indica la contraseña de la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Don't Copy Locale on Compact<br />
(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</p></td>
<td><p>Indica si Jet debe copiar información de configuración regional al compactar una base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Encrypt Database<br />
(DBPROP_JETOLEDB_ENCRYPTDATABASE)</p></td>
<td><p>Indica si una base de datos compactada debe ser cifrada. Si esta propiedad no está establecida, la base de datos compactada se cifrará si la base de datos original también estaba cifrada.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Engine Type<br />
(DBPROP_JETOLEDB_ENGINE)</p></td>
<td><p>Indica el motor de almacenamiento utilizado para obtener acceso al almacén de datos actual.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Exclusive Async Delay<br />
(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</p></td>
<td><p>Indica la longitud máxima de tiempo, en milisegundos, que Jet puede retrasar las escrituras asincrónicas en el disco cuando se abre la base de datos de forma exclusiva. Esta propiedad se omite a menos que <strong>Jet OLEDB:Flush Transaction Timeout</strong> esté establecido en 0.  </p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Flush Transaction Timeout<br />
(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</p></td>
<td><p>Indica la cantidad de tiempo que se debe esperar antes de que los datos almacenados en una memoria caché en espera de escritura asincrónica se escriban realmente en el disco. Este valor sobrescribe a los valores de <strong>Jet OLEDB:Shared Async Delay</strong> y <strong>Jet OLEDB:Exclusive Async Delay</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Global Bulk Transactions<br />
(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</p></td>
<td><p>Indica si se negocian transacciones masivas SQL.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Global Partial Bulk Ops<br />
(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</p></td>
<td><p>Indica la contraseña que se utiliza para abrir la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Implicit Commit Sync<br />
(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</p></td>
<td><p>Indica si los cambios realizados en transacciones implícitas internas se escriben en modo sincrónico o asincrónico.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Lock Delay<br />
(DBPROP_JETOLEDB_LOCKDELAY)</p></td>
<td><p>Indica el número de milisegundos que se debe esperar antes de intentar conseguir un bloqueo después de que un intento anterior diera lugar a un error.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Lock Retry<br />
(DBPROP_JETOLEDB_LOCKRETRY)</p></td>
<td><p>Indica cuántas veces se repite un intento de acceso a una página bloqueada.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Max Buffer Size<br />
(DBPROP_JETOLEDB_MAXBUFFERSIZE)</p></td>
<td><p>Indica la cantidad máxima de memoria, en kilobytes, que Jet puede utilizar antes de comenzar a volcar cambios al disco.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Max Locks Per File<br />
(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</p></td>
<td><p>Indica el número máximo de bloqueos que puede colocar Jet en una base de datos. El valor predeterminado es 9500.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: contraseña de base de datos nueva<br />
(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</p></td>
<td><p>Indica la nueva contraseña que se debe establecer para esta base de datos. La contraseña antigua se almacena en <strong>Jet OLEDB:Database Password</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: ODBC Command Time Out<br />
(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</p></td>
<td><p>Indica el número de milisegundos que transcurren antes de que una consulta remota ODBC de Jet supere el tiempo de espera.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Page bloqueos a bloqueo de tabla<br />
(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</p></td>
<td><p>Indica cuántas páginas deben ser bloqueadas en una transacción antes de que Jet intente promover el bloqueo a un bloqueo de tabla. Si este valor es 0, el bloqueo no se promueve nunca.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Page Timeout<br />
(DBPROP_JETOLEDB_PAGETIMEOUT)</p></td>
<td><p>Indica el número de milisegundos que esperará Jet antes de comprobar si su memoria caché no está actualizada con el archivo de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Recycle Long-Valued Pages<br />
(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</p></td>
<td><p>Indica si Jet debe intentar recuperar páginas BLOB de forma agresiva cuando se liberan.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Registry Path<br />
(DBPROP_JETOLEDB_REGPATH)</p></td>
<td><p>Indica la clave de Registro de Windows que contiene valores para el motor de base de datos Jet.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Reset ISAM Stats<br />
(DBPROP_JETOLEDB_RESETISAMSTATS)</p></td>
<td><p>Indica si el esquema DBSCHEMA_JETOLEDB_ISAMSTATS de <strong>Recordset</strong> debe restablecer sus contadores de rendimiento tras devolver información de rendimiento.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Shared Async Delay<br />
(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</p></td>
<td><p>Indica la cantidad de tiempo máxima, en milisegundos, que Jet puede retardar las escrituras asincrónicas en el disco cuando la base de datos está abierta en modo multiusuario.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:System Database<br />
(DBPROP_JETOLEDB_SYSDBPATH)</p></td>
<td><p>Indica la ruta de acceso y el nombre de archivo del archivo de información de grupo de trabajo (base de datos del sistema).</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Transaction Commit Mode<br />
(DBPROP_JETOLEDB_TXNCOMMITMODE)</p></td>
<td><p>Indica si Jet escribe los datos en el disco de forma sincrónica o asincrónica cuando se confirma una transacción.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:User Commit Sync<br />
(DBPROP_JETOLEDB_USERCOMMITSYNC)</p></td>
<td><p>Indica si los cambios realizados en transacciones se escriben en modo sincrónico o asincrónico.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Propiedades Recordset y Command específicas del proveedor

El proveedor de Jet también admite varias propiedades **Recordset** y **Command** específicas del proveedor. A estas propiedades se obtiene acceso desde la colección **Properties** de los objetos **Recordset** o **Command**, donde también se establecen. En la tabla aparece el nombre de la propiedad ADO y el nombre de la propiedad de OLE DB correspondiente entre paréntesis.

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
<td><p>Jet OLEDB: BULK Transactions<br />
(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</p></td>
<td><p>Indica si se negocian operaciones masivas de SQL. Las operaciones masivas grandes podrían producir un error al negociarse debido a retrasos de los recursos.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Enable Fat Cursors<br />
(DBPROP_JETOLEDB_ENABLEFATCURSOR)</p></td>
<td><p>Indica si Jet debe guardar en caché varias filas al rellenar un conjunto de registros para orígenes de filas remotos.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: FAT Cursor Cache Size<br />
(DBPROP_JETOLEDB_FATCURSORMAXROWS)</p></td>
<td><p>Indica el número de filas que se deben almacenar en caché cuando se utiliza almacenamiento remoto en caché de filas del almacén de datos. Este valor se omite a menos que <strong>Jet OLEDB:Enable Fat Cursors</strong> sea True.  </p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: incoherente<br />
(DBPROP_JETOLEDB_INCONSISTENT)</p></td>
<td><p>Indica si los resultados de una consulta permiten actualizaciones incoherentes.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Locking Granularity<br />
(DBPROP_JETOLEDB_LOCKGRANULARITY)</p></td>
<td><p>Indica si se abre una tabla mediante bloqueo de fila.</p></td>
</tr>
<tr class="even">
<td><p>Instrucción de paso a través de Jet OLEDB: ODBC<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</p></td>
<td><p>Indica que Jet debe pasar el texto SQL inalterado de un objeto <strong>Command</strong> al servidor.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Partial Bulk Ops<br />
(DBPROP_JETOLEDB_BULKPARTIAL)</p></td>
<td><p>Indica el comportamiento de Jet cuando se produce un error en las operaciones DML SQL.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Pass a través de Query Bulk-Op<br />
(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</p></td>
<td><p>Indica si las consultas que no devuelven un objeto <strong>Recordset</strong> se pasan inalteradas al origen de datos.</p></td>
</tr>
<tr class="odd">
<td><p>Cadena de conexión de Jet OLEDB: Pass a través de consulta<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</p></td>
<td><p>Indica la cadena de conexión de Jet utilizada para conectarse a un almacén de datos remoto. Este valor se omite a menos que <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> sea True.  </p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Stored Query<br />
(DBPROP_JETOLEDB_STOREDQUERY)</p></td>
<td><p>Indica si el texto del comando se debe interpretar como una consulta almacenada en lugar de un comando SQL.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Validate Rules On Set<br />
(DBPROP_JETOLEDB_VALIDATEONSET)</p></td>
<td><p>Indica si las reglas de validación Jet se evalúan cuando los datos de columna se establecen o cuando se confirman los cambios a la base de datos.</p></td>
</tr>
</tbody>
</table>


De forma predeterminada, el Proveedor OLE DB para Microsoft Jet abre las bases de datos de Microsoft Jet en modo de lectura y escritura. Para abrir una base de datos en modo de solo lectura, establezca la propiedad [Mode](mode-property-ado.md) del objeto **Connection** ADO en **adModeRead**.

## <a name="command-object-usage"></a>Uso del objeto Command

El texto del comando del objeto [Command](command-object-ado.md) utiliza el dialecto SQL de Microsoft Jet. En el texto del comando es posible especificar consultas que devuelven filas, consultas de acciones y nombres de tabla; sin embargo, no se admiten procedimientos almacenados y por tanto no se deben especificar.

## <a name="recordset-behavior"></a>Comportamiento del objeto Recordset

El motor de bases de datos Microsoft Jet no admite cursores dinámicos. Por lo tanto, el Proveedor OLE DB para Microsoft Jet no admite el tipo de cursor **adLockDynamic**. Cuando se solicita un cursor dinámico, el proveedor devuelve un cursor estático de claves y restablece la propiedad [CursorType](cursortype-property-ado.md) para indicar el tipo de objeto [Recordset](recordset-object-ado.md) devuelto. Además, si se solicita un objeto **Recordset** actualizable (**LockType** es **adLockOptimistic**, **adLockBatchOptimistic** o **adLockPessimistic**), el proveedor también devolverá un cursor estático de claves y restablecerá la propiedad **CursorType**.

## <a name="dynamic-properties"></a>Propiedades dinámicas

El Proveedor OLE DB para Microsoft Jet inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.

Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.

## <a name="connection-dynamic-properties"></a>Propiedades dinámicas de Connection

Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad de ADO</p></th>
<th><p>Nombre de propiedad de OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Active Sessions</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Asynchable Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Asynchable Commit</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Autocommit Isolation Levels</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Catalog Location</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Catalog Term</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Column Definition</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Current Catalog</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="odd">
<td><p>Data Source</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="even">
<td><p>Data Source Name</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="odd">
<td><p>Data Source Object Threading Model</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>DBMS Name</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="odd">
<td><p>DBMS Version</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="even">
<td><p>GROUP BY Support</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Heterogeneous Table Support</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Identifier Case Sensitivity</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Isolation Levels</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="even">
<td><p>Isolation Retention</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="odd">
<td><p>Locale Identifier</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
</tr>
<tr class="even">
<td><p>Maximum Index Size</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Row Size</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="even">
<td><p>Maximum Row Size Includes BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Tables in SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Mode</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Parameter Sets</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Multiple Results</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Storage Objects</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Multi-Table Update</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>NULL Collation Order</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>NULL Concatenation Behavior</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>OLE DB Version</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="even">
<td><p>OLE Object Support</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Open Rowset Support</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="even">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="odd">
<td><p>Output Parameter Availability</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Persistent ID Type</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Prepare Abort Behavior</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Prepare Commit Behavior</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Procedure Term</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="odd">
<td><p>Provider Friendly Name</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="even">
<td><p>Provider Name</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="odd">
<td><p>Provider Version</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="even">
<td><p>Read-Only Data Source</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Conversions on Command</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Schema Term</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Schema Usage</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>SQL Support</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Structured Storage</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Subquery Support</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Table Term</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>Transaction DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>User ID</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>User Name</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
<td><p>Window Handle</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Propiedades dinámicas del objeto Recordset

Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad de ADO</p></th>
<th><p>Nombre de propiedad de OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Append-Only Rowset</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
</tr>
<tr class="odd">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarks Ordered</p></td>
<td><p>DBPROP_ORDEREDBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Cache Deferred Columns</p></td>
<td><p>DBPROP_CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Column Writable</p></td>
<td><p>DBPROP_MAYWRITECOLUMN</p></td>
</tr>
<tr class="even">
<td><p>Defer Column</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="odd">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="even">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="even">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="odd">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="even">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="odd">
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="even">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsestLocate</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>IRowsetScroll</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>IStorage</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="even">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Memory Usage</p></td>
<td><p>DBPROP_MEMORYUSAGE</p></td>
</tr>
<tr class="even">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Others' Changes Visible</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Others' Inserts Visible</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="even">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="odd">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="even">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="even">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="odd">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="even">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="even">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Propiedades dinámicas de Command

Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad de ADO</p></th>
<th><p>Nombre de propiedad de OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Append-Only Rowset</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
</tr>
<tr class="odd">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="even">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Defer Column</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
</tr>
<tr class="odd">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="even">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetScroll</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
</tr>
<tr class="even">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="odd">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="even">
<td><p>IStorage</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="odd">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
</tr>
<tr class="even">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="odd">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Lock Mode</p></td>
<td><p>DBPROP_LOCKMODE</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Others' Changes Visible</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Others' Inserts Visible</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Server Data on Insert</p></td>
<td><p>DBPROP_SERVERDATAONINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="even">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Ver también

Para detalles de implementación específicos e información funcional acerca del proveedor OLE DB para Microsoft Jet, vea el proveedor OLE DB para la documentación de Microsoft Jet en el SDK de MDAC.

