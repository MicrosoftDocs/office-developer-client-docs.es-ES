---
title: Proveedor de Microsoft OLE DB para SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f999f9268511fd23f1fc6a20c8459d11345ceb4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484348"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="99f3e-102">Proveedor de Microsoft OLE DB para SQL Server</span><span class="sxs-lookup"><span data-stu-id="99f3e-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="99f3e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="99f3e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="99f3e-104">El Proveedor de Microsoft OLE DB para SQL Server, SQLOLEDB, permite que ADO obtenga acceso a Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="99f3e-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="99f3e-105">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="99f3e-105">Connection String Parameters</span></span>

<span data-ttu-id="99f3e-106">Para conectar con este proveedor, establezca el argumento *Provider* en la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="99f3e-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="99f3e-107">Este valor también puede establecerse o leerse mediante la propiedad [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="99f3e-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="99f3e-108">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="99f3e-108">Typical Connection String</span></span>

<span data-ttu-id="99f3e-109">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="99f3e-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="99f3e-110">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="99f3e-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f3e-111">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="99f3e-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="99f3e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="99f3e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="99f3e-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="99f3e-114">Especifica el Proveedor OLE DB para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="99f3e-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-115"><strong>Data Source</strong> o <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="99f3e-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="99f3e-116">Especifica el nombre de un servidor.</span><span class="sxs-lookup"><span data-stu-id="99f3e-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-117"><strong>Initial Catalog</strong> o <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="99f3e-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="99f3e-118">Especifica el nombre de una base de datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="99f3e-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-119"><strong>User ID</strong> o <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="99f3e-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="99f3e-120">Especifica el nombre de usuario (para autenticación de SQL Server).</span><span class="sxs-lookup"><span data-stu-id="99f3e-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-121"><strong>Password</strong> o <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="99f3e-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="99f3e-122">Especifica la contraseña de usuario (para autenticación de SQL Server).</span><span class="sxs-lookup"><span data-stu-id="99f3e-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="99f3e-123">Parámetros de conexión específicos del proveedor</span><span class="sxs-lookup"><span data-stu-id="99f3e-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="99f3e-p101">El proveedor admite varios parámetros de conexión específicos del proveedor además de los definidos por ADO. Al igual que las propiedades de conexión ADO, estas propiedades específicas del proveedor se pueden establecer mediante la colección [Properties](properties-collection-ado.md) de un objeto [Connection](connection-object-ado.md) o como parte de **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f3e-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="99f3e-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="99f3e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="99f3e-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="99f3e-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="99f3e-p102">Indica el modo de autenticación del usuario. Puede establecerse en <strong>Yes</strong> o <strong>No</strong>. El valor predeterminado es <strong>No</strong>. Si esta propiedad se establece en <strong>Yes</strong>, SQLOLEDB utiliza el modo de autenticación de Microsoft Windows NT para autorizar el acceso del usuario a la base de datos de SQL Server especificada por los valores de las propiedades <strong>Location</strong> y <a href="datasource-property-ado.md">Datasource</a>. Si esta propiedad se establece en <strong>No</strong>, SQLOLEDB utiliza un modo mixto para autorizar el acceso del usuario a la base de datos de SQL Server. El inicio de sesión y la contraseña de SQL Server se especifican en las propiedades <strong>User ID</strong> y <strong>Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="99f3e-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="99f3e-p103">Indica un nombre de idioma de SQL Server. Identifica el idioma utilizado para la selección de mensajes del sistema y el formato. El idioma debe estar instalado en el servidor SQL Server, de lo contrario, se producirá un error al establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="99f3e-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="99f3e-140">Indica la dirección de red del servidor SQL Server especificado mediante la propiedad <strong>Location</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f3e-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="99f3e-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="99f3e-142">Indica el nombre de la biblioteca de red (bibliotecas de vínculos dinámicos) utilizado para comunicar con el servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="99f3e-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="99f3e-143">El nombre no debe incluir la ruta de acceso o la extensión de nombre de archivo .dll.</span><span class="sxs-lookup"><span data-stu-id="99f3e-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="99f3e-144">El valor predeterminado es proporcionado por la configuración de cliente de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="99f3e-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="99f3e-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="99f3e-146">Determina si SQL Server crea procedimientos almacenados temporales cuando se preparan los comandos (por parte de la propiedad <strong>Prepared</strong>).</span><span class="sxs-lookup"><span data-stu-id="99f3e-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="99f3e-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="99f3e-p105">Indica si se convierten los caracteres OEM/ANSI. Esta propiedad se puede establecer en <strong>True</strong> o <strong>False</strong>. El valor predeterminado es <strong>True</strong>. Si esta propiedad se establece en <strong>True</strong>, SQLOLEDB realiza la conversión de caracteres OEM/ANSI cuando se recuperan las cadenas de caracteres de varios bytes del servidor SQL Server o se envían a éste. Si la propiedad se establece en <strong>False</strong>, SQLOLEDB no realiza la conversión de caracteres OEM/ANSI en los datos de las cadenas de caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="99f3e-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="99f3e-p106">Indica un tamaño de paquete de red en bytes. El valor de esta propiedad debe estar entre 512 y 32767. El tamaño predeterminado del paquete de red SQLOLEDB es 4096.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="99f3e-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="99f3e-158">Indica el nombre de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="99f3e-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="99f3e-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="99f3e-160">Una cadena que identifica a la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="99f3e-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="99f3e-161">Uso del objeto Command</span><span class="sxs-lookup"><span data-stu-id="99f3e-161">Command Object Usage</span></span>

<span data-ttu-id="99f3e-p107">SQLOLEDB acepta una mezcla de ODBC, ANSI y Transact-SQL específico de SQL Server como sintaxis válida. Por ejemplo, en la siguiente instrucción SQL se usa una secuencia de escape de SQL ODBC para especificar la función de cadena LCASE:</span><span class="sxs-lookup"><span data-stu-id="99f3e-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="99f3e-p108">LCASE devuelve una cadena de caracteres convirtiendo todos los caracteres en mayúscula a sus equivalentes en minúscula. La función de cadena SQL ANSI LOWER realiza la misma operación, así que la siguiente instrucción SQL es un equivalente ANSI de la instrucción ODBC mostrada arriba:</span><span class="sxs-lookup"><span data-stu-id="99f3e-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="99f3e-166">SQLOLEDB procesa correctamente cualquier forma de la instrucción cuando se especifica como texto de un comando.</span><span class="sxs-lookup"><span data-stu-id="99f3e-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="99f3e-167">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="99f3e-167">Stored Procedures</span></span>

<span data-ttu-id="99f3e-p109">Cuando ejecute un procedimiento almacenado de SQL Server mediante un comando SQLOLEDB, utilice la secuencia de escape de llamada al procedimiento ODBC en el texto del comando. SQLOLEDB utiliza el mecanismo de llamada al procedimiento remoto de SQL Server para optimizar el procesamiento del comando. Por ejemplo, la siguiente instrucción SQL ODBC es el texto de comando que se prefiere sobre el formato Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="99f3e-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="99f3e-171">SQL ODBC</span><span class="sxs-lookup"><span data-stu-id="99f3e-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="99f3e-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="99f3e-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="99f3e-173">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="99f3e-173">Recordset Behavior</span></span>

<span data-ttu-id="99f3e-p110">SQLOLEDB no puede usar cursores de SQL Server para admitir la variedad de resultados generados por los diversos comandos. Si un usuario solicita un conjunto de registros que necesita compatibilidad con los cursores de SQL Server, se produce un error si el texto del comando utilizado genera más de un único conjunto de registros como resultado.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="99f3e-p111">Los conjuntos de registros SQLOLEDB desplazables son admitidos por los cursores de SQL Server. SQL Server impone limitaciones sobre los cursores sensibles a los cambios realizados por otros usuarios de la base de datos. Específicamente, no es posible ordenar las filas de algunos cursores y se puede producir un error cuando se intenta crear un conjunto de registros mediante un comando que contiene una cláusula ORDER BY de SQL.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="99f3e-179">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="99f3e-179">Dynamic Properties</span></span>

<span data-ttu-id="99f3e-180">El Proveedor de Microsoft OLE DB para SQL Server inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="99f3e-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="99f3e-p112">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="99f3e-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="99f3e-185">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="99f3e-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="99f3e-186">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="99f3e-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f3e-187">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="99f3e-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="99f3e-188">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="99f3e-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="99f3e-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="99f3e-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="99f3e-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="99f3e-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="99f3e-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="99f3e-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="99f3e-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="99f3e-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="99f3e-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="99f3e-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="99f3e-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="99f3e-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="99f3e-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="99f3e-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="99f3e-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="99f3e-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="99f3e-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="99f3e-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="99f3e-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="99f3e-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="99f3e-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="99f3e-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="99f3e-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="99f3e-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="99f3e-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="99f3e-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="99f3e-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="99f3e-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="99f3e-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="99f3e-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="99f3e-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="99f3e-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="99f3e-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="99f3e-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="99f3e-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="99f3e-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="99f3e-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="99f3e-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="99f3e-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="99f3e-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="99f3e-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="99f3e-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="99f3e-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="99f3e-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="99f3e-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="99f3e-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="99f3e-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="99f3e-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="99f3e-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="99f3e-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="99f3e-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="99f3e-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="99f3e-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="99f3e-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="99f3e-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="99f3e-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="99f3e-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="99f3e-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="99f3e-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="99f3e-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="99f3e-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="99f3e-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="99f3e-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="99f3e-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="99f3e-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="99f3e-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="99f3e-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="99f3e-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="99f3e-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="99f3e-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="99f3e-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="99f3e-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="99f3e-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="99f3e-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="99f3e-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="99f3e-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="99f3e-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="99f3e-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="99f3e-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="99f3e-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="99f3e-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="99f3e-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="99f3e-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="99f3e-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="99f3e-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="99f3e-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="99f3e-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="99f3e-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="99f3e-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="99f3e-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="99f3e-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="99f3e-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="99f3e-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="99f3e-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="99f3e-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="99f3e-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="99f3e-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="99f3e-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="99f3e-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="99f3e-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="99f3e-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="99f3e-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="99f3e-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="99f3e-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="99f3e-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="99f3e-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="99f3e-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="99f3e-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="99f3e-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-265">Password</span><span class="sxs-lookup"><span data-stu-id="99f3e-265">Password</span></span></p></td>
<td><p><span data-ttu-id="99f3e-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="99f3e-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="99f3e-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="99f3e-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="99f3e-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="99f3e-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="99f3e-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="99f3e-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="99f3e-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="99f3e-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="99f3e-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="99f3e-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="99f3e-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="99f3e-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="99f3e-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="99f3e-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="99f3e-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="99f3e-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="99f3e-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="99f3e-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="99f3e-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="99f3e-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="99f3e-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="99f3e-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="99f3e-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="99f3e-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="99f3e-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="99f3e-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="99f3e-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="99f3e-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="99f3e-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="99f3e-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="99f3e-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="99f3e-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="99f3e-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="99f3e-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="99f3e-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="99f3e-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="99f3e-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="99f3e-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="99f3e-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="99f3e-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="99f3e-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="99f3e-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="99f3e-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="99f3e-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="99f3e-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="99f3e-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="99f3e-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="99f3e-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="99f3e-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="99f3e-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="99f3e-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="99f3e-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-303">User ID</span><span class="sxs-lookup"><span data-stu-id="99f3e-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="99f3e-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="99f3e-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-305">User Name</span><span class="sxs-lookup"><span data-stu-id="99f3e-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="99f3e-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="99f3e-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="99f3e-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="99f3e-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="99f3e-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="99f3e-309">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="99f3e-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="99f3e-310">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="99f3e-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f3e-311">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="99f3e-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="99f3e-312">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="99f3e-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="99f3e-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="99f3e-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="99f3e-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="99f3e-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="99f3e-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="99f3e-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="99f3e-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="99f3e-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="99f3e-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="99f3e-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="99f3e-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="99f3e-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="99f3e-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="99f3e-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="99f3e-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="99f3e-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="99f3e-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="99f3e-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="99f3e-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="99f3e-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="99f3e-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="99f3e-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="99f3e-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="99f3e-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="99f3e-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="99f3e-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="99f3e-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="99f3e-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="99f3e-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="99f3e-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="99f3e-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="99f3e-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="99f3e-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="99f3e-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="99f3e-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="99f3e-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="99f3e-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="99f3e-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="99f3e-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="99f3e-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="99f3e-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="99f3e-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="99f3e-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="99f3e-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="99f3e-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="99f3e-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="99f3e-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="99f3e-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="99f3e-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="99f3e-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="99f3e-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="99f3e-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="99f3e-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="99f3e-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="99f3e-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="99f3e-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="99f3e-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="99f3e-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="99f3e-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="99f3e-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="99f3e-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="99f3e-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="99f3e-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="99f3e-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="99f3e-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="99f3e-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="99f3e-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="99f3e-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="99f3e-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="99f3e-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="99f3e-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="99f3e-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="99f3e-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="99f3e-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="99f3e-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="99f3e-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="99f3e-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="99f3e-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="99f3e-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="99f3e-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="99f3e-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="99f3e-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="99f3e-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="99f3e-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="99f3e-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="99f3e-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="99f3e-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="99f3e-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="99f3e-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="99f3e-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="99f3e-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="99f3e-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="99f3e-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="99f3e-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="99f3e-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="99f3e-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="99f3e-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="99f3e-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="99f3e-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="99f3e-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="99f3e-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="99f3e-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="99f3e-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="99f3e-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="99f3e-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="99f3e-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="99f3e-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="99f3e-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="99f3e-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="99f3e-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="99f3e-444">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="99f3e-444">Command Dynamic Properties</span></span>

<span data-ttu-id="99f3e-445">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="99f3e-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f3e-446">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="99f3e-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="99f3e-447">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="99f3e-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="99f3e-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="99f3e-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="99f3e-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="99f3e-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="99f3e-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="99f3e-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="99f3e-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="99f3e-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="99f3e-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="99f3e-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="99f3e-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="99f3e-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="99f3e-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="99f3e-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="99f3e-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="99f3e-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="99f3e-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="99f3e-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="99f3e-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="99f3e-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="99f3e-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="99f3e-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="99f3e-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="99f3e-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="99f3e-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="99f3e-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="99f3e-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="99f3e-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="99f3e-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="99f3e-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="99f3e-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="99f3e-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="99f3e-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="99f3e-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="99f3e-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="99f3e-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="99f3e-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="99f3e-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="99f3e-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="99f3e-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="99f3e-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="99f3e-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="99f3e-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="99f3e-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="99f3e-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="99f3e-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="99f3e-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="99f3e-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="99f3e-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="99f3e-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="99f3e-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="99f3e-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="99f3e-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="99f3e-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="99f3e-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="99f3e-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="99f3e-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="99f3e-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="99f3e-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="99f3e-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="99f3e-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="99f3e-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="99f3e-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="99f3e-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="99f3e-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="99f3e-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="99f3e-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="99f3e-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="99f3e-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="99f3e-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="99f3e-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="99f3e-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="99f3e-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="99f3e-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="99f3e-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="99f3e-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="99f3e-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="99f3e-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="99f3e-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="99f3e-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="99f3e-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="99f3e-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="99f3e-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="99f3e-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="99f3e-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="99f3e-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="99f3e-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="99f3e-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="99f3e-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="99f3e-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="99f3e-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="99f3e-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="99f3e-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="99f3e-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="99f3e-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="99f3e-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="99f3e-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="99f3e-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="99f3e-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="99f3e-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="99f3e-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="99f3e-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="99f3e-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="99f3e-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="99f3e-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="99f3e-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="99f3e-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="99f3e-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="99f3e-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="99f3e-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="99f3e-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="99f3e-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="99f3e-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="99f3e-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="99f3e-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="99f3e-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="99f3e-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="99f3e-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="99f3e-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="99f3e-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="99f3e-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="99f3e-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="99f3e-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="99f3e-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="99f3e-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="99f3e-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="99f3e-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="99f3e-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="99f3e-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="99f3e-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="99f3e-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="99f3e-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="99f3e-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="99f3e-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="99f3e-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="99f3e-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="99f3e-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="99f3e-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="99f3e-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="99f3e-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="99f3e-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="99f3e-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="99f3e-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="99f3e-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="99f3e-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="99f3e-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="99f3e-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f3e-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="99f3e-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="99f3e-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="99f3e-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f3e-594">XSL</span><span class="sxs-lookup"><span data-stu-id="99f3e-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="99f3e-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="99f3e-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="99f3e-596">Para obtener detalles específicos sobre la implementación e información funcional acerca de Proveedor de Microsoft OLE DB para SQL Server, vea la documentación del Proveedor OLE DB para SQL Server de la sección OLE DB del paquete MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="99f3e-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

