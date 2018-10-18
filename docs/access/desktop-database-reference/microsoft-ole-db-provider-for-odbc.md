---
title: Proveedor de Microsoft OLE DB para ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0098e646ea48656f44bd3ccd380ae41efc94ffba
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606944"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="37811-102">Proveedor de Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="37811-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="37811-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37811-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37811-p101">Para un programador de ADO o RDS, un mundo ideal sería aquel en que cada origen de datos expusiera una interfaz OLE DB, de modo que ADO pudiera llamar directamente al origen de datos. Aunque cada vez más proveedores de bases de datos están implementando interfaces OLE DB, algunos orígenes de datos aún no están expuestos de esta forma. Sin embargo, es posible obtener acceso a prácticamente todos los sistemas DBMS que se usan en la actualidad a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="37811-107">Los controladores ODBC están disponibles para todos los principales DBMS que se utilizan hoy en día, incluidos Microsoft SQL Server, Microsoft Access (motor de bases de datos Microsoft Jet) y Microsoft FoxPro, además de otros productos de base de datos no pertenecientes a Microsoft, como Oracle.</span><span class="sxs-lookup"><span data-stu-id="37811-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="37811-p102">Sin embargo, el Proveedor Microsoft ODBC permite a ADO conectarse a cualquier origen de datos ODBC. El proveedor es de subprocesamiento libre y está habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="37811-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="37811-p103">El proveedor admite transacciones, aunque los diferentes motores DBMS ofrecen diferentes tipos de compatibilidad con ellas. Por ejemplo, Microsoft Access admite las transacciones anidadas de hasta cinco niveles.</span><span class="sxs-lookup"><span data-stu-id="37811-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="37811-112">Éste es el proveedor predeterminado para ADO y admite todas las propiedades y los métodos ADO dependientes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="37811-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="37811-113">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="37811-113">Connection String Parameters</span></span>

<span data-ttu-id="37811-114">Para conectar con este proveedor, establezca el argumento **Provider=** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="37811-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="37811-115">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="37811-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="37811-116">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="37811-116">Typical Connection String</span></span>

<span data-ttu-id="37811-117">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="37811-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="37811-118">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="37811-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-119">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="37811-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="37811-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="37811-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="37811-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="37811-122">Especifica el Proveedor OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="37811-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="37811-124">Especifica el nombre del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="37811-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="37811-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="37811-126">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="37811-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="37811-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="37811-128">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="37811-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="37811-129"><strong>URL</strong></span></span></p></td>
<span data-ttu-id="37811-130"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="37811-130"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="37811-131">Especifica la dirección URL de un archivo o directorio publicado en una carpeta Web.</span><span class="sxs-lookup"><span data-stu-id="37811-131">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
=======
<td><p><span data-ttu-id="37811-132">Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</span><span class="sxs-lookup"><span data-stu-id="37811-132">Specifies the URL of a file or directory published in a web folder.</span></span></p></td><span data-ttu-id="37811-133">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="37811-133">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="37811-134">Dado que éste es el proveedor predeterminado para ADO, si se omite el parámetro **Provider=** de la cadena de conexión, ADO intentará establecer una conexión con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="37811-134">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="37811-p104">El proveedor no admite ningún parámetro de conexión específico además de los definidos por ADO. No obstante, pasará cualquier parámetro de conexión que no sea de ADO al controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="37811-p105">Dado que se puede omitir el parámetro **Provider**, es posible elaborar una cadena de conexión ADO idéntica a una cadena de conexión ODBC para el mismo origen de datos. Utilice los mismos nombres de parámetro (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), los valores y la sintaxis que cuando elabora una cadena de conexión ODBC. Es posible conectar con o sin un nombre de origen de datos predefinido (DSN) o un FileDSN.</span><span class="sxs-lookup"><span data-stu-id="37811-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="37811-140">**Sintaxis con un DSN o un FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="37811-140">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="37811-141">**Sintaxis sin ningún DSN (conexión sin DSN):**</span><span class="sxs-lookup"><span data-stu-id="37811-141">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="37811-p106">Si se utiliza un **DSN** o un **FileDSN**, debe definirse mediante el Administrador de origen de datos ODBC del Panel de control de Windows. En Microsoft Windows 2000, el Administrador ODBC se encuentra en Herramientas administrativas. En versiones anteriores de Windows, el icono Administrador ODBC se denomina **ODBC de 32 bits** o simplemente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="37811-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="37811-145">Como alternativa al establecimiento de un **DSN**, puede especificar el controlador ODBC (**DRIVER=**), como "SQL Server;" el nombre del servidor (**SERVER=**); y el nombre de la base de datos (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="37811-145">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="37811-146">También puede especificar un nombre de cuenta de usuario (**UID=**) y la contraseña para esa cuenta (**PWD=**) en los parámetros específicos de ODBC o en los parámetros estándar *user* y *password* definidos por ADO.</span><span class="sxs-lookup"><span data-stu-id="37811-146">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="37811-147">Aunque una definición **DSN** ya especifica una base de datos, puede especificar *un* parámetro de *base de datos* además de un **DSN** para conectarse a una base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="37811-147">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="37811-148">Es una buena idea incluir siempre *el* parámetro de *base de datos* al utilizar un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="37811-148">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="37811-149">Eso garantizará la conexión a la base de datos adecuada en caso de que otro usuario haya modificado el parámetro desde la última vez que se comprobó la definición **DSN**.</span><span class="sxs-lookup"><span data-stu-id="37811-149">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="37811-150">Propiedades Connection específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="37811-150">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="37811-p108">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="37811-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-153">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="37811-153">Property Name</span></span></p></th>
<th><p><span data-ttu-id="37811-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="37811-154">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-155">Accessible Procedures</span><span class="sxs-lookup"><span data-stu-id="37811-155">Accessible Procedures</span></span><br />
<span data-ttu-id="37811-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="37811-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="37811-157">Indica si el usuario tiene acceso a procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="37811-157">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-158">Tablas accesibles</span><span class="sxs-lookup"><span data-stu-id="37811-158">Accessible Tables</span></span><br />
<span data-ttu-id="37811-159">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="37811-159">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="37811-160">Indica si el usuario tiene permiso para ejecutar instrucciones SELECT en las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="37811-160">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-161">Instrucciones activas</span><span class="sxs-lookup"><span data-stu-id="37811-161">Active Statements</span></span><br />
<span data-ttu-id="37811-162">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="37811-162">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="37811-163">Indica el número de controladores que puede admitir un controlador ODBC en una conexión.</span><span class="sxs-lookup"><span data-stu-id="37811-163">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-164">Nombre del controlador</span><span class="sxs-lookup"><span data-stu-id="37811-164">Driver Name</span></span><br />
<span data-ttu-id="37811-165">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="37811-165">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="37811-166">Indica el nombre de archivo del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-166">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-167">Versión del controlador ODBC</span><span class="sxs-lookup"><span data-stu-id="37811-167">Driver ODBC Version</span></span><br />
<span data-ttu-id="37811-168">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="37811-168">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="37811-169">Indica la versión de ODBC que admite este controlador.</span><span class="sxs-lookup"><span data-stu-id="37811-169">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-170">Uso de archivos</span><span class="sxs-lookup"><span data-stu-id="37811-170">File Usage</span></span><br />
<span data-ttu-id="37811-171">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="37811-171">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="37811-172">Indica cómo trata el controlador a un archivo de un origen de datos, como una tabla o como un catálogo.</span><span class="sxs-lookup"><span data-stu-id="37811-172">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-173">Al igual que la cláusula Escape</span><span class="sxs-lookup"><span data-stu-id="37811-173">Like Escape Clause</span></span><br />
<span data-ttu-id="37811-174">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="37811-174">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="37811-175">Indica si el controlador admite la definición y el uso de un carácter de escape para el carácter de porcentaje (%) y de un carácter de subrayado (_) en el predicado LIKE de una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="37811-175">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-176">Max Columns in Group By</span><span class="sxs-lookup"><span data-stu-id="37811-176">Max Columns in Group By</span></span><br />
<span data-ttu-id="37811-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="37811-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="37811-178">Indica el número máximo de columnas que se puede enumerar en la cláusula GROUP BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="37811-178">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-179">Número máximo de columnas en el índice</span><span class="sxs-lookup"><span data-stu-id="37811-179">Max Columns in Index</span></span><br />
<span data-ttu-id="37811-180">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="37811-180">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="37811-181">Indica el número máximo de columnas que puede ser incluido en un índice.</span><span class="sxs-lookup"><span data-stu-id="37811-181">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-182">Max Columns in Order By</span><span class="sxs-lookup"><span data-stu-id="37811-182">Max Columns in Order By</span></span><br />
<span data-ttu-id="37811-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="37811-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="37811-184">Indica el número máximo de columnas que se puede enumerar en la cláusula ORDER BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="37811-184">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-185">Número máximo de columnas en Seleccionar</span><span class="sxs-lookup"><span data-stu-id="37811-185">Max Columns in Select</span></span><br />
<span data-ttu-id="37811-186">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="37811-186">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="37811-187">Indica el número máximo de columnas que se puede enumerar en la parte SELECT de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="37811-187">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-188">Número máximo de columnas de tabla</span><span class="sxs-lookup"><span data-stu-id="37811-188">Max Columns in Table</span></span><br />
<span data-ttu-id="37811-189">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="37811-189">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="37811-190">Indica el número máximo de columnas permitido en una tabla.</span><span class="sxs-lookup"><span data-stu-id="37811-190">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-191">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="37811-191">Numeric Functions</span></span><br />
<span data-ttu-id="37811-192">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="37811-192">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="37811-p109">Indica las funciones numéricas admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-195">Outer Join Capabilities</span><span class="sxs-lookup"><span data-stu-id="37811-195">Outer Join Capabilities</span></span><br />
<span data-ttu-id="37811-196">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="37811-196">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="37811-197">Indica los tipos de combinaciones externas admitidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="37811-197">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-198">Combinaciones externas</span><span class="sxs-lookup"><span data-stu-id="37811-198">Outer Joins</span></span><br />
<span data-ttu-id="37811-199">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="37811-199">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="37811-200">Indica si el proveedor admite combinaciones externas.</span><span class="sxs-lookup"><span data-stu-id="37811-200">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-201">Caracteres especiales</span><span class="sxs-lookup"><span data-stu-id="37811-201">Special Characters</span></span><br />
<span data-ttu-id="37811-202">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="37811-202">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="37811-203">Indica qué caracteres tienen un significado especial para el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-203">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-204">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="37811-204">Stored Procedures</span></span><br />
<span data-ttu-id="37811-205">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="37811-205">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="37811-206">Indica si hay procedimientos almacenados disponibles para ser utilizados con este controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-206">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-207">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="37811-207">String Functions</span></span><br />
<span data-ttu-id="37811-208">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="37811-208">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="37811-p110">Indica qué funciones de cadena son admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-211">Funciones del sistema</span><span class="sxs-lookup"><span data-stu-id="37811-211">System Functions</span></span><br />
<span data-ttu-id="37811-212">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="37811-212">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="37811-p111">Indica las funciones del sistema admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-215">Funciones de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="37811-215">Time/Date Functions</span></span><br />
<span data-ttu-id="37811-216">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="37811-216">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="37811-p112">Indica las funciones de fecha y hora admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-219">Compatibilidad con la gramática SQL</span><span class="sxs-lookup"><span data-stu-id="37811-219">SQL Grammar Support</span></span><br />
<span data-ttu-id="37811-220">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="37811-220">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="37811-221">Indica la gramática SQL admitida por el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-221">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="37811-222">Propiedades Recordset y Command específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="37811-222">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="37811-p113">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección **Properties** de los objetos **Recordset** y **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="37811-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-225">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="37811-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="37811-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="37811-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-227">Query Based Updates/Deletes/Inserts</span><span class="sxs-lookup"><span data-stu-id="37811-227">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="37811-228">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="37811-228">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="37811-229">Indica si se pueden realizar actualizaciones, eliminaciones e inserciones mediante consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="37811-229">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-230">ODBC Concurrency Type</span><span class="sxs-lookup"><span data-stu-id="37811-230">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="37811-231">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="37811-231">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="37811-232">Indica el método utilizado para minimizar los problemas potenciales causados por el intento de dos usuarios de obtener acceso a los mismos datos del origen de datos de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="37811-232">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-233">Accesibilidad BLOB en el cursor de sólo avance</span><span class="sxs-lookup"><span data-stu-id="37811-233">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="37811-234">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="37811-234">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="37811-235">Indica si es posible obtener acceso a <strong>campos</strong> BLOB cuando se utiliza un cursor de sólo avance.</span><span class="sxs-lookup"><span data-stu-id="37811-235">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-236">Incluir SQL_FLOAT, SQL_DOUBLE y SQL_REAL en QBU WHERE clauses</span><span class="sxs-lookup"><span data-stu-id="37811-236">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="37811-237">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="37811-237">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="37811-238">Indica si se pueden incluir valores SQL_FLOAT, SQL_DOUBLE y SQL_REAL en una cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="37811-238">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-239">Posición en la última fila después de insertar</span><span class="sxs-lookup"><span data-stu-id="37811-239">Position on the last row after insert</span></span><br />
<span data-ttu-id="37811-240">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="37811-240">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="37811-241">Indica que tras haber insertado un nuevo registro en una tabla, la última fila de la misma se convertirá en la fila actual.</span><span class="sxs-lookup"><span data-stu-id="37811-241">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-242">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="37811-242">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="37811-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="37811-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="37811-244">Indica si la interfaz <strong>IRowsetChange</strong> admite información ampliada.</span><span class="sxs-lookup"><span data-stu-id="37811-244">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-245">Tipo de Cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="37811-245">ODBC Cursor Type</span></span><br />
<span data-ttu-id="37811-246">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="37811-246">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="37811-247">Indica el tipo de cursor usado por el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="37811-247">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-248">Generar un conjunto de filas que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="37811-248">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="37811-249">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="37811-249">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="37811-250">Indica que el controlador ODBC genera un conjunto de registros que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="37811-250">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="37811-251">Texto del comando</span><span class="sxs-lookup"><span data-stu-id="37811-251">Command Text</span></span>

<span data-ttu-id="37811-252">La forma de utilizar el objeto [Command](command-object-ado.md) depende en gran medida del origen de datos y del tipo de consulta o instrucción de comando que acepte.</span><span class="sxs-lookup"><span data-stu-id="37811-252">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="37811-253">ODBC proporciona una sintaxis específica para llamar a los procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="37811-253">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="37811-254">Para la propiedad [CommandText](commandtext-property-ado.md) de un objeto **Command** , el argumento *CommandText* del método **Execute** en un objeto [Connection](connection-object-ado.md) o el argumento *Source* en el método **Open** en un [objeto Recordset](recordset-object-ado.md) objeto, pasa en una cadena con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="37811-254">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="37811-p115">Cada **?** hace referencia a un objeto de la colección [Parameters](parameters-collection-ado.md). El primer **?** hace referencia a **Parameters**(0), el siguiente **?** a **Parameters**(1) y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="37811-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="37811-p116">Las referencias del parámetro son opcionales y dependen de la estructura del procedimiento almacenado. Si desea llamar a un procedimiento almacenado que no define parámetros, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="37811-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="37811-262">Si tiene dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="37811-262">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="37811-p117">Si el procedimiento almacenado va a devolver un valor, el valor devuelto se trata como otro parámetro. Si no dispone de parámetros de consulta pero tiene un valor devuelto, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="37811-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="37811-265">Por último, si tiene un valor devuelto y dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="37811-265">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="37811-266">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="37811-266">Recordset Behavior</span></span>

<span data-ttu-id="37811-267">En las tablas siguientes se enumeran los métodos y las propiedades ADO estándar disponibles en un objeto **Recordset** abierto con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="37811-267">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="37811-268">Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección **Properties** del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.</span><span class="sxs-lookup"><span data-stu-id="37811-268">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="37811-269">Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="37811-269">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-270">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37811-270">Property</span></span></p></th>
<th><p><span data-ttu-id="37811-271">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="37811-271">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="37811-272">Dinámico</span><span class="sxs-lookup"><span data-stu-id="37811-272">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="37811-273">Conjunto de claves</span><span class="sxs-lookup"><span data-stu-id="37811-273">Keyset</span></span></p></th>
<th><p><span data-ttu-id="37811-274">Estático</span><span class="sxs-lookup"><span data-stu-id="37811-274">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="37811-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="37811-276">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-276">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-277">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-277">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-278">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-278">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-279">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-279">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="37811-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="37811-281">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-281">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-282">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-282">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-283">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-284">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-284">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="37811-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="37811-286">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-286">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-287">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-287">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-288">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-288">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-289">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-289">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-290"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="37811-290"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="37811-291">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-291">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-292">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-292">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-293">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-293">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-294">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-294">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-295"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="37811-295"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="37811-296">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-296">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-297">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-297">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-298">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-299">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-299">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-300"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="37811-300"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="37811-301">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-301">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-302">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-302">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-303">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-304">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-304">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="37811-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="37811-306">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-306">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-307">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-307">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-308">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-309">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-309">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-310"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="37811-310"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="37811-311">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-311">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-312">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-312">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-313">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-313">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-314">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-314">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-315"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="37811-315"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="37811-316">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-316">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-317">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-317">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-318">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-318">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-319">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-319">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-320"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="37811-320"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="37811-321">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-321">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-322">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-322">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-323">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-324">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-324">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-325"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="37811-325"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="37811-326">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-326">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-327">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-327">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-328">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-329">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-329">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="37811-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="37811-331">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-331">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-332">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-332">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-333">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-334">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-334">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="37811-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="37811-336">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-336">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-337">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-337">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-338">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-339">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-339">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-340"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="37811-340"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="37811-341">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-341">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-342">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-342">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-343">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-343">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-344">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-344">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-345"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="37811-345"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="37811-346">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-346">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-347">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-347">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-348">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-349">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-349">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-350"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="37811-350"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="37811-351">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-351">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-352">no disponible</span><span class="sxs-lookup"><span data-stu-id="37811-352">not available</span></span></p></td>
<td><p><span data-ttu-id="37811-353">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-353">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-354">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-354">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-355"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="37811-355"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="37811-356">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-356">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-357">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-357">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-358">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-358">read/write</span></span></p></td>
<td><p><span data-ttu-id="37811-359">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="37811-359">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-360"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="37811-360"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="37811-361">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-361">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-362">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-362">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-363">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-364">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-364">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-365"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="37811-365"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="37811-366">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-366">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-367">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-367">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-368">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-368">read-only</span></span></p></td>
<td><p><span data-ttu-id="37811-369">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="37811-369">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37811-370">Las propiedades [AbsolutePosition](absoluteposition-property-ado.md) y [AbsolutePage](absolutepage-property-ado.md) son de sólo escritura cuando se utiliza ADO con la versión 1.0 del Proveedor de Microsoft OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="37811-370">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="37811-371">Disponibilidad de métodos estándar **Recordset** ADO:</span><span class="sxs-lookup"><span data-stu-id="37811-371">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-372">Método</span><span class="sxs-lookup"><span data-stu-id="37811-372">Method</span></span></p></th>
<th><p><span data-ttu-id="37811-373">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="37811-373">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="37811-374">Dinámico</span><span class="sxs-lookup"><span data-stu-id="37811-374">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="37811-375">Conjunto de claves</span><span class="sxs-lookup"><span data-stu-id="37811-375">Keyset</span></span></p></th>
<th><p><span data-ttu-id="37811-376">Estático</span><span class="sxs-lookup"><span data-stu-id="37811-376">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-377"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="37811-377"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="37811-378">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-378">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-379">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-379">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-380">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-381">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-382"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="37811-382"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="37811-383">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-383">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-384">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-384">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-385">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-386">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-386">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="37811-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="37811-388">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-388">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-389">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-389">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-390">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-391">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-391">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="37811-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="37811-393">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-393">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-394">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-394">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-395">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-395">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-396">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-396">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-397"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="37811-397"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="37811-398">No</span><span class="sxs-lookup"><span data-stu-id="37811-398">No</span></span></p></td>
<td><p><span data-ttu-id="37811-399">No</span><span class="sxs-lookup"><span data-stu-id="37811-399">No</span></span></p></td>
<td><p><span data-ttu-id="37811-400">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-401">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-401">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-402"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="37811-402"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="37811-403">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-403">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-404">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-404">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-405">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-406">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-406">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-407"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="37811-407"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="37811-408">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-408">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-409">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-409">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-410">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-411">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-411">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-412"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="37811-412"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="37811-413">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-413">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-414">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-414">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-415">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-416">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-416">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-417"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="37811-417"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="37811-418">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-418">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-419">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-419">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-420">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-421">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-421">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="37811-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="37811-423">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-423">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-424">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-424">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-425">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-425">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-426">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-426">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="37811-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="37811-428">No</span><span class="sxs-lookup"><span data-stu-id="37811-428">No</span></span></p></td>
<td><p><span data-ttu-id="37811-429">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-429">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-430">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-431">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-431">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="37811-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="37811-433">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-433">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-434">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-434">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-435">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-435">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-436">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-436">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="37811-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="37811-438">No</span><span class="sxs-lookup"><span data-stu-id="37811-438">No</span></span></p></td>
<td><p><span data-ttu-id="37811-439">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-439">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-440">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-441">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="37811-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="37811-443">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-443">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-444">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-444">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-445">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-446">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-446">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-447"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="37811-447"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="37811-448">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-448">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-449">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-449">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-450">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-451">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-451">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-452"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="37811-452"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="37811-453">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-453">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-454">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-454">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-455">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-455">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-456">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-456">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-457"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="37811-457"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="37811-458">No</span><span class="sxs-lookup"><span data-stu-id="37811-458">No</span></span></p></td>
<td><p><span data-ttu-id="37811-459">No</span><span class="sxs-lookup"><span data-stu-id="37811-459">No</span></span></p></td>
<td><p><span data-ttu-id="37811-460">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-461">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-461">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-462"><a href="supports-method-ado.md">Admite</a></span><span class="sxs-lookup"><span data-stu-id="37811-462"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="37811-463">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-463">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-464">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-464">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-465">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-466">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-466">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-467"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="37811-467"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="37811-468">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-468">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-469">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-469">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-470">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-471">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-471">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="37811-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="37811-473">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-473">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-474">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-474">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-475">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-475">Yes</span></span></p></td>
<td><p><span data-ttu-id="37811-476">Sí</span><span class="sxs-lookup"><span data-stu-id="37811-476">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37811-477">\*No compatible con las bases de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="37811-477">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="37811-478">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="37811-478">Dynamic Properties</span></span>

<span data-ttu-id="37811-479">El Proveedor OLE DB para ODBC inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="37811-479">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="37811-p118">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="37811-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="37811-484">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="37811-484">Connection Dynamic Properties</span></span>

<span data-ttu-id="37811-485">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="37811-485">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-486">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="37811-486">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="37811-487">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="37811-487">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-488">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="37811-488">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="37811-489">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="37811-489">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-490">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="37811-490">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="37811-491">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="37811-491">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-492">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="37811-492">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="37811-493">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="37811-493">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-494">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="37811-494">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="37811-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="37811-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-496">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="37811-496">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="37811-497">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="37811-497">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-498">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="37811-498">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="37811-499">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="37811-499">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-500">Column Definition</span><span class="sxs-lookup"><span data-stu-id="37811-500">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="37811-501">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="37811-501">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-502">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="37811-502">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="37811-503">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="37811-503">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-504">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="37811-504">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="37811-505">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="37811-505">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-506">Data Source</span><span class="sxs-lookup"><span data-stu-id="37811-506">Data Source</span></span></p></td>
<td><p><span data-ttu-id="37811-507">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="37811-507">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-508">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="37811-508">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="37811-509">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="37811-509">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-510">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="37811-510">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="37811-511">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="37811-511">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-512">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="37811-512">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="37811-513">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="37811-513">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-514">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="37811-514">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="37811-515">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="37811-515">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-516">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="37811-516">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="37811-517">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="37811-517">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-518">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="37811-518">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="37811-519">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="37811-519">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-520">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="37811-520">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="37811-521">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="37811-521">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-522">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="37811-522">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="37811-523">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="37811-523">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-524">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="37811-524">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="37811-525">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="37811-525">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-526">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="37811-526">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="37811-527">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="37811-527">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-528">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="37811-528">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="37811-529">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="37811-529">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-530">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="37811-530">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="37811-531">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="37811-531">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-532">Location</span><span class="sxs-lookup"><span data-stu-id="37811-532">Location</span></span></p></td>
<td><p><span data-ttu-id="37811-533">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="37811-533">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-534">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="37811-534">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="37811-535">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="37811-535">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-536">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="37811-536">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="37811-537">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="37811-537">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-538">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="37811-538">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="37811-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="37811-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-540">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="37811-540">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="37811-541">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="37811-541">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-542">Mode</span><span class="sxs-lookup"><span data-stu-id="37811-542">Mode</span></span></p></td>
<td><p><span data-ttu-id="37811-543">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="37811-543">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-544">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="37811-544">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="37811-545">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="37811-545">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-546">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="37811-546">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="37811-547">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="37811-547">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-548">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="37811-548">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="37811-549">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="37811-549">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-550">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="37811-550">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="37811-551">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="37811-551">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-552">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="37811-552">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="37811-553">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="37811-553">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-554">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="37811-554">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="37811-555">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="37811-555">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-556">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="37811-556">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="37811-557">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="37811-557">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-558">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="37811-558">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="37811-559">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="37811-559">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-560">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="37811-560">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="37811-561">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="37811-561">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-562">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="37811-562">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="37811-563">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="37811-563">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-564">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="37811-564">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="37811-565">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="37811-565">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-566">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="37811-566">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="37811-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="37811-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-568">Password</span><span class="sxs-lookup"><span data-stu-id="37811-568">Password</span></span></p></td>
<td><p><span data-ttu-id="37811-569">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="37811-569">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-570">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="37811-570">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="37811-571">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="37811-571">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-572">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="37811-572">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="37811-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="37811-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-574">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="37811-574">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="37811-575">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="37811-575">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-576">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="37811-576">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="37811-577">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="37811-577">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-578">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="37811-578">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="37811-579">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="37811-579">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-580">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="37811-580">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="37811-581">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="37811-581">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-582">Prompt</span><span class="sxs-lookup"><span data-stu-id="37811-582">Prompt</span></span></p></td>
<td><p><span data-ttu-id="37811-583">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="37811-583">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-584">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="37811-584">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="37811-585">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="37811-585">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-586">Provider Name</span><span class="sxs-lookup"><span data-stu-id="37811-586">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="37811-587">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="37811-587">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-588">Provider Version</span><span class="sxs-lookup"><span data-stu-id="37811-588">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="37811-589">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="37811-589">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-590">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="37811-590">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="37811-591">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="37811-591">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-592">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="37811-592">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="37811-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="37811-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-594">Schema Term</span><span class="sxs-lookup"><span data-stu-id="37811-594">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="37811-595">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="37811-595">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-596">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="37811-596">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="37811-597">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="37811-597">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-598">SQL Support</span><span class="sxs-lookup"><span data-stu-id="37811-598">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="37811-599">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="37811-599">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-600">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="37811-600">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="37811-601">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="37811-601">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-602">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="37811-602">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="37811-603">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="37811-603">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-604">Table Term</span><span class="sxs-lookup"><span data-stu-id="37811-604">Table Term</span></span></p></td>
<td><p><span data-ttu-id="37811-605">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="37811-605">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-606">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="37811-606">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="37811-607">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="37811-607">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-608">User ID</span><span class="sxs-lookup"><span data-stu-id="37811-608">User ID</span></span></p></td>
<td><p><span data-ttu-id="37811-609">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="37811-609">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-610">User Name</span><span class="sxs-lookup"><span data-stu-id="37811-610">User Name</span></span></p></td>
<td><p><span data-ttu-id="37811-611">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="37811-611">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-612">Window Handle</span><span class="sxs-lookup"><span data-stu-id="37811-612">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="37811-613">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="37811-613">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="37811-614">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="37811-614">Recordset Dynamic Properties</span></span>

<span data-ttu-id="37811-615">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="37811-615">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-616">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="37811-616">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="37811-617">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="37811-617">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-618">Access Order</span><span class="sxs-lookup"><span data-stu-id="37811-618">Access Order</span></span></p></td>
<td><p><span data-ttu-id="37811-619">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="37811-619">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-620">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="37811-620">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="37811-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="37811-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-622">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="37811-622">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="37811-623">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="37811-623">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-624">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="37811-624">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="37811-625">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="37811-625">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-626">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="37811-626">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-627">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="37811-627">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-628">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="37811-628">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="37811-629">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="37811-629">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-630">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="37811-630">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-631">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="37811-631">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-632">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="37811-632">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="37811-633">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="37811-633">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-634">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="37811-634">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="37811-635">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="37811-635">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-636">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="37811-636">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-637">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="37811-637">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-638">IAccessor</span><span class="sxs-lookup"><span data-stu-id="37811-638">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="37811-639">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="37811-639">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-640">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="37811-640">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="37811-641">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="37811-641">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-642">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="37811-642">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="37811-643">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="37811-643">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-644">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="37811-644">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="37811-645">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="37811-645">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-646">IConvertType</span><span class="sxs-lookup"><span data-stu-id="37811-646">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="37811-647">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="37811-647">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-648">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="37811-648">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-649">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="37811-649">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-650">IRowset</span><span class="sxs-lookup"><span data-stu-id="37811-650">IRowset</span></span></p></td>
<td><p><span data-ttu-id="37811-651">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="37811-651">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-652">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="37811-652">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="37811-653">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="37811-653">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-654">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="37811-654">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="37811-655">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="37811-655">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-656">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="37811-656">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="37811-657">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="37811-657">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-658">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="37811-658">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="37811-659">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="37811-659">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-660">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="37811-660">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-661">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="37811-661">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="37811-662">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="37811-662">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-663">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="37811-663">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="37811-664">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="37811-664">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-665">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="37811-665">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="37811-666">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="37811-666">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-667">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="37811-667">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="37811-668">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="37811-668">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-669">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="37811-669">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="37811-670">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="37811-670">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-671">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="37811-671">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-672">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="37811-672">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-673">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="37811-673">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-674">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="37811-674">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-675">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="37811-675">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-676">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="37811-676">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-677">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="37811-677">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="37811-678">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="37811-678">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-679">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="37811-679">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="37811-680">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="37811-680">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-681">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="37811-681">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="37811-682">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="37811-682">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-683">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="37811-683">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="37811-684">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="37811-684">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-685">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="37811-685">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="37811-686">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="37811-686">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-687">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="37811-687">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="37811-688">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="37811-688">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-689">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="37811-689">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="37811-690">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="37811-690">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-691">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="37811-691">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="37811-692">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="37811-692">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-693">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="37811-693">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="37811-694">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="37811-694">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-695">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="37811-695">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-696">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="37811-696">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-697">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="37811-697">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="37811-698">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="37811-698">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-699">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="37811-699">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="37811-700">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="37811-700">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-701">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="37811-701">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-702">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="37811-702">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-703">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="37811-703">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-704">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="37811-704">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-705">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="37811-705">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-706">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="37811-706">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-707">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="37811-707">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="37811-708">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="37811-708">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-709">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="37811-709">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-710">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="37811-710">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-711">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="37811-711">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="37811-712">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="37811-712">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-713">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="37811-713">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-714">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="37811-714">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-715">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="37811-715">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-716">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="37811-716">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-717">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="37811-717">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-718">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="37811-718">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-719">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="37811-719">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-720">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="37811-720">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-721">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="37811-721">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="37811-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-723">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="37811-723">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-724">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="37811-724">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-725">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="37811-725">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="37811-726">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="37811-726">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-727">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="37811-727">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="37811-728">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="37811-728">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-729">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="37811-729">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="37811-730">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="37811-730">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-731">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="37811-731">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-732">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="37811-732">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-733">Updatability</span><span class="sxs-lookup"><span data-stu-id="37811-733">Updatability</span></span></p></td>
<td><p><span data-ttu-id="37811-734">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="37811-734">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-735">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="37811-735">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="37811-736">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="37811-736">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="37811-737">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="37811-737">Command Dynamic Properties</span></span>

<span data-ttu-id="37811-738">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="37811-738">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37811-739">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="37811-739">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="37811-740">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="37811-740">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37811-741">Access Order</span><span class="sxs-lookup"><span data-stu-id="37811-741">Access Order</span></span></p></td>
<td><p><span data-ttu-id="37811-742">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="37811-742">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-743">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="37811-743">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="37811-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="37811-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-745">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="37811-745">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="37811-746">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="37811-746">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-747">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="37811-747">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="37811-748">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="37811-748">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-749">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="37811-749">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-750">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="37811-750">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-751">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="37811-751">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="37811-752">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="37811-752">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-753">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="37811-753">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-754">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="37811-754">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-755">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="37811-755">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="37811-756">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="37811-756">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-757">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="37811-757">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="37811-758">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="37811-758">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-759">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="37811-759">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-760">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="37811-760">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-761">IAccessor</span><span class="sxs-lookup"><span data-stu-id="37811-761">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="37811-762">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="37811-762">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-763">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="37811-763">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="37811-764">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="37811-764">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-765">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="37811-765">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="37811-766">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="37811-766">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-767">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="37811-767">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="37811-768">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="37811-768">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-769">IConvertType</span><span class="sxs-lookup"><span data-stu-id="37811-769">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="37811-770">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="37811-770">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-771">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="37811-771">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-772">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="37811-772">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-773">IRowset</span><span class="sxs-lookup"><span data-stu-id="37811-773">IRowset</span></span></p></td>
<td><p><span data-ttu-id="37811-774">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="37811-774">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-775">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="37811-775">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="37811-776">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="37811-776">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-777">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="37811-777">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="37811-778">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="37811-778">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-779">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="37811-779">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="37811-780">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="37811-780">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-781">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="37811-781">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="37811-782">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="37811-782">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-783">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="37811-783">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-784">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="37811-784">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="37811-785">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="37811-785">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-786">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="37811-786">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="37811-787">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="37811-787">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-788">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="37811-788">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="37811-789">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="37811-789">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-790">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="37811-790">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="37811-791">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="37811-791">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-792">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="37811-792">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="37811-793">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="37811-793">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-794">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="37811-794">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-795">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="37811-795">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-796">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="37811-796">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-797">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="37811-797">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-798">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="37811-798">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-799">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="37811-799">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-800">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="37811-800">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="37811-801">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="37811-801">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-802">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="37811-802">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="37811-803">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="37811-803">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-804">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="37811-804">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="37811-805">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="37811-805">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-806">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="37811-806">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="37811-807">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="37811-807">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-808">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="37811-808">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="37811-809">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="37811-809">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-810">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="37811-810">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="37811-811">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="37811-811">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-812">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="37811-812">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="37811-813">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="37811-813">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-814">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="37811-814">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="37811-815">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="37811-815">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-816">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="37811-816">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="37811-817">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="37811-817">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-818">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="37811-818">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="37811-819">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="37811-819">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-820">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="37811-820">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="37811-821">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="37811-821">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-822">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="37811-822">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="37811-823">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="37811-823">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-824">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="37811-824">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-825">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="37811-825">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-826">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="37811-826">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-827">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="37811-827">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-828">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="37811-828">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-829">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="37811-829">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-830">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="37811-830">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="37811-831">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="37811-831">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-832">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="37811-832">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-833">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="37811-833">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-834">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="37811-834">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="37811-835">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="37811-835">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-836">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="37811-836">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-837">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="37811-837">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-838">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="37811-838">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-839">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="37811-839">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-840">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="37811-840">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-841">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="37811-841">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-842">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="37811-842">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-843">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="37811-843">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-844">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="37811-844">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="37811-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-846">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="37811-846">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="37811-847">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="37811-847">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-848">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="37811-848">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="37811-849">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="37811-849">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-850">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="37811-850">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="37811-851">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="37811-851">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-852">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="37811-852">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="37811-853">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="37811-853">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37811-854">Updatability</span><span class="sxs-lookup"><span data-stu-id="37811-854">Updatability</span></span></p></td>
<td><p><span data-ttu-id="37811-855">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="37811-855">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37811-856">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="37811-856">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="37811-857">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="37811-857">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="37811-858">Vea también</span><span class="sxs-lookup"><span data-stu-id="37811-858">See also</span></span>

<span data-ttu-id="37811-859">Para obtener información detallada acerca de implementación específico e información funcional acerca el proveedor Microsoft OLE DB para ODBC, consulte la [Guía del programador de OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) o visite el [Centro de desarrolladores de plataforma de datos](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="37811-859">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

