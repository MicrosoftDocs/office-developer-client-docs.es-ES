---
title: Proveedor de Microsoft OLE DB para SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4faa664ed9001c1c06906f58c7d873faf75a5d0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705109"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="5cbcd-102">Proveedor de Microsoft OLE DB para SQL Server</span><span class="sxs-lookup"><span data-stu-id="5cbcd-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="5cbcd-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cbcd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cbcd-104">El Proveedor de Microsoft OLE DB para SQL Server, SQLOLEDB, permite que ADO obtenga acceso a Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="5cbcd-105">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="5cbcd-105">Connection String Parameters</span></span>

<span data-ttu-id="5cbcd-106">Para conectar con este proveedor, establezca el argumento *Provider* en la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="5cbcd-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="5cbcd-107">Este valor también puede establecerse o leerse mediante la propiedad [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5cbcd-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="5cbcd-108">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="5cbcd-108">Typical Connection String</span></span>

<span data-ttu-id="5cbcd-109">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="5cbcd-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="5cbcd-110">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="5cbcd-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cbcd-111">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="5cbcd-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="5cbcd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cbcd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcd-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcd-114">Especifica el Proveedor OLE DB para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-115"><strong>Data Source</strong> o <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcd-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcd-116">Especifica el nombre de un servidor.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-117"><strong>Initial Catalog</strong> o <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcd-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcd-118">Especifica el nombre de una base de datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-119"><strong>User ID</strong> o <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcd-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcd-120">Especifica el nombre de usuario (para autenticación de SQL Server).</span><span class="sxs-lookup"><span data-stu-id="5cbcd-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-121"><strong>Password</strong> o <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcd-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcd-122">Especifica la contraseña de usuario (para autenticación de SQL Server).</span><span class="sxs-lookup"><span data-stu-id="5cbcd-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="5cbcd-123">Parámetros de conexión específicos del proveedor</span><span class="sxs-lookup"><span data-stu-id="5cbcd-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="5cbcd-p101">El proveedor admite varios parámetros de conexión específicos del proveedor además de los definidos por ADO. Al igual que las propiedades de conexión ADO, estas propiedades específicas del proveedor se pueden establecer mediante la colección [Properties](properties-collection-ado.md) de un objeto [Connection](connection-object-ado.md) o como parte de **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cbcd-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5cbcd-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="5cbcd-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cbcd-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="5cbcd-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-p102">Indica el modo de autenticación del usuario. Puede establecerse en <strong>Yes</strong> o <strong>No</strong>. El valor predeterminado es <strong>No</strong>. Si esta propiedad se establece en <strong>Yes</strong>, SQLOLEDB utiliza el modo de autenticación de Microsoft Windows NT para autorizar el acceso del usuario a la base de datos de SQL Server especificada por los valores de las propiedades <strong>Location</strong> y <a href="datasource-property-ado.md">Datasource</a>. Si esta propiedad se establece en <strong>No</strong>, SQLOLEDB utiliza un modo mixto para autorizar el acceso del usuario a la base de datos de SQL Server. El inicio de sesión y la contraseña de SQL Server se especifican en las propiedades <strong>User ID</strong> y <strong>Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="5cbcd-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-p103">Indica un nombre de idioma de SQL Server. Identifica el idioma utilizado para la selección de mensajes del sistema y el formato. El idioma debe estar instalado en el servidor SQL Server, de lo contrario, se producirá un error al establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="5cbcd-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-140">Indica la dirección de red del servidor SQL Server especificado mediante la propiedad <strong>Location</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="5cbcd-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-142">Indica el nombre de la biblioteca de red (bibliotecas de vínculos dinámicos) utilizado para comunicar con el servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="5cbcd-143">El nombre no debe incluir la ruta de acceso o la extensión de nombre de archivo .dll.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="5cbcd-144">El valor predeterminado es proporcionado por la configuración de cliente de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="5cbcd-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-146">Determina si SQL Server crea procedimientos almacenados temporales cuando se preparan los comandos (por parte de la propiedad <strong>Prepared</strong>).</span><span class="sxs-lookup"><span data-stu-id="5cbcd-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-p105">Indica si se convierten los caracteres OEM/ANSI. Esta propiedad se puede establecer en <strong>True</strong> o <strong>False</strong>. El valor predeterminado es <strong>True</strong>. Si esta propiedad se establece en <strong>True</strong>, SQLOLEDB realiza la conversión de caracteres OEM/ANSI cuando se recuperan las cadenas de caracteres de varios bytes del servidor SQL Server o se envían a éste. Si la propiedad se establece en <strong>False</strong>, SQLOLEDB no realiza la conversión de caracteres OEM/ANSI en los datos de las cadenas de caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="5cbcd-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-p106">Indica un tamaño de paquete de red en bytes. El valor de esta propiedad debe estar entre 512 y 32767. El tamaño predeterminado del paquete de red SQLOLEDB es 4096.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="5cbcd-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-158">Indica el nombre de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="5cbcd-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-160">Una cadena que identifica a la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="5cbcd-161">Uso del objeto Command</span><span class="sxs-lookup"><span data-stu-id="5cbcd-161">Command Object Usage</span></span>

<span data-ttu-id="5cbcd-p107">SQLOLEDB acepta una mezcla de ODBC, ANSI y Transact-SQL específico de SQL Server como sintaxis válida. Por ejemplo, en la siguiente instrucción SQL se usa una secuencia de escape de SQL ODBC para especificar la función de cadena LCASE:</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="5cbcd-p108">LCASE devuelve una cadena de caracteres convirtiendo todos los caracteres en mayúscula a sus equivalentes en minúscula. La función de cadena SQL ANSI LOWER realiza la misma operación, así que la siguiente instrucción SQL es un equivalente ANSI de la instrucción ODBC mostrada arriba:</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="5cbcd-166">SQLOLEDB procesa correctamente cualquier forma de la instrucción cuando se especifica como texto de un comando.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="5cbcd-167">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="5cbcd-167">Stored Procedures</span></span>

<span data-ttu-id="5cbcd-p109">Cuando ejecute un procedimiento almacenado de SQL Server mediante un comando SQLOLEDB, utilice la secuencia de escape de llamada al procedimiento ODBC en el texto del comando. SQLOLEDB utiliza el mecanismo de llamada al procedimiento remoto de SQL Server para optimizar el procesamiento del comando. Por ejemplo, la siguiente instrucción SQL ODBC es el texto de comando que se prefiere sobre el formato Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="5cbcd-171">SQL ODBC</span><span class="sxs-lookup"><span data-stu-id="5cbcd-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="5cbcd-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="5cbcd-173">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-173">Recordset Behavior</span></span>

<span data-ttu-id="5cbcd-p110">SQLOLEDB no puede usar cursores de SQL Server para admitir la variedad de resultados generados por los diversos comandos. Si un usuario solicita un conjunto de registros que necesita compatibilidad con los cursores de SQL Server, se produce un error si el texto del comando utilizado genera más de un único conjunto de registros como resultado.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="5cbcd-p111">Los conjuntos de registros SQLOLEDB desplazables son admitidos por los cursores de SQL Server. SQL Server impone limitaciones sobre los cursores sensibles a los cambios realizados por otros usuarios de la base de datos. Específicamente, no es posible ordenar las filas de algunos cursores y se puede producir un error cuando se intenta crear un conjunto de registros mediante un comando que contiene una cláusula ORDER BY de SQL.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="5cbcd-179">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="5cbcd-179">Dynamic Properties</span></span>

<span data-ttu-id="5cbcd-180">El Proveedor de Microsoft OLE DB para SQL Server inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="5cbcd-p112">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="5cbcd-185">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="5cbcd-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="5cbcd-186">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cbcd-187">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="5cbcd-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5cbcd-188">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="5cbcd-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="5cbcd-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="5cbcd-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="5cbcd-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="5cbcd-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="5cbcd-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="5cbcd-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="5cbcd-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="5cbcd-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="5cbcd-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="5cbcd-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="5cbcd-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="5cbcd-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="5cbcd-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="5cbcd-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="5cbcd-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="5cbcd-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="5cbcd-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="5cbcd-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="5cbcd-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="5cbcd-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="5cbcd-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="5cbcd-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="5cbcd-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="5cbcd-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="5cbcd-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="5cbcd-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="5cbcd-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5cbcd-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="5cbcd-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="5cbcd-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="5cbcd-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="5cbcd-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="5cbcd-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="5cbcd-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="5cbcd-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="5cbcd-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="5cbcd-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="5cbcd-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="5cbcd-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="5cbcd-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="5cbcd-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="5cbcd-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="5cbcd-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="5cbcd-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5cbcd-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="5cbcd-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="5cbcd-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="5cbcd-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="5cbcd-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="5cbcd-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="5cbcd-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="5cbcd-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-265">Password</span><span class="sxs-lookup"><span data-stu-id="5cbcd-265">Password</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="5cbcd-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="5cbcd-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="5cbcd-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="5cbcd-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="5cbcd-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5cbcd-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="5cbcd-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5cbcd-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="5cbcd-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="5cbcd-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="5cbcd-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="5cbcd-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="5cbcd-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="5cbcd-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="5cbcd-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="5cbcd-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="5cbcd-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="5cbcd-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="5cbcd-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="5cbcd-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="5cbcd-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="5cbcd-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="5cbcd-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="5cbcd-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="5cbcd-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="5cbcd-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="5cbcd-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="5cbcd-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="5cbcd-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-303">User ID</span><span class="sxs-lookup"><span data-stu-id="5cbcd-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="5cbcd-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-305">User Name</span><span class="sxs-lookup"><span data-stu-id="5cbcd-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="5cbcd-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="5cbcd-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="5cbcd-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="5cbcd-309">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="5cbcd-310">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cbcd-311">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="5cbcd-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5cbcd-312">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="5cbcd-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="5cbcd-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="5cbcd-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="5cbcd-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="5cbcd-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="5cbcd-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="5cbcd-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="5cbcd-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="5cbcd-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="5cbcd-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="5cbcd-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="5cbcd-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="5cbcd-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="5cbcd-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="5cbcd-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5cbcd-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5cbcd-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="5cbcd-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="5cbcd-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5cbcd-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5cbcd-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="5cbcd-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5cbcd-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5cbcd-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5cbcd-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5cbcd-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5cbcd-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="5cbcd-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="5cbcd-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="5cbcd-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="5cbcd-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="5cbcd-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="5cbcd-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="5cbcd-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="5cbcd-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="5cbcd-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="5cbcd-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="5cbcd-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="5cbcd-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="5cbcd-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="5cbcd-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="5cbcd-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="5cbcd-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="5cbcd-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="5cbcd-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5cbcd-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="5cbcd-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="5cbcd-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5cbcd-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="5cbcd-444">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="5cbcd-444">Command Dynamic Properties</span></span>

<span data-ttu-id="5cbcd-445">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cbcd-446">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="5cbcd-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5cbcd-447">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="5cbcd-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="5cbcd-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="5cbcd-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="5cbcd-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="5cbcd-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="5cbcd-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="5cbcd-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="5cbcd-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="5cbcd-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="5cbcd-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="5cbcd-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="5cbcd-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="5cbcd-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="5cbcd-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="5cbcd-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="5cbcd-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="5cbcd-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="5cbcd-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="5cbcd-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="5cbcd-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5cbcd-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5cbcd-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="5cbcd-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="5cbcd-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="5cbcd-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5cbcd-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5cbcd-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="5cbcd-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="5cbcd-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5cbcd-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5cbcd-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5cbcd-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5cbcd-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5cbcd-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5cbcd-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5cbcd-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="5cbcd-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="5cbcd-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="5cbcd-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="5cbcd-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="5cbcd-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="5cbcd-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="5cbcd-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="5cbcd-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="5cbcd-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="5cbcd-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="5cbcd-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="5cbcd-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="5cbcd-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="5cbcd-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="5cbcd-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="5cbcd-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="5cbcd-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="5cbcd-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="5cbcd-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="5cbcd-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="5cbcd-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="5cbcd-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="5cbcd-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="5cbcd-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="5cbcd-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="5cbcd-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="5cbcd-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="5cbcd-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5cbcd-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="5cbcd-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="5cbcd-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="5cbcd-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="5cbcd-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5cbcd-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5cbcd-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcd-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="5cbcd-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="5cbcd-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcd-594">XSL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="5cbcd-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="5cbcd-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cbcd-596">Para obtener detalles específicos sobre la implementación e información funcional acerca de Proveedor de Microsoft OLE DB para SQL Server, vea la documentación del Proveedor OLE DB para SQL Server de la sección OLE DB del paquete MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="5cbcd-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

