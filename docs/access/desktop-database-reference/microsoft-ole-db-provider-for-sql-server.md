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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288893"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="a38ec-102">Proveedor de Microsoft OLE DB para SQL Server</span><span class="sxs-lookup"><span data-stu-id="a38ec-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="a38ec-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a38ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a38ec-104">El Proveedor de Microsoft OLE DB para SQL Server, SQLOLEDB, permite que ADO obtenga acceso a Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a38ec-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="a38ec-105">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="a38ec-105">Connection String Parameters</span></span>

<span data-ttu-id="a38ec-106">Para conectarse a este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="a38ec-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="a38ec-107">Este valor también puede establecerse o leerse mediante la propiedad [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a38ec-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="a38ec-108">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="a38ec-108">Typical Connection String</span></span>

<span data-ttu-id="a38ec-109">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="a38ec-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="a38ec-110">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="a38ec-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a38ec-111">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="a38ec-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="a38ec-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a38ec-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="a38ec-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="a38ec-114">Especifica el Proveedor OLE DB para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a38ec-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-115"><strong>Data Source</strong> o <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a38ec-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a38ec-116">Especifica el nombre de un servidor.</span><span class="sxs-lookup"><span data-stu-id="a38ec-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-117"><strong>Initial Catalog</strong> o <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="a38ec-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="a38ec-118">Especifica el nombre de una base de datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="a38ec-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-119"><strong>User ID</strong> o <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="a38ec-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="a38ec-120">Especifica el nombre de usuario (para autenticación de SQL Server).</span><span class="sxs-lookup"><span data-stu-id="a38ec-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-121"><strong>Password</strong> o <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="a38ec-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="a38ec-122">Especifica la contraseña de usuario (para autenticación de SQL Server).</span><span class="sxs-lookup"><span data-stu-id="a38ec-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="a38ec-123">Parámetros de conexión específicos del proveedor</span><span class="sxs-lookup"><span data-stu-id="a38ec-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="a38ec-p101">El proveedor admite varios parámetros de conexión específicos del proveedor además de los definidos por ADO. Al igual que las propiedades de conexión ADO, estas propiedades específicas del proveedor se pueden establecer mediante la colección [Properties](properties-collection-ado.md) de un objeto [Connection](connection-object-ado.md) o como parte de **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a38ec-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a38ec-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="a38ec-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a38ec-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="a38ec-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="a38ec-p102">Indica el modo de autenticación del usuario. Puede establecerse en <strong>Yes</strong> o <strong>No</strong>. El valor predeterminado es <strong>No</strong>. Si esta propiedad se establece en <strong>Yes</strong>, SQLOLEDB utiliza el modo de autenticación de Microsoft Windows NT para autorizar el acceso del usuario a la base de datos de SQL Server especificada por los valores de las propiedades <strong>Location</strong> y <a href="datasource-property-ado.md">Datasource</a>. Si esta propiedad se establece en <strong>No</strong>, SQLOLEDB utiliza un modo mixto para autorizar el acceso del usuario a la base de datos de SQL Server. El inicio de sesión y la contraseña de SQL Server se especifican en las propiedades <strong>User ID</strong> y <strong>Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="a38ec-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="a38ec-p103">Indica un nombre de idioma de SQL Server. Identifica el idioma utilizado para la selección de mensajes del sistema y el formato. El idioma debe estar instalado en el servidor SQL Server, de lo contrario, se producirá un error al establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="a38ec-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="a38ec-140">Indica la dirección de red del servidor SQL Server especificado mediante la propiedad <strong>Location</strong>.</span><span class="sxs-lookup"><span data-stu-id="a38ec-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="a38ec-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="a38ec-142">Indica el nombre de la biblioteca de red (bibliotecas de vínculos dinámicos) usada para comunicarse con el servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a38ec-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="a38ec-143">El nombre no debe incluir la ruta de acceso ni la extensión de nombre de archivo .dll.</span><span class="sxs-lookup"><span data-stu-id="a38ec-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="a38ec-144">El valor predeterminado lo proporciona la configuración SQL Server cliente.</span><span class="sxs-lookup"><span data-stu-id="a38ec-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="a38ec-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="a38ec-146">Determina si SQL Server crea procedimientos almacenados temporales cuando se preparan los comandos (por parte de la propiedad <strong>Prepared</strong>).</span><span class="sxs-lookup"><span data-stu-id="a38ec-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="a38ec-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="a38ec-p105">Indica si se convierten los caracteres OEM/ANSI. Esta propiedad se puede establecer en <strong>True</strong> o <strong>False</strong>. El valor predeterminado es <strong>True</strong>. Si esta propiedad se establece en <strong>True</strong>, SQLOLEDB realiza la conversión de caracteres OEM/ANSI cuando se recuperan las cadenas de caracteres de varios bytes del servidor SQL Server o se envían a éste. Si la propiedad se establece en <strong>False</strong>, SQLOLEDB no realiza la conversión de caracteres OEM/ANSI en los datos de las cadenas de caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="a38ec-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="a38ec-p106">Indica un tamaño de paquete de red en bytes. El valor de esta propiedad debe estar entre 512 y 32767. El tamaño predeterminado del paquete de red SQLOLEDB es 4096.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="a38ec-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="a38ec-158">Indica el nombre de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="a38ec-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="a38ec-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="a38ec-160">Una cadena que identifica a la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a38ec-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="a38ec-161">Uso del objeto Command</span><span class="sxs-lookup"><span data-stu-id="a38ec-161">Command Object Usage</span></span>

<span data-ttu-id="a38ec-p107">SQLOLEDB acepta una mezcla de ODBC, ANSI y Transact-SQL específico de SQL Server como sintaxis válida. Por ejemplo, en la siguiente instrucción SQL se usa una secuencia de escape de SQL ODBC para especificar la función de cadena LCASE:</span><span class="sxs-lookup"><span data-stu-id="a38ec-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="a38ec-p108">LCASE devuelve una cadena de caracteres convirtiendo todos los caracteres en mayúscula a sus equivalentes en minúscula. La función de cadena SQL ANSI LOWER realiza la misma operación, así que la siguiente instrucción SQL es un equivalente ANSI de la instrucción ODBC mostrada arriba:</span><span class="sxs-lookup"><span data-stu-id="a38ec-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="a38ec-166">SQLOLEDB procesa correctamente cualquier forma de la instrucción cuando se especifica como texto de un comando.</span><span class="sxs-lookup"><span data-stu-id="a38ec-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="a38ec-167">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="a38ec-167">Stored Procedures</span></span>

<span data-ttu-id="a38ec-p109">Cuando ejecute un procedimiento almacenado de SQL Server mediante un comando SQLOLEDB, utilice la secuencia de escape de llamada al procedimiento ODBC en el texto del comando. SQLOLEDB utiliza el mecanismo de llamada al procedimiento remoto de SQL Server para optimizar el procesamiento del comando. Por ejemplo, la siguiente instrucción SQL ODBC es el texto de comando que se prefiere sobre el formato Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="a38ec-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="a38ec-171">SQL ODBC</span><span class="sxs-lookup"><span data-stu-id="a38ec-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="a38ec-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="a38ec-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="a38ec-173">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="a38ec-173">Recordset Behavior</span></span>

<span data-ttu-id="a38ec-p110">SQLOLEDB no puede usar cursores de SQL Server para admitir la variedad de resultados generados por los diversos comandos. Si un usuario solicita un conjunto de registros que necesita compatibilidad con los cursores de SQL Server, se produce un error si el texto del comando utilizado genera más de un único conjunto de registros como resultado.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="a38ec-p111">Los conjuntos de registros SQLOLEDB desplazables son admitidos por los cursores de SQL Server. SQL Server impone limitaciones sobre los cursores sensibles a los cambios realizados por otros usuarios de la base de datos. Específicamente, no es posible ordenar las filas de algunos cursores y se puede producir un error cuando se intenta crear un conjunto de registros mediante un comando que contiene una cláusula ORDER BY de SQL.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="a38ec-179">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="a38ec-179">Dynamic Properties</span></span>

<span data-ttu-id="a38ec-180">El Proveedor de Microsoft OLE DB para SQL Server inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="a38ec-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="a38ec-p112">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a38ec-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="a38ec-185">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="a38ec-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="a38ec-186">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="a38ec-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a38ec-187">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a38ec-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a38ec-188">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a38ec-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="a38ec-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="a38ec-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="a38ec-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="a38ec-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="a38ec-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="a38ec-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="a38ec-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="a38ec-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="a38ec-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a38ec-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a38ec-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a38ec-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="a38ec-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="a38ec-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="a38ec-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="a38ec-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="a38ec-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="a38ec-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="a38ec-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="a38ec-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="a38ec-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="a38ec-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="a38ec-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a38ec-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="a38ec-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="a38ec-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="a38ec-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="a38ec-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="a38ec-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="a38ec-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="a38ec-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="a38ec-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="a38ec-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="a38ec-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a38ec-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a38ec-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="a38ec-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="a38ec-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="a38ec-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="a38ec-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="a38ec-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="a38ec-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="a38ec-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="a38ec-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="a38ec-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="a38ec-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="a38ec-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="a38ec-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="a38ec-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="a38ec-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="a38ec-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="a38ec-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="a38ec-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="a38ec-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="a38ec-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="a38ec-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a38ec-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a38ec-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a38ec-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="a38ec-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="a38ec-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="a38ec-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="a38ec-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="a38ec-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="a38ec-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="a38ec-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="a38ec-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="a38ec-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="a38ec-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="a38ec-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="a38ec-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="a38ec-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="a38ec-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="a38ec-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="a38ec-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="a38ec-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="a38ec-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="a38ec-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="a38ec-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="a38ec-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="a38ec-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="a38ec-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a38ec-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a38ec-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="a38ec-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="a38ec-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="a38ec-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="a38ec-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="a38ec-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="a38ec-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="a38ec-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="a38ec-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a38ec-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="a38ec-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="a38ec-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="a38ec-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="a38ec-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="a38ec-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="a38ec-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="a38ec-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a38ec-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="a38ec-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="a38ec-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="a38ec-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="a38ec-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="a38ec-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="a38ec-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="a38ec-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="a38ec-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-265">Password</span><span class="sxs-lookup"><span data-stu-id="a38ec-265">Password</span></span></p></td>
<td><p><span data-ttu-id="a38ec-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="a38ec-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="a38ec-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="a38ec-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="a38ec-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="a38ec-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="a38ec-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="a38ec-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="a38ec-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="a38ec-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a38ec-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="a38ec-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="a38ec-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a38ec-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="a38ec-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="a38ec-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="a38ec-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="a38ec-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="a38ec-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="a38ec-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="a38ec-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="a38ec-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="a38ec-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="a38ec-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="a38ec-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="a38ec-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="a38ec-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="a38ec-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="a38ec-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="a38ec-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="a38ec-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="a38ec-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="a38ec-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="a38ec-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a38ec-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="a38ec-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="a38ec-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="a38ec-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="a38ec-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="a38ec-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="a38ec-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="a38ec-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a38ec-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="a38ec-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="a38ec-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="a38ec-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="a38ec-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="a38ec-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="a38ec-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="a38ec-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="a38ec-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="a38ec-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="a38ec-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="a38ec-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-303">User ID</span><span class="sxs-lookup"><span data-stu-id="a38ec-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="a38ec-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="a38ec-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-305">User Name</span><span class="sxs-lookup"><span data-stu-id="a38ec-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="a38ec-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="a38ec-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="a38ec-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="a38ec-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="a38ec-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="a38ec-309">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="a38ec-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="a38ec-310">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a38ec-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a38ec-311">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a38ec-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a38ec-312">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a38ec-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="a38ec-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a38ec-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a38ec-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a38ec-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a38ec-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="a38ec-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a38ec-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a38ec-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a38ec-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a38ec-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a38ec-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="a38ec-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a38ec-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a38ec-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a38ec-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="a38ec-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="a38ec-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a38ec-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="a38ec-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="a38ec-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="a38ec-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="a38ec-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a38ec-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="a38ec-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a38ec-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a38ec-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a38ec-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a38ec-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a38ec-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a38ec-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a38ec-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a38ec-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a38ec-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a38ec-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a38ec-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a38ec-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a38ec-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a38ec-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a38ec-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a38ec-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a38ec-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a38ec-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a38ec-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a38ec-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a38ec-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a38ec-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="a38ec-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a38ec-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a38ec-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="a38ec-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a38ec-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a38ec-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a38ec-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a38ec-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a38ec-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a38ec-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a38ec-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a38ec-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a38ec-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a38ec-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a38ec-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="a38ec-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="a38ec-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="a38ec-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a38ec-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a38ec-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="a38ec-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a38ec-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a38ec-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="a38ec-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a38ec-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a38ec-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="a38ec-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a38ec-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a38ec-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="a38ec-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a38ec-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a38ec-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="a38ec-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a38ec-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a38ec-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="a38ec-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a38ec-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a38ec-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="a38ec-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a38ec-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="a38ec-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a38ec-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a38ec-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a38ec-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="a38ec-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a38ec-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a38ec-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a38ec-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a38ec-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="a38ec-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a38ec-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a38ec-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="a38ec-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="a38ec-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="a38ec-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a38ec-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a38ec-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="a38ec-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="a38ec-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="a38ec-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a38ec-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a38ec-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a38ec-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a38ec-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="a38ec-444">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="a38ec-444">Command Dynamic Properties</span></span>

<span data-ttu-id="a38ec-445">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="a38ec-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a38ec-446">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a38ec-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a38ec-447">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a38ec-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="a38ec-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a38ec-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a38ec-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="a38ec-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="a38ec-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="a38ec-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a38ec-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a38ec-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="a38ec-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a38ec-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a38ec-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a38ec-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a38ec-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a38ec-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="a38ec-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a38ec-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a38ec-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a38ec-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="a38ec-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="a38ec-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="a38ec-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="a38ec-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="a38ec-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="a38ec-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="a38ec-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="a38ec-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="a38ec-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="a38ec-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="a38ec-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="a38ec-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="a38ec-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a38ec-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="a38ec-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a38ec-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a38ec-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a38ec-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a38ec-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a38ec-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a38ec-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a38ec-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a38ec-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a38ec-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a38ec-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a38ec-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a38ec-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a38ec-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a38ec-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a38ec-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a38ec-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a38ec-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a38ec-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a38ec-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a38ec-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a38ec-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a38ec-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a38ec-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a38ec-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a38ec-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="a38ec-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a38ec-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a38ec-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="a38ec-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a38ec-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a38ec-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a38ec-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a38ec-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a38ec-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a38ec-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a38ec-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a38ec-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a38ec-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a38ec-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a38ec-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a38ec-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="a38ec-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="a38ec-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="a38ec-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="a38ec-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a38ec-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="a38ec-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="a38ec-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a38ec-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a38ec-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="a38ec-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a38ec-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a38ec-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="a38ec-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="a38ec-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="a38ec-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="a38ec-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="a38ec-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="a38ec-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a38ec-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a38ec-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="a38ec-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a38ec-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a38ec-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="a38ec-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a38ec-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a38ec-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="a38ec-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a38ec-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a38ec-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="a38ec-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a38ec-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="a38ec-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a38ec-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a38ec-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="a38ec-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a38ec-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a38ec-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="a38ec-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a38ec-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a38ec-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="a38ec-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a38ec-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a38ec-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a38ec-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="a38ec-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a38ec-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a38ec-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a38ec-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a38ec-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a38ec-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="a38ec-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a38ec-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a38ec-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="a38ec-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a38ec-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a38ec-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="a38ec-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="a38ec-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="a38ec-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="a38ec-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="a38ec-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="a38ec-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a38ec-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a38ec-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="a38ec-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="a38ec-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a38ec-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="a38ec-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a38ec-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a38ec-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a38ec-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a38ec-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a38ec-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a38ec-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="a38ec-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="a38ec-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="a38ec-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a38ec-594">XSL</span><span class="sxs-lookup"><span data-stu-id="a38ec-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="a38ec-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="a38ec-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a38ec-596">Para obtener detalles específicos sobre la implementación e información funcional acerca de Proveedor de Microsoft OLE DB para SQL Server, vea la documentación del Proveedor OLE DB para SQL Server de la sección OLE DB del paquete MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="a38ec-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

