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
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="fe2d4-102">Proveedor de Microsoft OLE DB para Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="fe2d4-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="fe2d4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe2d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe2d4-104">El Proveedor OLE DB para Microsoft Jet permite que ADO obtenga acceso a bases de datos de Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="fe2d4-105">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="fe2d4-105">Connection String Parameters</span></span>

<span data-ttu-id="fe2d4-106">Para conectar con este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="fe2d4-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="fe2d4-107">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="fe2d4-108">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="fe2d4-108">Typical Connection String</span></span>

<span data-ttu-id="fe2d4-109">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="fe2d4-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="fe2d4-110">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="fe2d4-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe2d4-111">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="fe2d4-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="fe2d4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe2d4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="fe2d4-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="fe2d4-114">Especifica el Proveedor OLE DB para Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="fe2d4-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="fe2d4-116">Especifica el nombre de archivo y la ruta de acceso a la base de datos (por ejemplo, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="fe2d4-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="fe2d4-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="fe2d4-118">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-118">Specifies the user name.</span></span> <span data-ttu-id="fe2d4-119">Si no se especifica esta palabra clave, la cadena &quot;administración&quot;, se usa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="fe2d4-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="fe2d4-121">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-121">Specifies the user password.</span></span> <span data-ttu-id="fe2d4-122">Si no se especifica esta palabra clave, una cadena vacía (&quot;&quot;), se usa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="fe2d4-123">Parámetros de conexión específicos del proveedor</span><span class="sxs-lookup"><span data-stu-id="fe2d4-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="fe2d4-p103">El Proveedor OLE DB para Microsoft Jet admite varias propiedades dinámicas específicas del proveedor además de las definidas por ADO. Al igual que ocurre con el resto de parámetros **Connection**, se pueden establecer mediante la colección **Properties** del objeto **Connection** o como parte de la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p103">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO. As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="fe2d4-126">En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe2d4-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fe2d4-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="fe2d4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe2d4-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-129">Cantidad de espacio recuperado de Jet OLEDB</span><span class="sxs-lookup"><span data-stu-id="fe2d4-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="fe2d4-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p104">Indica una estimación de la cantidad de espacio, en bytes, que se puede recuperar al compactar la base de datos. Este valor sólo es válido después de haber establecido una conexión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-133">Jet OLEDB: Connection Control</span><span class="sxs-lookup"><span data-stu-id="fe2d4-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="fe2d4-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-135">Indica si los usuarios se pueden conectar a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-136">Jet OLEDB: crear base de datos del sistema</span><span class="sxs-lookup"><span data-stu-id="fe2d4-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="fe2d4-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-138">Indica si se debe crear una base de datos del sistema al crear un nuevo origen de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-139">Jet OLEDB: Database Locking Mode</span><span class="sxs-lookup"><span data-stu-id="fe2d4-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="fe2d4-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p105">Indica el modo de bloqueo de esta base de datos. El primer usuario que la abre determina el modo que se utilizará mientras la base de datos esté abierta.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p105">Indicates the locking mode for this database. The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="fe2d4-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="fe2d4-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-145">Indica la contraseña de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="fe2d4-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="fe2d4-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-148">Indica si Jet debe copiar información de configuración regional al compactar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="fe2d4-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="fe2d4-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p106">Indica si una base de datos compactada debe ser cifrada. Si esta propiedad no está establecida, la base de datos compactada se cifrará si la base de datos original también estaba cifrada.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="fe2d4-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="fe2d4-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-155">Indica el motor de almacenamiento utilizado para obtener acceso al almacén de datos actual.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="fe2d4-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="fe2d4-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p107">Indica la longitud máxima de tiempo, en milisegundos, que Jet puede retrasar las escrituras asincrónicas en el disco cuando se abre la base de datos de forma exclusiva. Esta propiedad se omite a menos que <strong>Jet OLEDB:Flush Transaction Timeout</strong> esté establecido en 0.  </span><span class="sxs-lookup"><span data-stu-id="fe2d4-p107">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively. This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="fe2d4-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="fe2d4-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p108">Indica la cantidad de tiempo que se debe esperar antes de que los datos almacenados en una memoria caché en espera de escritura asincrónica se escriban realmente en el disco. Este valor sobrescribe a los valores de <strong>Jet OLEDB:Shared Async Delay</strong> y <strong>Jet OLEDB:Exclusive Async Delay</strong>.  </span><span class="sxs-lookup"><span data-stu-id="fe2d4-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-164">Jet OLEDB: Global Bulk Transactions</span><span class="sxs-lookup"><span data-stu-id="fe2d4-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="fe2d4-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-166">Indica si se negocian transacciones masivas SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-167">Jet OLEDB: Global Partial Bulk Ops</span><span class="sxs-lookup"><span data-stu-id="fe2d4-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="fe2d4-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-169">Indica la contraseña que se utiliza para abrir la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="fe2d4-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="fe2d4-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-172">Indica si los cambios realizados en transacciones implícitas internas se escriben en modo sincrónico o asincrónico.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="fe2d4-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="fe2d4-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-175">Indica el número de milisegundos que se debe esperar antes de intentar conseguir un bloqueo después de que un intento anterior diera lugar a un error.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="fe2d4-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="fe2d4-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-178">Indica cuántas veces se repite un intento de acceso a una página bloqueada.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="fe2d4-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="fe2d4-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-181">Indica la cantidad máxima de memoria, en kilobytes, que Jet puede utilizar antes de comenzar a volcar cambios al disco.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="fe2d4-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="fe2d4-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p109">Indica el número máximo de bloqueos que puede colocar Jet en una base de datos. El valor predeterminado es 9500.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p109">Indicates the maximum number of locks Jet can place on a database. The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-186">Jet OLEDB: contraseña de base de datos nueva</span><span class="sxs-lookup"><span data-stu-id="fe2d4-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="fe2d4-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p110">Indica la nueva contraseña que se debe establecer para esta base de datos. La contraseña antigua se almacena en <strong>Jet OLEDB:Database Password</strong>.  </span><span class="sxs-lookup"><span data-stu-id="fe2d4-p110">Indicates the new password to be set for this database. The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-190">Jet OLEDB: ODBC Command Time Out</span><span class="sxs-lookup"><span data-stu-id="fe2d4-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="fe2d4-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-192">Indica el número de milisegundos que transcurren antes de que una consulta remota ODBC de Jet supere el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-193">Jet OLEDB: Page bloqueos a bloqueo de tabla</span><span class="sxs-lookup"><span data-stu-id="fe2d4-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="fe2d4-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p111">Indica cuántas páginas deben ser bloqueadas en una transacción antes de que Jet intente promover el bloqueo a un bloqueo de tabla. Si este valor es 0, el bloqueo no se promueve nunca.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="fe2d4-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="fe2d4-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-199">Indica el número de milisegundos que esperará Jet antes de comprobar si su memoria caché no está actualizada con el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="fe2d4-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="fe2d4-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-202">Indica si Jet debe intentar recuperar páginas BLOB de forma agresiva cuando se liberan.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="fe2d4-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="fe2d4-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-205">Indica la clave de Registro de Windows que contiene valores para el motor de base de datos Jet.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-206">Jet OLEDB: Reset ISAM Stats</span><span class="sxs-lookup"><span data-stu-id="fe2d4-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="fe2d4-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-208">Indica si el esquema DBSCHEMA_JETOLEDB_ISAMSTATS de <strong>Recordset</strong> debe restablecer sus contadores de rendimiento tras devolver información de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="fe2d4-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="fe2d4-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-211">Indica la cantidad de tiempo máxima, en milisegundos, que Jet puede retardar las escrituras asincrónicas en el disco cuando la base de datos está abierta en modo multiusuario.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="fe2d4-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="fe2d4-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-214">Indica la ruta de acceso y el nombre de archivo del archivo de información de grupo de trabajo (base de datos del sistema).</span><span class="sxs-lookup"><span data-stu-id="fe2d4-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-215">Jet OLEDB: Transaction Commit Mode</span><span class="sxs-lookup"><span data-stu-id="fe2d4-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="fe2d4-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-217">Indica si Jet escribe los datos en el disco de forma sincrónica o asincrónica cuando se confirma una transacción.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="fe2d4-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="fe2d4-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-220">Indica si los cambios realizados en transacciones se escriben en modo sincrónico o asincrónico.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="fe2d4-221">Propiedades Recordset y Command específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="fe2d4-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="fe2d4-p112">El proveedor de Jet también admite varias propiedades **Recordset** y **Command** específicas del proveedor. A estas propiedades se obtiene acceso desde la colección **Properties** de los objetos **Recordset** o **Command**, donde también se establecen. En la tabla aparece el nombre de la propiedad ADO y el nombre de la propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe2d4-225">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="fe2d4-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="fe2d4-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe2d4-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-227">Jet OLEDB: BULK Transactions</span><span class="sxs-lookup"><span data-stu-id="fe2d4-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="fe2d4-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p113">Indica si se negocian operaciones masivas de SQL. Las operaciones masivas grandes podrían producir un error al negociarse debido a retrasos de los recursos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p113">Indicates whether SQL bulk operations are transacted. Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-231">Jet OLEDB: Enable Fat Cursors</span><span class="sxs-lookup"><span data-stu-id="fe2d4-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="fe2d4-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-233">Indica si Jet debe guardar en caché varias filas al rellenar un conjunto de registros para orígenes de filas remotos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-234">Jet OLEDB: FAT Cursor Cache Size</span><span class="sxs-lookup"><span data-stu-id="fe2d4-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="fe2d4-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p114">Indica el número de filas que se deben almacenar en caché cuando se utiliza almacenamiento remoto en caché de filas del almacén de datos. Este valor se omite a menos que <strong>Jet OLEDB:Enable Fat Cursors</strong> sea True.  </span><span class="sxs-lookup"><span data-stu-id="fe2d4-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-238">Jet OLEDB: incoherente</span><span class="sxs-lookup"><span data-stu-id="fe2d4-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="fe2d4-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-240">Indica si los resultados de una consulta permiten actualizaciones incoherentes.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-241">Jet OLEDB: Locking Granularity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="fe2d4-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-243">Indica si se abre una tabla mediante bloqueo de fila.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-244">Instrucción de paso a través de Jet OLEDB: ODBC</span><span class="sxs-lookup"><span data-stu-id="fe2d4-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="fe2d4-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-246">Indica que Jet debe pasar el texto SQL inalterado de un objeto <strong>Command</strong> al servidor.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-247">Jet OLEDB: Partial Bulk Ops</span><span class="sxs-lookup"><span data-stu-id="fe2d4-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="fe2d4-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-249">Indica el comportamiento de Jet cuando se produce un error en las operaciones DML SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-250">Jet OLEDB: Pass a través de Query Bulk-Op</span><span class="sxs-lookup"><span data-stu-id="fe2d4-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="fe2d4-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-252">Indica si las consultas que no devuelven un objeto <strong>Recordset</strong> se pasan inalteradas al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-253">Cadena de conexión de Jet OLEDB: Pass a través de consulta</span><span class="sxs-lookup"><span data-stu-id="fe2d4-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="fe2d4-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-p115">Indica la cadena de conexión de Jet utilizada para conectarse a un almacén de datos remoto. Este valor se omite a menos que <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> sea True.  </span><span class="sxs-lookup"><span data-stu-id="fe2d4-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-257">Jet OLEDB: Stored Query</span><span class="sxs-lookup"><span data-stu-id="fe2d4-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="fe2d4-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-259">Indica si el texto del comando se debe interpretar como una consulta almacenada en lugar de un comando SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-260">Jet OLEDB: Validate Rules On Set</span><span class="sxs-lookup"><span data-stu-id="fe2d4-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="fe2d4-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="fe2d4-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-262">Indica si las reglas de validación Jet se evalúan cuando los datos de columna se establecen o cuando se confirman los cambios a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe2d4-p116">De forma predeterminada, el Proveedor OLE DB para Microsoft Jet abre las bases de datos de Microsoft Jet en modo de lectura y escritura. Para abrir una base de datos en modo de solo lectura, establezca la propiedad [Mode](mode-property-ado.md) del objeto **Connection** ADO en **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="fe2d4-265">Uso del objeto Command</span><span class="sxs-lookup"><span data-stu-id="fe2d4-265">Command Object Usage</span></span>

<span data-ttu-id="fe2d4-p117">El texto del comando del objeto [Command](command-object-ado.md) utiliza el dialecto SQL de Microsoft Jet. En el texto del comando es posible especificar consultas que devuelven filas, consultas de acciones y nombres de tabla; sin embargo, no se admiten procedimientos almacenados y por tanto no se deben especificar.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="fe2d4-268">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-268">Recordset Behavior</span></span>

<span data-ttu-id="fe2d4-p118">El motor de bases de datos Microsoft Jet no admite cursores dinámicos. Por lo tanto, el Proveedor OLE DB para Microsoft Jet no admite el tipo de cursor **adLockDynamic**. Cuando se solicita un cursor dinámico, el proveedor devuelve un cursor estático de claves y restablece la propiedad [CursorType](cursortype-property-ado.md) para indicar el tipo de objeto [Recordset](recordset-object-ado.md) devuelto. Además, si se solicita un objeto **Recordset** actualizable (**LockType** es **adLockOptimistic**, **adLockBatchOptimistic** o **adLockPessimistic**), el proveedor también devolverá un cursor estático de claves y restablecerá la propiedad **CursorType**.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="fe2d4-273">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="fe2d4-273">Dynamic Properties</span></span>

<span data-ttu-id="fe2d4-274">El Proveedor OLE DB para Microsoft Jet inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="fe2d4-p119">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="fe2d4-279">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="fe2d4-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="fe2d4-280">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe2d4-281">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="fe2d4-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="fe2d4-282">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="fe2d4-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="fe2d4-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="fe2d4-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="fe2d4-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="fe2d4-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="fe2d4-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="fe2d4-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="fe2d4-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="fe2d4-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="fe2d4-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="fe2d4-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="fe2d4-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="fe2d4-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="fe2d4-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="fe2d4-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="fe2d4-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="fe2d4-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="fe2d4-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="fe2d4-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="fe2d4-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="fe2d4-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="fe2d4-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="fe2d4-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="fe2d4-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="fe2d4-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="fe2d4-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="fe2d4-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="fe2d4-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="fe2d4-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="fe2d4-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="fe2d4-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="fe2d4-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="fe2d4-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="fe2d4-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-329">Mode</span><span class="sxs-lookup"><span data-stu-id="fe2d4-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="fe2d4-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="fe2d4-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="fe2d4-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="fe2d4-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="fe2d4-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="fe2d4-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="fe2d4-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="fe2d4-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="fe2d4-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="fe2d4-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="fe2d4-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="fe2d4-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="fe2d4-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="fe2d4-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="fe2d4-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-355">Password</span><span class="sxs-lookup"><span data-stu-id="fe2d4-355">Password</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="fe2d4-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="fe2d4-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="fe2d4-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="fe2d4-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="fe2d4-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="fe2d4-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="fe2d4-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="fe2d4-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="fe2d4-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="fe2d4-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="fe2d4-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="fe2d4-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="fe2d4-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="fe2d4-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="fe2d4-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="fe2d4-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="fe2d4-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="fe2d4-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="fe2d4-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="fe2d4-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="fe2d4-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="fe2d4-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d4-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="fe2d4-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="fe2d4-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="fe2d4-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="fe2d4-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="fe2d4-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="fe2d4-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-391">User ID</span><span class="sxs-lookup"><span data-stu-id="fe2d4-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="fe2d4-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-393">User Name</span><span class="sxs-lookup"><span data-stu-id="fe2d4-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="fe2d4-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="fe2d4-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="fe2d4-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="fe2d4-397">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="fe2d4-398">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe2d4-399">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="fe2d4-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="fe2d4-400">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="fe2d4-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="fe2d4-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="fe2d4-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="fe2d4-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="fe2d4-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="fe2d4-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="fe2d4-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="fe2d4-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="fe2d4-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="fe2d4-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="fe2d4-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="fe2d4-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="fe2d4-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="fe2d4-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="fe2d4-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="fe2d4-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="fe2d4-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="fe2d4-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="fe2d4-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fe2d4-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fe2d4-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="fe2d4-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="fe2d4-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="fe2d4-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="fe2d4-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fe2d4-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fe2d4-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="fe2d4-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="fe2d4-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="fe2d4-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fe2d4-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fe2d4-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="fe2d4-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="fe2d4-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-466">IStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fe2d4-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="fe2d4-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="fe2d4-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="fe2d4-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="fe2d4-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="fe2d4-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="fe2d4-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="fe2d4-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="fe2d4-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="fe2d4-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="fe2d4-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="fe2d4-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="fe2d4-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="fe2d4-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="fe2d4-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="fe2d4-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="fe2d4-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="fe2d4-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="fe2d4-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fe2d4-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="fe2d4-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="fe2d4-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fe2d4-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="fe2d4-544">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="fe2d4-544">Command Dynamic Properties</span></span>

<span data-ttu-id="fe2d4-545">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe2d4-546">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="fe2d4-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="fe2d4-547">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="fe2d4-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="fe2d4-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="fe2d4-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="fe2d4-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="fe2d4-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="fe2d4-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="fe2d4-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="fe2d4-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="fe2d4-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="fe2d4-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="fe2d4-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="fe2d4-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="fe2d4-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="fe2d4-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fe2d4-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fe2d4-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="fe2d4-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="fe2d4-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="fe2d4-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="fe2d4-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="fe2d4-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fe2d4-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fe2d4-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="fe2d4-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="fe2d4-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="fe2d4-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fe2d4-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fe2d4-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fe2d4-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="fe2d4-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="fe2d4-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-607">IStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="fe2d4-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fe2d4-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="fe2d4-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="fe2d4-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="fe2d4-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="fe2d4-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fe2d4-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="fe2d4-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="fe2d4-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="fe2d4-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="fe2d4-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="fe2d4-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="fe2d4-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="fe2d4-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="fe2d4-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="fe2d4-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="fe2d4-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="fe2d4-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="fe2d4-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="fe2d4-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="fe2d4-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="fe2d4-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="fe2d4-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="fe2d4-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="fe2d4-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="fe2d4-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fe2d4-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="fe2d4-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="fe2d4-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2d4-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="fe2d4-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="fe2d4-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2d4-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fe2d4-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fe2d4-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fe2d4-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="fe2d4-687">Ver también</span><span class="sxs-lookup"><span data-stu-id="fe2d4-687">See also</span></span>

<span data-ttu-id="fe2d4-688">Para detalles de implementación específicos e información funcional acerca del proveedor OLE DB para Microsoft Jet, vea el proveedor OLE DB para la documentación de Microsoft Jet en el SDK de MDAC.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

