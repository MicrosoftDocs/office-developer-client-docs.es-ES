---
title: Proveedor de Microsoft OLE DB para ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704563"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="65289-102">Proveedor de Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="65289-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="65289-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65289-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65289-p101">Para un programador de ADO o RDS, un mundo ideal sería aquel en que cada origen de datos expusiera una interfaz OLE DB, de modo que ADO pudiera llamar directamente al origen de datos. Aunque cada vez más proveedores de bases de datos están implementando interfaces OLE DB, algunos orígenes de datos aún no están expuestos de esta forma. Sin embargo, es posible obtener acceso a prácticamente todos los sistemas DBMS que se usan en la actualidad a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="65289-107">Los controladores ODBC están disponibles para todos los principales DBMS que se utilizan hoy en día, incluidos Microsoft SQL Server, Microsoft Access (motor de bases de datos Microsoft Jet) y Microsoft FoxPro, además de otros productos de base de datos no pertenecientes a Microsoft, como Oracle.</span><span class="sxs-lookup"><span data-stu-id="65289-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="65289-p102">Sin embargo, el Proveedor Microsoft ODBC permite a ADO conectarse a cualquier origen de datos ODBC. El proveedor es de subprocesamiento libre y está habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="65289-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="65289-p103">El proveedor admite transacciones, aunque los diferentes motores DBMS ofrecen diferentes tipos de compatibilidad con ellas. Por ejemplo, Microsoft Access admite las transacciones anidadas de hasta cinco niveles.</span><span class="sxs-lookup"><span data-stu-id="65289-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="65289-112">Éste es el proveedor predeterminado para ADO y admite todas las propiedades y los métodos ADO dependientes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="65289-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="65289-113">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="65289-113">Connection String Parameters</span></span>

<span data-ttu-id="65289-114">Para conectar con este proveedor, establezca el argumento **Provider=** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="65289-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="65289-115">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="65289-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="65289-116">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="65289-116">Typical Connection String</span></span>

<span data-ttu-id="65289-117">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="65289-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="65289-118">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="65289-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65289-119">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="65289-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="65289-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="65289-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="65289-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="65289-122">Especifica el Proveedor OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="65289-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="65289-124">Especifica el nombre del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="65289-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="65289-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="65289-126">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="65289-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="65289-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="65289-128">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="65289-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="65289-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="65289-130">Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</span><span class="sxs-lookup"><span data-stu-id="65289-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65289-131">Dado que éste es el proveedor predeterminado para ADO, si se omite el parámetro **Provider=** de la cadena de conexión, ADO intentará establecer una conexión con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="65289-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="65289-p104">El proveedor no admite ningún parámetro de conexión específico además de los definidos por ADO. No obstante, pasará cualquier parámetro de conexión que no sea de ADO al controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="65289-p105">Dado que se puede omitir el parámetro **Provider**, es posible elaborar una cadena de conexión ADO idéntica a una cadena de conexión ODBC para el mismo origen de datos. Utilice los mismos nombres de parámetro (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), los valores y la sintaxis que cuando elabora una cadena de conexión ODBC. Es posible conectar con o sin un nombre de origen de datos predefinido (DSN) o un FileDSN.</span><span class="sxs-lookup"><span data-stu-id="65289-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="65289-137">**Sintaxis con un DSN o un FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="65289-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="65289-138">**Sintaxis sin ningún DSN (conexión sin DSN):**</span><span class="sxs-lookup"><span data-stu-id="65289-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="65289-p106">Si se utiliza un **DSN** o un **FileDSN**, debe definirse mediante el Administrador de origen de datos ODBC del Panel de control de Windows. En Microsoft Windows 2000, el Administrador ODBC se encuentra en Herramientas administrativas. En versiones anteriores de Windows, el icono Administrador ODBC se denomina **ODBC de 32 bits** o simplemente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="65289-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="65289-142">Como alternativa al establecimiento de un **DSN**, puede especificar el controlador ODBC (**DRIVER=**), como "SQL Server;" el nombre del servidor (**SERVER=**); y el nombre de la base de datos (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="65289-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="65289-143">También puede especificar un nombre de cuenta de usuario (**UID=**) y la contraseña para esa cuenta (**PWD=**) en los parámetros específicos de ODBC o en los parámetros estándar *user* y *password* definidos por ADO.</span><span class="sxs-lookup"><span data-stu-id="65289-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="65289-144">Aunque una definición **DSN** ya especifica una base de datos, puede especificar *un* parámetro de *base de datos* además de un **DSN** para conectarse a una base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="65289-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="65289-145">Es una buena idea incluir siempre *el* parámetro de *base de datos* al utilizar un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="65289-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="65289-146">Eso garantizará la conexión a la base de datos adecuada en caso de que otro usuario haya modificado el parámetro desde la última vez que se comprobó la definición **DSN**.</span><span class="sxs-lookup"><span data-stu-id="65289-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="65289-147">Propiedades Connection específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="65289-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="65289-p108">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="65289-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65289-150">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="65289-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="65289-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="65289-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-152">Accessible Procedures</span><span class="sxs-lookup"><span data-stu-id="65289-152">Accessible Procedures</span></span><br />
<span data-ttu-id="65289-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="65289-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="65289-154">Indica si el usuario tiene acceso a procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="65289-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-155">Tablas accesibles</span><span class="sxs-lookup"><span data-stu-id="65289-155">Accessible Tables</span></span><br />
<span data-ttu-id="65289-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="65289-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="65289-157">Indica si el usuario tiene permiso para ejecutar instrucciones SELECT en las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="65289-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-158">Instrucciones activas</span><span class="sxs-lookup"><span data-stu-id="65289-158">Active Statements</span></span><br />
<span data-ttu-id="65289-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="65289-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="65289-160">Indica el número de controladores que puede admitir un controlador ODBC en una conexión.</span><span class="sxs-lookup"><span data-stu-id="65289-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-161">Nombre del controlador</span><span class="sxs-lookup"><span data-stu-id="65289-161">Driver Name</span></span><br />
<span data-ttu-id="65289-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="65289-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="65289-163">Indica el nombre de archivo del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-164">Versión del controlador ODBC</span><span class="sxs-lookup"><span data-stu-id="65289-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="65289-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="65289-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="65289-166">Indica la versión de ODBC que admite este controlador.</span><span class="sxs-lookup"><span data-stu-id="65289-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-167">Uso de archivos</span><span class="sxs-lookup"><span data-stu-id="65289-167">File Usage</span></span><br />
<span data-ttu-id="65289-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="65289-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="65289-169">Indica cómo trata el controlador a un archivo de un origen de datos, como una tabla o como un catálogo.</span><span class="sxs-lookup"><span data-stu-id="65289-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-170">Al igual que la cláusula Escape</span><span class="sxs-lookup"><span data-stu-id="65289-170">Like Escape Clause</span></span><br />
<span data-ttu-id="65289-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="65289-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="65289-172">Indica si el controlador admite la definición y el uso de un carácter de escape para el carácter de porcentaje (%) y de un carácter de subrayado (_) en el predicado LIKE de una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="65289-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-173">Max Columns in Group By</span><span class="sxs-lookup"><span data-stu-id="65289-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="65289-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="65289-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="65289-175">Indica el número máximo de columnas que se puede enumerar en la cláusula GROUP BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="65289-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-176">Número máximo de columnas en el índice</span><span class="sxs-lookup"><span data-stu-id="65289-176">Max Columns in Index</span></span><br />
<span data-ttu-id="65289-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="65289-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="65289-178">Indica el número máximo de columnas que puede ser incluido en un índice.</span><span class="sxs-lookup"><span data-stu-id="65289-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-179">Max Columns in Order By</span><span class="sxs-lookup"><span data-stu-id="65289-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="65289-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="65289-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="65289-181">Indica el número máximo de columnas que se puede enumerar en la cláusula ORDER BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="65289-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-182">Número máximo de columnas en Seleccionar</span><span class="sxs-lookup"><span data-stu-id="65289-182">Max Columns in Select</span></span><br />
<span data-ttu-id="65289-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="65289-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="65289-184">Indica el número máximo de columnas que se puede enumerar en la parte SELECT de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="65289-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-185">Número máximo de columnas de tabla</span><span class="sxs-lookup"><span data-stu-id="65289-185">Max Columns in Table</span></span><br />
<span data-ttu-id="65289-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="65289-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="65289-187">Indica el número máximo de columnas permitido en una tabla.</span><span class="sxs-lookup"><span data-stu-id="65289-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-188">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="65289-188">Numeric Functions</span></span><br />
<span data-ttu-id="65289-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="65289-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="65289-p109">Indica las funciones numéricas admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-192">Outer Join Capabilities</span><span class="sxs-lookup"><span data-stu-id="65289-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="65289-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="65289-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="65289-194">Indica los tipos de combinaciones externas admitidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="65289-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-195">Combinaciones externas</span><span class="sxs-lookup"><span data-stu-id="65289-195">Outer Joins</span></span><br />
<span data-ttu-id="65289-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="65289-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="65289-197">Indica si el proveedor admite combinaciones externas.</span><span class="sxs-lookup"><span data-stu-id="65289-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-198">Caracteres especiales</span><span class="sxs-lookup"><span data-stu-id="65289-198">Special Characters</span></span><br />
<span data-ttu-id="65289-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="65289-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="65289-200">Indica qué caracteres tienen un significado especial para el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-201">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="65289-201">Stored Procedures</span></span><br />
<span data-ttu-id="65289-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="65289-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="65289-203">Indica si hay procedimientos almacenados disponibles para ser utilizados con este controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-204">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="65289-204">String Functions</span></span><br />
<span data-ttu-id="65289-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="65289-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="65289-p110">Indica qué funciones de cadena son admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-208">Funciones del sistema</span><span class="sxs-lookup"><span data-stu-id="65289-208">System Functions</span></span><br />
<span data-ttu-id="65289-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="65289-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="65289-p111">Indica las funciones del sistema admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-212">Funciones de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="65289-212">Time/Date Functions</span></span><br />
<span data-ttu-id="65289-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="65289-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="65289-p112">Indica las funciones de fecha y hora admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-216">Compatibilidad con la gramática SQL</span><span class="sxs-lookup"><span data-stu-id="65289-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="65289-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="65289-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="65289-218">Indica la gramática SQL admitida por el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="65289-219">Propiedades Recordset y Command específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="65289-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="65289-p113">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección **Properties** de los objetos **Recordset** y **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="65289-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65289-222">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="65289-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="65289-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="65289-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-224">Query Based Updates/Deletes/Inserts</span><span class="sxs-lookup"><span data-stu-id="65289-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="65289-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="65289-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="65289-226">Indica si se pueden realizar actualizaciones, eliminaciones e inserciones mediante consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="65289-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-227">ODBC Concurrency Type</span><span class="sxs-lookup"><span data-stu-id="65289-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="65289-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="65289-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="65289-229">Indica el método utilizado para minimizar los problemas potenciales causados por el intento de dos usuarios de obtener acceso a los mismos datos del origen de datos de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="65289-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-230">Accesibilidad BLOB en el cursor de sólo avance</span><span class="sxs-lookup"><span data-stu-id="65289-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="65289-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="65289-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="65289-232">Indica si es posible obtener acceso a <strong>campos</strong> BLOB cuando se utiliza un cursor de sólo avance.</span><span class="sxs-lookup"><span data-stu-id="65289-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-233">Incluir SQL_FLOAT, SQL_DOUBLE y SQL_REAL en QBU WHERE clauses</span><span class="sxs-lookup"><span data-stu-id="65289-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="65289-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="65289-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="65289-235">Indica si se pueden incluir valores SQL_FLOAT, SQL_DOUBLE y SQL_REAL en una cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="65289-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-236">Posición en la última fila después de insertar</span><span class="sxs-lookup"><span data-stu-id="65289-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="65289-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="65289-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="65289-238">Indica que tras haber insertado un nuevo registro en una tabla, la última fila de la misma se convertirá en la fila actual.</span><span class="sxs-lookup"><span data-stu-id="65289-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="65289-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="65289-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="65289-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="65289-241">Indica si la interfaz <strong>IRowsetChange</strong> admite información ampliada.</span><span class="sxs-lookup"><span data-stu-id="65289-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-242">Tipo de Cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="65289-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="65289-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="65289-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="65289-244">Indica el tipo de cursor usado por el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="65289-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-245">Generar un conjunto de filas que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="65289-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="65289-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="65289-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="65289-247">Indica que el controlador ODBC genera un conjunto de registros que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="65289-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="65289-248">Texto del comando</span><span class="sxs-lookup"><span data-stu-id="65289-248">Command Text</span></span>

<span data-ttu-id="65289-249">La forma de utilizar el objeto [Command](command-object-ado.md) depende en gran medida del origen de datos y del tipo de consulta o instrucción de comando que acepte.</span><span class="sxs-lookup"><span data-stu-id="65289-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="65289-250">ODBC proporciona una sintaxis específica para llamar a los procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="65289-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="65289-251">Para la propiedad [CommandText](commandtext-property-ado.md) de un objeto **Command** , el argumento *CommandText* del método **Execute** en un objeto [Connection](connection-object-ado.md) o el argumento *Source* en el método **Open** en un [objeto Recordset](recordset-object-ado.md) objeto, pasa en una cadena con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="65289-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="65289-p115">Cada **?** hace referencia a un objeto de la colección [Parameters](parameters-collection-ado.md). El primer **?** hace referencia a **Parameters**(0), el siguiente **?** a **Parameters**(1) y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="65289-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="65289-p116">Las referencias del parámetro son opcionales y dependen de la estructura del procedimiento almacenado. Si desea llamar a un procedimiento almacenado que no define parámetros, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="65289-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="65289-259">Si tiene dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="65289-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="65289-p117">Si el procedimiento almacenado va a devolver un valor, el valor devuelto se trata como otro parámetro. Si no dispone de parámetros de consulta pero tiene un valor devuelto, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="65289-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="65289-262">Por último, si tiene un valor devuelto y dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="65289-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="65289-263">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="65289-263">Recordset Behavior</span></span>

<span data-ttu-id="65289-264">En las tablas siguientes se enumeran los métodos y las propiedades ADO estándar disponibles en un objeto **Recordset** abierto con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="65289-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="65289-265">Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección **Properties** del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.</span><span class="sxs-lookup"><span data-stu-id="65289-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="65289-266">Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="65289-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="65289-267">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65289-267">Property</span></span></p></th>
<th><p><span data-ttu-id="65289-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="65289-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="65289-269">Dinámico</span><span class="sxs-lookup"><span data-stu-id="65289-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="65289-270">Conjunto de claves</span><span class="sxs-lookup"><span data-stu-id="65289-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="65289-271">Estático</span><span class="sxs-lookup"><span data-stu-id="65289-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="65289-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="65289-273">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-273">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-274">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-274">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-275">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-276">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="65289-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="65289-278">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-278">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-279">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-279">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-280">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-281">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="65289-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="65289-283">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-284">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-285">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-286">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="65289-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="65289-288">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-289">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-290">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-291">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="65289-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="65289-293">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-293">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-294">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-294">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-295">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-296">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="65289-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="65289-298">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-299">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-300">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-301">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="65289-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="65289-303">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-304">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-305">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-306">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="65289-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="65289-308">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-309">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-310">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-311">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="65289-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="65289-313">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-314">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-315">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-316">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-317"><a href="filter-property-ado.md">Filtro</a></span><span class="sxs-lookup"><span data-stu-id="65289-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="65289-318">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-319">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-320">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-321">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="65289-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="65289-323">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-324">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-325">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-326">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="65289-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="65289-328">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-329">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-330">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-331">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="65289-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="65289-333">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-334">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-335">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-336">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="65289-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="65289-338">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-339">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-339">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-340">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-341">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="65289-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="65289-343">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-344">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-345">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-346">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="65289-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="65289-348">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-349">no disponible</span><span class="sxs-lookup"><span data-stu-id="65289-349">not available</span></span></p></td>
<td><p><span data-ttu-id="65289-350">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-351">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="65289-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="65289-353">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-354">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-355">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="65289-356">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="65289-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="65289-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="65289-358">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-359">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-360">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-361">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-362"><a href="status-property-ado-recordset.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="65289-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="65289-363">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-364">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-365">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="65289-366">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="65289-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65289-367">Las propiedades [AbsolutePosition](absoluteposition-property-ado.md) y [AbsolutePage](absolutepage-property-ado.md) son de sólo escritura cuando se utiliza ADO con la versión 1.0 del Proveedor de Microsoft OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="65289-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="65289-368">Disponibilidad de métodos estándar **Recordset** ADO:</span><span class="sxs-lookup"><span data-stu-id="65289-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="65289-369">Método</span><span class="sxs-lookup"><span data-stu-id="65289-369">Method</span></span></p></th>
<th><p><span data-ttu-id="65289-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="65289-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="65289-371">Dinámico</span><span class="sxs-lookup"><span data-stu-id="65289-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="65289-372">Conjunto de claves</span><span class="sxs-lookup"><span data-stu-id="65289-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="65289-373">Estático</span><span class="sxs-lookup"><span data-stu-id="65289-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="65289-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="65289-375">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-376">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-377">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-378">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="65289-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="65289-380">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-381">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-382">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-383">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="65289-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="65289-385">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-386">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-387">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-388">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="65289-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="65289-390">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-391">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-392">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-393">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="65289-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="65289-395">No</span><span class="sxs-lookup"><span data-stu-id="65289-395">No</span></span></p></td>
<td><p><span data-ttu-id="65289-396">No</span><span class="sxs-lookup"><span data-stu-id="65289-396">No</span></span></p></td>
<td><p><span data-ttu-id="65289-397">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-398">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="65289-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="65289-400">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-401">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-402">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-403">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-404"><a href="delete-method-ado-recordset.md">Eliminar</a></span><span class="sxs-lookup"><span data-stu-id="65289-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="65289-405">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-406">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-407">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-408">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="65289-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="65289-410">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-411">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-412">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-413">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="65289-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="65289-415">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-416">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-417">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-418">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="65289-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="65289-420">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-421">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-422">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-423">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="65289-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="65289-425">No</span><span class="sxs-lookup"><span data-stu-id="65289-425">No</span></span></p></td>
<td><p><span data-ttu-id="65289-426">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-427">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-428">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="65289-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="65289-430">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-431">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-432">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-433">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="65289-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="65289-435">No</span><span class="sxs-lookup"><span data-stu-id="65289-435">No</span></span></p></td>
<td><p><span data-ttu-id="65289-436">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-437">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-438">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="65289-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="65289-440">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-441">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-442">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-443">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="65289-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="65289-445">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-446">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-447">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-448">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="65289-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="65289-450">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-451">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-452">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-453">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="65289-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="65289-455">No</span><span class="sxs-lookup"><span data-stu-id="65289-455">No</span></span></p></td>
<td><p><span data-ttu-id="65289-456">No</span><span class="sxs-lookup"><span data-stu-id="65289-456">No</span></span></p></td>
<td><p><span data-ttu-id="65289-457">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-458">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-459"><a href="supports-method-ado.md">Admite</a></span><span class="sxs-lookup"><span data-stu-id="65289-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="65289-460">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-461">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-462">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-463">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-464"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="65289-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="65289-465">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-466">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-467">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-468">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="65289-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="65289-470">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-471">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-472">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="65289-473">Sí</span><span class="sxs-lookup"><span data-stu-id="65289-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65289-474">\*No compatible con las bases de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="65289-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="65289-475">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="65289-475">Dynamic Properties</span></span>

<span data-ttu-id="65289-476">El Proveedor OLE DB para ODBC inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="65289-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="65289-p118">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="65289-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="65289-481">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="65289-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="65289-482">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="65289-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65289-483">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="65289-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="65289-484">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="65289-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="65289-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="65289-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="65289-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="65289-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="65289-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="65289-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="65289-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="65289-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="65289-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="65289-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="65289-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="65289-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="65289-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="65289-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="65289-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="65289-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="65289-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="65289-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="65289-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="65289-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="65289-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="65289-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="65289-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="65289-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="65289-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="65289-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="65289-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="65289-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="65289-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="65289-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="65289-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="65289-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="65289-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="65289-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="65289-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="65289-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="65289-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="65289-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="65289-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="65289-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="65289-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="65289-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="65289-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="65289-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="65289-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="65289-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="65289-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="65289-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="65289-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="65289-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="65289-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="65289-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="65289-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="65289-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="65289-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="65289-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="65289-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="65289-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="65289-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="65289-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="65289-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="65289-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="65289-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="65289-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="65289-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="65289-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-529">Location</span><span class="sxs-lookup"><span data-stu-id="65289-529">Location</span></span></p></td>
<td><p><span data-ttu-id="65289-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="65289-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="65289-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="65289-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="65289-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="65289-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="65289-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="65289-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="65289-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="65289-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="65289-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="65289-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="65289-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="65289-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-539">Mode</span><span class="sxs-lookup"><span data-stu-id="65289-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="65289-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="65289-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="65289-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="65289-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="65289-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="65289-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="65289-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="65289-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="65289-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="65289-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="65289-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="65289-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="65289-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="65289-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="65289-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="65289-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="65289-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="65289-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="65289-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="65289-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="65289-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="65289-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="65289-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="65289-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="65289-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="65289-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="65289-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="65289-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="65289-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="65289-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="65289-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="65289-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="65289-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="65289-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="65289-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="65289-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="65289-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="65289-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-565">Password</span><span class="sxs-lookup"><span data-stu-id="65289-565">Password</span></span></p></td>
<td><p><span data-ttu-id="65289-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="65289-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="65289-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="65289-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="65289-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="65289-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="65289-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="65289-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="65289-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="65289-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="65289-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="65289-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="65289-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="65289-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="65289-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="65289-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="65289-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="65289-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="65289-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="65289-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="65289-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="65289-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="65289-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="65289-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="65289-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="65289-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="65289-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="65289-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="65289-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="65289-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="65289-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="65289-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="65289-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="65289-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="65289-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="65289-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="65289-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="65289-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="65289-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="65289-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="65289-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="65289-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="65289-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="65289-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="65289-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="65289-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="65289-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="65289-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="65289-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="65289-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="65289-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="65289-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="65289-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="65289-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="65289-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="65289-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="65289-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="65289-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="65289-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-605">User ID</span><span class="sxs-lookup"><span data-stu-id="65289-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="65289-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="65289-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-607">User Name</span><span class="sxs-lookup"><span data-stu-id="65289-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="65289-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="65289-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="65289-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="65289-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="65289-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="65289-611">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="65289-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="65289-612">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="65289-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65289-613">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="65289-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="65289-614">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="65289-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="65289-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="65289-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="65289-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="65289-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="65289-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="65289-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="65289-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="65289-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="65289-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="65289-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="65289-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="65289-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="65289-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="65289-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="65289-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="65289-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="65289-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="65289-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="65289-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="65289-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="65289-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="65289-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="65289-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="65289-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="65289-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="65289-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="65289-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="65289-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="65289-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="65289-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="65289-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="65289-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="65289-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="65289-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="65289-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="65289-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="65289-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="65289-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="65289-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="65289-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="65289-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="65289-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="65289-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="65289-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="65289-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="65289-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="65289-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="65289-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="65289-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="65289-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="65289-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="65289-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="65289-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="65289-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="65289-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="65289-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="65289-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="65289-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="65289-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="65289-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="65289-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="65289-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="65289-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="65289-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="65289-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="65289-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="65289-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="65289-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="65289-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="65289-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="65289-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="65289-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="65289-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="65289-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="65289-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="65289-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="65289-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="65289-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="65289-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="65289-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="65289-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="65289-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="65289-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="65289-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="65289-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="65289-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="65289-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="65289-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="65289-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="65289-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="65289-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="65289-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="65289-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="65289-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="65289-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="65289-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="65289-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="65289-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="65289-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="65289-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="65289-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="65289-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="65289-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="65289-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="65289-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="65289-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="65289-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="65289-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="65289-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="65289-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="65289-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="65289-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="65289-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="65289-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="65289-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="65289-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="65289-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="65289-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="65289-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="65289-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="65289-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="65289-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="65289-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="65289-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="65289-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="65289-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="65289-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="65289-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="65289-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="65289-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="65289-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="65289-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="65289-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="65289-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="65289-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="65289-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="65289-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="65289-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="65289-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="65289-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="65289-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="65289-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="65289-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="65289-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="65289-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="65289-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="65289-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="65289-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="65289-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="65289-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="65289-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="65289-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="65289-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="65289-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="65289-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="65289-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="65289-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="65289-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="65289-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="65289-734">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="65289-734">Command Dynamic Properties</span></span>

<span data-ttu-id="65289-735">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="65289-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65289-736">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="65289-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="65289-737">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="65289-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65289-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="65289-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="65289-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="65289-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="65289-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="65289-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="65289-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="65289-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="65289-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="65289-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="65289-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="65289-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="65289-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="65289-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="65289-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="65289-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="65289-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="65289-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="65289-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="65289-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="65289-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="65289-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="65289-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="65289-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="65289-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="65289-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="65289-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="65289-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="65289-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="65289-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="65289-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="65289-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="65289-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="65289-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="65289-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="65289-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="65289-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="65289-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="65289-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="65289-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="65289-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="65289-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="65289-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="65289-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="65289-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="65289-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="65289-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="65289-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="65289-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="65289-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="65289-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="65289-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="65289-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="65289-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="65289-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="65289-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="65289-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="65289-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="65289-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="65289-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="65289-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="65289-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="65289-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="65289-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="65289-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="65289-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="65289-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="65289-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="65289-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="65289-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="65289-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="65289-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="65289-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="65289-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="65289-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="65289-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="65289-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="65289-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="65289-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="65289-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="65289-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="65289-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="65289-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="65289-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="65289-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="65289-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="65289-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="65289-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="65289-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="65289-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="65289-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="65289-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="65289-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="65289-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="65289-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="65289-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="65289-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="65289-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="65289-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="65289-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="65289-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="65289-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="65289-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="65289-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="65289-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="65289-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="65289-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="65289-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="65289-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="65289-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="65289-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="65289-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="65289-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="65289-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="65289-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="65289-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="65289-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="65289-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="65289-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="65289-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="65289-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="65289-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="65289-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="65289-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="65289-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="65289-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="65289-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="65289-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="65289-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="65289-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="65289-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="65289-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="65289-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="65289-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="65289-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="65289-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="65289-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="65289-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="65289-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="65289-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="65289-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="65289-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="65289-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="65289-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="65289-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="65289-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="65289-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="65289-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="65289-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="65289-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="65289-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="65289-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="65289-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="65289-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65289-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="65289-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="65289-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="65289-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65289-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="65289-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="65289-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="65289-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="65289-855">Ver también</span><span class="sxs-lookup"><span data-stu-id="65289-855">See also</span></span>

<span data-ttu-id="65289-856">Para obtener información detallada acerca de implementación específico e información funcional acerca el proveedor Microsoft OLE DB para ODBC, consulte la [Guía del programador de OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) o visite el [Centro de desarrolladores de plataforma de datos](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="65289-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

