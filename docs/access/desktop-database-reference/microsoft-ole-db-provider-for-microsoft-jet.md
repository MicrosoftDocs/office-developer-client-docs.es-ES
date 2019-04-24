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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288928"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="1f415-102">Proveedor de Microsoft OLE DB para Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="1f415-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="1f415-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f415-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f415-104">El Proveedor OLE DB para Microsoft Jet permite que ADO obtenga acceso a bases de datos de Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="1f415-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="1f415-105">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="1f415-105">Connection String Parameters</span></span>

<span data-ttu-id="1f415-106">Para conectar con este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="1f415-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="1f415-107">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="1f415-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="1f415-108">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="1f415-108">Typical Connection String</span></span>

<span data-ttu-id="1f415-109">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="1f415-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="1f415-110">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="1f415-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f415-111">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="1f415-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="1f415-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f415-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f415-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="1f415-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="1f415-114">Especifica el Proveedor OLE DB para Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="1f415-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="1f415-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="1f415-116">Especifica el nombre de archivo y la ruta de acceso a la base de datos (por ejemplo, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="1f415-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="1f415-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="1f415-118">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="1f415-118">Specifies the user name.</span></span> <span data-ttu-id="1f415-119">Si no se especifica esta palabra clave, se utiliza &quot;de&quot;forma predeterminada la cadena admin.</span><span class="sxs-lookup"><span data-stu-id="1f415-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="1f415-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="1f415-121">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="1f415-121">Specifies the user password.</span></span> <span data-ttu-id="1f415-122">Si no se especifica esta palabra clave, se utiliza de&quot;&quot;forma predeterminada la cadena vacía ().</span><span class="sxs-lookup"><span data-stu-id="1f415-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="1f415-123">Parámetros de conexión específicos del proveedor</span><span class="sxs-lookup"><span data-stu-id="1f415-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="1f415-p103">El Proveedor OLE DB para Microsoft Jet admite varias propiedades dinámicas específicas del proveedor además de las definidas por ADO. Al igual que ocurre con el resto de parámetros **Connection**, se pueden establecer mediante la colección **Properties** del objeto **Connection** o como parte de la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="1f415-p103">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO. As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="1f415-126">En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="1f415-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f415-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f415-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="1f415-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f415-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f415-129">Jet OLEDB: Compact Reclaimed Space amount</span><span class="sxs-lookup"><span data-stu-id="1f415-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="1f415-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="1f415-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-p104">Indica una estimación de la cantidad de espacio, en bytes, que se puede recuperar al compactar la base de datos. Este valor sólo es válido después de haber establecido una conexión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-133">Jet OLEDB: Connection control</span><span class="sxs-lookup"><span data-stu-id="1f415-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="1f415-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="1f415-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="1f415-135">Indica si los usuarios se pueden conectar a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-136">Jet OLEDB: Create System Database</span><span class="sxs-lookup"><span data-stu-id="1f415-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="1f415-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="1f415-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-138">Indica si se debe crear una base de datos del sistema al crear un nuevo origen de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-139">Jet OLEDB: Database Locking Mode</span><span class="sxs-lookup"><span data-stu-id="1f415-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="1f415-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="1f415-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-141">Indica el modo de bloqueo de esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-141">Indicates the locking mode for this database.</span></span> <span data-ttu-id="1f415-142">El primer usuario que la abre determina el modo que se utilizará mientras la base de datos esté abierta.</span><span class="sxs-lookup"><span data-stu-id="1f415-142">The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="1f415-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="1f415-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="1f415-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="1f415-145">Indica la contraseña de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="1f415-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="1f415-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="1f415-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-148">Indica si Jet debe copiar información de configuración regional al compactar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="1f415-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="1f415-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="1f415-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-p106">Indica si una base de datos compactada debe ser cifrada. Si esta propiedad no está establecida, la base de datos compactada se cifrará si la base de datos original también estaba cifrada.</span><span class="sxs-lookup"><span data-stu-id="1f415-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="1f415-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="1f415-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="1f415-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-155">Indica el motor de almacenamiento utilizado para obtener acceso al almacén de datos actual.</span><span class="sxs-lookup"><span data-stu-id="1f415-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="1f415-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="1f415-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="1f415-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="1f415-p107">Indica la longitud máxima de tiempo, en milisegundos, que Jet puede retrasar las escrituras asincrónicas en el disco cuando se abre la base de datos de forma exclusiva. Esta propiedad se omite a menos que <strong>Jet OLEDB:Flush Transaction Timeout</strong> esté establecido en 0.  </span><span class="sxs-lookup"><span data-stu-id="1f415-p107">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively. This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="1f415-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="1f415-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="1f415-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="1f415-p108">Indica la cantidad de tiempo que se debe esperar antes de que los datos almacenados en una memoria caché en espera de escritura asincrónica se escriban realmente en el disco. Este valor sobrescribe a los valores de <strong>Jet OLEDB:Shared Async Delay</strong> y <strong>Jet OLEDB:Exclusive Async Delay</strong>.  </span><span class="sxs-lookup"><span data-stu-id="1f415-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-164">Jet OLEDB: global bulk transActions</span><span class="sxs-lookup"><span data-stu-id="1f415-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="1f415-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="1f415-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="1f415-166">Indica si se negocian transacciones masivas SQL.</span><span class="sxs-lookup"><span data-stu-id="1f415-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-167">Jet OLEDB: global Partial bulk OPS</span><span class="sxs-lookup"><span data-stu-id="1f415-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="1f415-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="1f415-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="1f415-169">Indica la contraseña que se utiliza para abrir la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="1f415-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="1f415-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="1f415-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="1f415-172">Indica si los cambios realizados en transacciones implícitas internas se escriben en modo sincrónico o asincrónico.</span><span class="sxs-lookup"><span data-stu-id="1f415-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="1f415-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="1f415-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="1f415-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="1f415-175">Indica el número de milisegundos que se debe esperar antes de intentar conseguir un bloqueo después de que un intento anterior diera lugar a un error.</span><span class="sxs-lookup"><span data-stu-id="1f415-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="1f415-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="1f415-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="1f415-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="1f415-178">Indica cuántas veces se repite un intento de acceso a una página bloqueada.</span><span class="sxs-lookup"><span data-stu-id="1f415-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="1f415-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="1f415-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="1f415-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-181">Indica la cantidad máxima de memoria, en kilobytes, que Jet puede utilizar antes de comenzar a volcar cambios al disco.</span><span class="sxs-lookup"><span data-stu-id="1f415-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="1f415-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="1f415-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="1f415-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-184">Indica el número máximo de bloqueos que puede colocar Jet en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-184">Indicates the maximum number of locks Jet can place on a database.</span></span> <span data-ttu-id="1f415-185">El valor predeterminado es 9500.</span><span class="sxs-lookup"><span data-stu-id="1f415-185">The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-186">Jet OLEDB: New Database Password</span><span class="sxs-lookup"><span data-stu-id="1f415-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="1f415-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="1f415-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="1f415-188">Indica la nueva contraseña que se debe establecer para esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-188">Indicates the new password to be set for this database.</span></span> <span data-ttu-id="1f415-189">La contraseña antigua se almacena en <strong>Jet OLEDB:Database Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f415-189">The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-190">Jet OLEDB: ODBC Command time out</span><span class="sxs-lookup"><span data-stu-id="1f415-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="1f415-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="1f415-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="1f415-192">Indica el número de milisegundos que transcurren antes de que una consulta remota ODBC de Jet supere el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="1f415-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-193">Jet OLEDB: Page Locks to table Lock</span><span class="sxs-lookup"><span data-stu-id="1f415-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="1f415-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="1f415-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="1f415-p111">Indica cuántas páginas deben ser bloqueadas en una transacción antes de que Jet intente promover el bloqueo a un bloqueo de tabla. Si este valor es 0, el bloqueo no se promueve nunca.</span><span class="sxs-lookup"><span data-stu-id="1f415-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="1f415-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="1f415-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="1f415-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="1f415-199">Indica el número de milisegundos que esperará Jet antes de comprobar si su memoria caché no está actualizada con el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="1f415-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="1f415-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="1f415-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="1f415-202">Indica si Jet debe intentar recuperar páginas BLOB de forma agresiva cuando se liberan.</span><span class="sxs-lookup"><span data-stu-id="1f415-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="1f415-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="1f415-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="1f415-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="1f415-205">Indica la clave de Registro de Windows que contiene valores para el motor de base de datos Jet.</span><span class="sxs-lookup"><span data-stu-id="1f415-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-206">Jet OLEDB: RESET ISAM stats</span><span class="sxs-lookup"><span data-stu-id="1f415-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="1f415-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="1f415-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="1f415-208">Indica si el esquema DBSCHEMA_JETOLEDB_ISAMSTATS de <strong>Recordset</strong> debe restablecer sus contadores de rendimiento tras devolver información de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1f415-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="1f415-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="1f415-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="1f415-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="1f415-211">Indica la cantidad de tiempo máxima, en milisegundos, que Jet puede retardar las escrituras asincrónicas en el disco cuando la base de datos está abierta en modo multiusuario.</span><span class="sxs-lookup"><span data-stu-id="1f415-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="1f415-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="1f415-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="1f415-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="1f415-214">Indica la ruta de acceso y el nombre de archivo del archivo de información de grupo de trabajo (base de datos del sistema).</span><span class="sxs-lookup"><span data-stu-id="1f415-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-215">Jet OLEDB: Transaction commit Mode</span><span class="sxs-lookup"><span data-stu-id="1f415-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="1f415-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="1f415-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="1f415-217">Indica si Jet escribe los datos en el disco de forma sincrónica o asincrónica cuando se confirma una transacción.</span><span class="sxs-lookup"><span data-stu-id="1f415-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="1f415-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="1f415-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="1f415-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="1f415-220">Indica si los cambios realizados en transacciones se escriben en modo sincrónico o asincrónico.</span><span class="sxs-lookup"><span data-stu-id="1f415-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="1f415-221">Propiedades Recordset y Command específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="1f415-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="1f415-p112">El proveedor de Jet también admite varias propiedades **Recordset** y **Command** específicas del proveedor. A estas propiedades se obtiene acceso desde la colección **Properties** de los objetos **Recordset** o **Command**, donde también se establecen. En la tabla aparece el nombre de la propiedad ADO y el nombre de la propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="1f415-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f415-225">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="1f415-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f415-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f415-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f415-227">Jet OLEDB: Bulk transActions</span><span class="sxs-lookup"><span data-stu-id="1f415-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="1f415-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="1f415-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="1f415-229">Indica si se negocian operaciones masivas de SQL.</span><span class="sxs-lookup"><span data-stu-id="1f415-229">Indicates whether SQL bulk operations are transacted.</span></span> <span data-ttu-id="1f415-230">Las operaciones masivas grandes podrían producir un error al negociarse debido a retrasos de los recursos.</span><span class="sxs-lookup"><span data-stu-id="1f415-230">Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-231">Jet OLEDB: enAble FAT Cursors</span><span class="sxs-lookup"><span data-stu-id="1f415-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="1f415-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="1f415-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="1f415-233">Indica si Jet debe guardar en caché varias filas al rellenar un conjunto de registros para orígenes de filas remotos.</span><span class="sxs-lookup"><span data-stu-id="1f415-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-234">Jet OLEDB: FAT cursor cache size</span><span class="sxs-lookup"><span data-stu-id="1f415-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="1f415-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="1f415-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="1f415-p114">Indica el número de filas que se deben almacenar en caché cuando se utiliza almacenamiento remoto en caché de filas del almacén de datos. Este valor se omite a menos que <strong>Jet OLEDB:Enable Fat Cursors</strong> sea True.  </span><span class="sxs-lookup"><span data-stu-id="1f415-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-238">Jet OLEDB: incoherente</span><span class="sxs-lookup"><span data-stu-id="1f415-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="1f415-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="1f415-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="1f415-240">Indica si los resultados de una consulta permiten actualizaciones incoherentes.</span><span class="sxs-lookup"><span data-stu-id="1f415-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-241">Jet OLEDB: Locking Granularity</span><span class="sxs-lookup"><span data-stu-id="1f415-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="1f415-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="1f415-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="1f415-243">Indica si se abre una tabla mediante bloqueo de fila.</span><span class="sxs-lookup"><span data-stu-id="1f415-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-244">Jet OLEDB: ODBC pass-through Statement</span><span class="sxs-lookup"><span data-stu-id="1f415-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="1f415-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="1f415-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="1f415-246">Indica que Jet debe pasar el texto SQL inalterado de un objeto <strong>Command</strong> al servidor.</span><span class="sxs-lookup"><span data-stu-id="1f415-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-247">Jet OLEDB: Partial bulk OPS</span><span class="sxs-lookup"><span data-stu-id="1f415-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="1f415-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="1f415-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="1f415-249">Indica el comportamiento de Jet cuando se produce un error en las operaciones DML SQL.</span><span class="sxs-lookup"><span data-stu-id="1f415-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-250">Jet OLEDB: pass through Query bulk-op</span><span class="sxs-lookup"><span data-stu-id="1f415-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="1f415-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="1f415-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="1f415-252">Indica si las consultas que no devuelven un objeto <strong>Recordset</strong> se pasan inalteradas al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-253">Jet OLEDB: pass through Query Connect String</span><span class="sxs-lookup"><span data-stu-id="1f415-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="1f415-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="1f415-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="1f415-p115">Indica la cadena de conexión de Jet utilizada para conectarse a un almacén de datos remoto. Este valor se omite a menos que <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> sea True.  </span><span class="sxs-lookup"><span data-stu-id="1f415-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-257">Jet OLEDB: Stored Query</span><span class="sxs-lookup"><span data-stu-id="1f415-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="1f415-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="1f415-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="1f415-259">Indica si el texto del comando se debe interpretar como una consulta almacenada en lugar de un comando SQL.</span><span class="sxs-lookup"><span data-stu-id="1f415-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-260">Jet OLEDB: Validate rules on set</span><span class="sxs-lookup"><span data-stu-id="1f415-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="1f415-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="1f415-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="1f415-262">Indica si las reglas de validación Jet se evalúan cuando los datos de columna se establecen o cuando se confirman los cambios a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f415-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f415-p116">De forma predeterminada, el Proveedor OLE DB para Microsoft Jet abre las bases de datos de Microsoft Jet en modo de lectura y escritura. Para abrir una base de datos en modo de solo lectura, establezca la propiedad [Mode](mode-property-ado.md) del objeto **Connection** ADO en **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="1f415-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="1f415-265">Uso del objeto Command</span><span class="sxs-lookup"><span data-stu-id="1f415-265">Command Object Usage</span></span>

<span data-ttu-id="1f415-p117">El texto del comando del objeto [Command](command-object-ado.md) utiliza el dialecto SQL de Microsoft Jet. En el texto del comando es posible especificar consultas que devuelven filas, consultas de acciones y nombres de tabla; sin embargo, no se admiten procedimientos almacenados y por tanto no se deben especificar.</span><span class="sxs-lookup"><span data-stu-id="1f415-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="1f415-268">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="1f415-268">Recordset Behavior</span></span>

<span data-ttu-id="1f415-p118">El motor de bases de datos Microsoft Jet no admite cursores dinámicos. Por lo tanto, el Proveedor OLE DB para Microsoft Jet no admite el tipo de cursor **adLockDynamic**. Cuando se solicita un cursor dinámico, el proveedor devuelve un cursor estático de claves y restablece la propiedad [CursorType](cursortype-property-ado.md) para indicar el tipo de objeto [Recordset](recordset-object-ado.md) devuelto. Además, si se solicita un objeto **Recordset** actualizable (**LockType** es **adLockOptimistic**, **adLockBatchOptimistic** o **adLockPessimistic**), el proveedor también devolverá un cursor estático de claves y restablecerá la propiedad **CursorType**.</span><span class="sxs-lookup"><span data-stu-id="1f415-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="1f415-273">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="1f415-273">Dynamic Properties</span></span>

<span data-ttu-id="1f415-274">El Proveedor OLE DB para Microsoft Jet inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="1f415-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="1f415-p119">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1f415-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="1f415-279">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="1f415-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="1f415-280">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="1f415-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f415-281">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="1f415-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f415-282">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="1f415-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f415-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="1f415-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="1f415-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="1f415-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="1f415-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="1f415-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="1f415-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="1f415-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="1f415-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="1f415-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="1f415-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="1f415-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="1f415-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="1f415-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="1f415-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="1f415-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="1f415-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="1f415-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="1f415-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="1f415-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="1f415-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="1f415-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="1f415-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="1f415-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="1f415-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="1f415-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="1f415-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="1f415-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="1f415-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="1f415-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="1f415-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f415-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f415-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f415-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="1f415-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="1f415-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="1f415-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="1f415-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="1f415-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="1f415-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="1f415-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="1f415-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="1f415-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="1f415-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="1f415-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="1f415-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="1f415-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="1f415-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="1f415-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="1f415-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="1f415-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="1f415-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="1f415-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="1f415-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="1f415-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="1f415-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="1f415-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="1f415-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="1f415-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="1f415-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="1f415-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="1f415-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="1f415-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="1f415-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="1f415-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="1f415-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="1f415-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="1f415-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="1f415-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="1f415-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-329">Mode</span><span class="sxs-lookup"><span data-stu-id="1f415-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="1f415-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="1f415-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="1f415-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="1f415-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="1f415-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="1f415-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="1f415-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="1f415-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f415-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f415-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f415-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="1f415-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="1f415-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f415-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="1f415-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="1f415-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="1f415-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="1f415-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f415-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f415-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="1f415-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="1f415-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="1f415-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="1f415-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="1f415-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f415-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="1f415-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="1f415-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f415-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="1f415-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="1f415-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="1f415-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="1f415-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="1f415-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="1f415-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="1f415-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="1f415-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="1f415-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-355">Password</span><span class="sxs-lookup"><span data-stu-id="1f415-355">Password</span></span></p></td>
<td><p><span data-ttu-id="1f415-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="1f415-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="1f415-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="1f415-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="1f415-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="1f415-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f415-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f415-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="1f415-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f415-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f415-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="1f415-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="1f415-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="1f415-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="1f415-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="1f415-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="1f415-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="1f415-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="1f415-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="1f415-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="1f415-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="1f415-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="1f415-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="1f415-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="1f415-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="1f415-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="1f415-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="1f415-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="1f415-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="1f415-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="1f415-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="1f415-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="1f415-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="1f415-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="1f415-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="1f415-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="1f415-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f415-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="1f415-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="1f415-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f415-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="1f415-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="1f415-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="1f415-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="1f415-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="1f415-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="1f415-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="1f415-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="1f415-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="1f415-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="1f415-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="1f415-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="1f415-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-391">User ID</span><span class="sxs-lookup"><span data-stu-id="1f415-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="1f415-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="1f415-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-393">User Name</span><span class="sxs-lookup"><span data-stu-id="1f415-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="1f415-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="1f415-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="1f415-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="1f415-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="1f415-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="1f415-397">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="1f415-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="1f415-398">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1f415-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f415-399">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="1f415-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f415-400">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="1f415-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f415-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="1f415-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="1f415-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="1f415-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="1f415-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="1f415-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="1f415-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f415-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f415-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f415-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="1f415-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="1f415-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="1f415-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="1f415-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="1f415-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="1f415-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="1f415-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="1f415-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f415-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="1f415-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="1f415-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f415-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="1f415-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f415-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f415-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="1f415-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="1f415-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="1f415-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="1f415-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="1f415-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="1f415-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f415-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="1f415-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="1f415-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f415-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="1f415-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f415-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f415-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f415-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="1f415-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f415-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="1f415-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="1f415-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f415-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="1f415-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f415-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f415-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="1f415-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f415-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f415-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="1f415-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f415-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="1f415-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f415-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="1f415-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f415-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f415-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="1f415-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f415-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f415-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="1f415-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f415-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="1f415-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f415-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="1f415-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="1f415-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="1f415-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f415-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="1f415-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f415-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f415-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="1f415-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f415-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f415-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="1f415-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f415-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="1f415-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="1f415-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="1f415-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-466">IStream</span><span class="sxs-lookup"><span data-stu-id="1f415-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="1f415-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="1f415-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="1f415-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f415-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f415-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f415-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f415-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f415-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f415-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="1f415-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="1f415-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f415-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="1f415-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="1f415-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="1f415-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="1f415-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="1f415-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="1f415-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="1f415-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="1f415-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1f415-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="1f415-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="1f415-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f415-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="1f415-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="1f415-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f415-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="1f415-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="1f415-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="1f415-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="1f415-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="1f415-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="1f415-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="1f415-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="1f415-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="1f415-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="1f415-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="1f415-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="1f415-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="1f415-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f415-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="1f415-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f415-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f415-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="1f415-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f415-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f415-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f415-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f415-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f415-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f415-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="1f415-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="1f415-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f415-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f415-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f415-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f415-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="1f415-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f415-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f415-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f415-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="1f415-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="1f415-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="1f415-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f415-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f415-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f415-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="1f415-544">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="1f415-544">Command Dynamic Properties</span></span>

<span data-ttu-id="1f415-545">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="1f415-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f415-546">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="1f415-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f415-547">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="1f415-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f415-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="1f415-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="1f415-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="1f415-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="1f415-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="1f415-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="1f415-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f415-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f415-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f415-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="1f415-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="1f415-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="1f415-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="1f415-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="1f415-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="1f415-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="1f415-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f415-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f415-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="1f415-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="1f415-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="1f415-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f415-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="1f415-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="1f415-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f415-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="1f415-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f415-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f415-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f415-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="1f415-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f415-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="1f415-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="1f415-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f415-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="1f415-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f415-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f415-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="1f415-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f415-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f415-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="1f415-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f415-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="1f415-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="1f415-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f415-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="1f415-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f415-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f415-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="1f415-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f415-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f415-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="1f415-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f415-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="1f415-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f415-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="1f415-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f415-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="1f415-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f415-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="1f415-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f415-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f415-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="1f415-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f415-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f415-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="1f415-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f415-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="1f415-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="1f415-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="1f415-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-607">IStream</span><span class="sxs-lookup"><span data-stu-id="1f415-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="1f415-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="1f415-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="1f415-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f415-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f415-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f415-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f415-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f415-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f415-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f415-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="1f415-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="1f415-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="1f415-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="1f415-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="1f415-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="1f415-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="1f415-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="1f415-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="1f415-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="1f415-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="1f415-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="1f415-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1f415-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f415-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f415-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="1f415-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="1f415-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f415-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="1f415-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="1f415-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f415-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="1f415-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="1f415-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="1f415-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="1f415-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="1f415-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="1f415-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="1f415-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f415-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="1f415-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="1f415-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="1f415-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="1f415-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="1f415-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="1f415-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="1f415-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f415-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="1f415-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f415-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f415-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="1f415-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f415-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f415-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f415-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f415-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="1f415-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f415-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f415-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="1f415-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="1f415-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="1f415-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="1f415-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f415-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f415-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="1f415-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="1f415-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="1f415-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f415-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f415-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="1f415-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f415-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f415-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f415-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f415-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="1f415-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="1f415-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="1f415-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f415-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f415-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f415-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f415-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1f415-687">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f415-687">See also</span></span>

<span data-ttu-id="1f415-688">Para obtener detalles de implementación específicos e información sobre el funcionamiento del proveedor OLE DB para Microsoft Jet, consulte la documentación del Proveedor OLE DB para Microsoft Jet en el SDK de MDAC.</span><span class="sxs-lookup"><span data-stu-id="1f415-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

