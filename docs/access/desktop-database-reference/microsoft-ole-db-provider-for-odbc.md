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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288914"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="38b61-102">Proveedor de Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="38b61-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="38b61-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38b61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38b61-p101">Para un programador de ADO o RDS, un mundo ideal sería aquel en que cada origen de datos expusiera una interfaz OLE DB, de modo que ADO pudiera llamar directamente al origen de datos. Aunque cada vez más proveedores de bases de datos están implementando interfaces OLE DB, algunos orígenes de datos aún no están expuestos de esta forma. Sin embargo, es posible obtener acceso a prácticamente todos los sistemas DBMS que se usan en la actualidad a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="38b61-107">Los controladores ODBC están disponibles para todos los principales DBMS que se utilizan hoy en día, incluidos Microsoft SQL Server, Microsoft Access (motor de bases de datos Microsoft Jet) y Microsoft FoxPro, además de otros productos de base de datos no pertenecientes a Microsoft, como Oracle.</span><span class="sxs-lookup"><span data-stu-id="38b61-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="38b61-p102">Sin embargo, el Proveedor Microsoft ODBC permite a ADO conectarse a cualquier origen de datos ODBC. El proveedor es de subprocesamiento libre y está habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="38b61-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="38b61-p103">El proveedor admite transacciones, aunque los diferentes motores DBMS ofrecen diferentes tipos de compatibilidad con ellas. Por ejemplo, Microsoft Access admite las transacciones anidadas de hasta cinco niveles.</span><span class="sxs-lookup"><span data-stu-id="38b61-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="38b61-112">Éste es el proveedor predeterminado para ADO y admite todas las propiedades y los métodos ADO dependientes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="38b61-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="38b61-113">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="38b61-113">Connection String Parameters</span></span>

<span data-ttu-id="38b61-114">Para conectar con este proveedor, establezca el argumento **Provider=** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="38b61-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="38b61-115">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="38b61-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="38b61-116">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="38b61-116">Typical Connection String</span></span>

<span data-ttu-id="38b61-117">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="38b61-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="38b61-118">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="38b61-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38b61-119">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="38b61-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="38b61-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="38b61-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="38b61-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="38b61-122">Especifica el Proveedor OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="38b61-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="38b61-124">Especifica el nombre del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="38b61-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="38b61-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="38b61-126">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="38b61-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="38b61-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="38b61-128">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="38b61-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="38b61-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="38b61-130">Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</span><span class="sxs-lookup"><span data-stu-id="38b61-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="38b61-131">Dado que éste es el proveedor predeterminado para ADO, si se omite el parámetro **Provider=** de la cadena de conexión, ADO intentará establecer una conexión con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="38b61-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="38b61-p104">El proveedor no admite ningún parámetro de conexión específico además de los definidos por ADO. No obstante, pasará cualquier parámetro de conexión que no sea de ADO al controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="38b61-p105">Dado que se puede omitir el parámetro **Provider**, es posible elaborar una cadena de conexión ADO idéntica a una cadena de conexión ODBC para el mismo origen de datos. Utilice los mismos nombres de parámetro (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), los valores y la sintaxis que cuando elabora una cadena de conexión ODBC. Es posible conectar con o sin un nombre de origen de datos predefinido (DSN) o un FileDSN.</span><span class="sxs-lookup"><span data-stu-id="38b61-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="38b61-137">**Sintaxis con un DSN o un FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="38b61-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="38b61-138">**Sintaxis sin ningún DSN (conexión sin DSN):**</span><span class="sxs-lookup"><span data-stu-id="38b61-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="38b61-p106">Si se utiliza un **DSN** o un **FileDSN**, debe definirse mediante el Administrador de origen de datos ODBC del Panel de control de Windows. En Microsoft Windows 2000, el Administrador ODBC se encuentra en Herramientas administrativas. En versiones anteriores de Windows, el icono Administrador ODBC se denomina **ODBC de 32 bits** o simplemente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="38b61-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="38b61-142">Como alternativa al establecimiento de un **DSN**, puede especificar el controlador ODBC (**DRIVER=**), como "SQL Server;" el nombre del servidor (**SERVER=**); y el nombre de la base de datos (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="38b61-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="38b61-143">También puede especificar un nombre de cuenta de usuario (**UID=**) y la contraseña para esa cuenta (**PWD=**) en los parámetros específicos de ODBC o en los parámetros estándar *user* y *password* definidos por ADO.</span><span class="sxs-lookup"><span data-stu-id="38b61-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="38b61-144">Aunque una **definición de DSN** ya   especifica una base de datos, puede especificar un parámetro de base de datos además de un **DSN** para conectarse a una base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="38b61-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="38b61-145">Es una buena idea incluir siempre el *parámetro* *de base de* datos cuando se usa un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="38b61-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="38b61-146">Eso garantizará la conexión a la base de datos adecuada en caso de que otro usuario haya modificado el parámetro desde la última vez que se comprobó la definición **DSN**.</span><span class="sxs-lookup"><span data-stu-id="38b61-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="38b61-147">Propiedades Connection específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="38b61-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="38b61-p108">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="38b61-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38b61-150">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="38b61-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="38b61-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="38b61-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-152">Procedimientos accesibles</span><span class="sxs-lookup"><span data-stu-id="38b61-152">Accessible Procedures</span></span><br />
<span data-ttu-id="38b61-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="38b61-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="38b61-154">Indica si el usuario tiene acceso a procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="38b61-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-155">Tablas accesibles</span><span class="sxs-lookup"><span data-stu-id="38b61-155">Accessible Tables</span></span><br />
<span data-ttu-id="38b61-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="38b61-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="38b61-157">Indica si el usuario tiene permiso para ejecutar instrucciones SELECT en las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="38b61-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-158">Instrucciones activas</span><span class="sxs-lookup"><span data-stu-id="38b61-158">Active Statements</span></span><br />
<span data-ttu-id="38b61-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="38b61-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="38b61-160">Indica el número de controladores que puede admitir un controlador ODBC en una conexión.</span><span class="sxs-lookup"><span data-stu-id="38b61-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-161">Nombre del controlador</span><span class="sxs-lookup"><span data-stu-id="38b61-161">Driver Name</span></span><br />
<span data-ttu-id="38b61-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="38b61-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="38b61-163">Indica el nombre de archivo del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-164">Driver ODBC Version</span><span class="sxs-lookup"><span data-stu-id="38b61-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="38b61-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="38b61-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="38b61-166">Indica la versión de ODBC que admite este controlador.</span><span class="sxs-lookup"><span data-stu-id="38b61-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-167">Uso de archivos</span><span class="sxs-lookup"><span data-stu-id="38b61-167">File Usage</span></span><br />
<span data-ttu-id="38b61-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="38b61-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="38b61-169">Indica cómo trata el controlador a un archivo de un origen de datos, como una tabla o como un catálogo.</span><span class="sxs-lookup"><span data-stu-id="38b61-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-170">Like Escape Clause</span><span class="sxs-lookup"><span data-stu-id="38b61-170">Like Escape Clause</span></span><br />
<span data-ttu-id="38b61-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="38b61-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="38b61-172">Indica si el controlador admite la definición y el uso de un carácter de escape para el carácter de porcentaje (%) y de un carácter de subrayado (_) en el predicado LIKE de una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="38b61-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-173">Max Columns in Group By</span><span class="sxs-lookup"><span data-stu-id="38b61-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="38b61-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="38b61-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="38b61-175">Indica el número máximo de columnas que se puede enumerar en la cláusula GROUP BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="38b61-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-176">Max Columns in Index</span><span class="sxs-lookup"><span data-stu-id="38b61-176">Max Columns in Index</span></span><br />
<span data-ttu-id="38b61-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="38b61-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="38b61-178">Indica el número máximo de columnas que puede ser incluido en un índice.</span><span class="sxs-lookup"><span data-stu-id="38b61-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-179">Max Columns in Order By</span><span class="sxs-lookup"><span data-stu-id="38b61-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="38b61-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="38b61-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="38b61-181">Indica el número máximo de columnas que se puede enumerar en la cláusula ORDER BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="38b61-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-182">Max Columns in Select</span><span class="sxs-lookup"><span data-stu-id="38b61-182">Max Columns in Select</span></span><br />
<span data-ttu-id="38b61-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="38b61-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="38b61-184">Indica el número máximo de columnas que se puede enumerar en la parte SELECT de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="38b61-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-185">Columnas máximas de la tabla</span><span class="sxs-lookup"><span data-stu-id="38b61-185">Max Columns in Table</span></span><br />
<span data-ttu-id="38b61-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="38b61-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="38b61-187">Indica el número máximo de columnas permitido en una tabla.</span><span class="sxs-lookup"><span data-stu-id="38b61-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-188">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="38b61-188">Numeric Functions</span></span><br />
<span data-ttu-id="38b61-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="38b61-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="38b61-p109">Indica las funciones numéricas admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-192">Capacidades de unión externa</span><span class="sxs-lookup"><span data-stu-id="38b61-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="38b61-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="38b61-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="38b61-194">Indica los tipos de combinaciones externas admitidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="38b61-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-195">Combinaciones externas</span><span class="sxs-lookup"><span data-stu-id="38b61-195">Outer Joins</span></span><br />
<span data-ttu-id="38b61-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="38b61-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="38b61-197">Indica si el proveedor admite combinaciones externas.</span><span class="sxs-lookup"><span data-stu-id="38b61-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-198">Caracteres especiales</span><span class="sxs-lookup"><span data-stu-id="38b61-198">Special Characters</span></span><br />
<span data-ttu-id="38b61-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="38b61-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="38b61-200">Indica qué caracteres tienen un significado especial para el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-201">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="38b61-201">Stored Procedures</span></span><br />
<span data-ttu-id="38b61-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="38b61-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="38b61-203">Indica si hay procedimientos almacenados disponibles para ser utilizados con este controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-204">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="38b61-204">String Functions</span></span><br />
<span data-ttu-id="38b61-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="38b61-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="38b61-p110">Indica qué funciones de cadena son admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-208">Funciones del sistema</span><span class="sxs-lookup"><span data-stu-id="38b61-208">System Functions</span></span><br />
<span data-ttu-id="38b61-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="38b61-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="38b61-p111">Indica las funciones del sistema admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-212">Funciones time/date</span><span class="sxs-lookup"><span data-stu-id="38b61-212">Time/Date Functions</span></span><br />
<span data-ttu-id="38b61-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="38b61-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="38b61-p112">Indica las funciones de fecha y hora admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-216">SQL gramática</span><span class="sxs-lookup"><span data-stu-id="38b61-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="38b61-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="38b61-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="38b61-218">Indica la gramática SQL admitida por el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="38b61-219">Propiedades Recordset y Command específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="38b61-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="38b61-p113">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección **Properties** de los objetos **Recordset** y **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="38b61-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38b61-222">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="38b61-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="38b61-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="38b61-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-224">Actualizaciones/eliminaciones/inserciones basadas en consultas</span><span class="sxs-lookup"><span data-stu-id="38b61-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="38b61-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="38b61-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="38b61-226">Indica si se pueden realizar actualizaciones, eliminaciones e inserciones mediante consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="38b61-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-227">Tipo de simultaneidad ODBC</span><span class="sxs-lookup"><span data-stu-id="38b61-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="38b61-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="38b61-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="38b61-229">Indica el método utilizado para minimizar los problemas potenciales causados por el intento de dos usuarios de obtener acceso a los mismos datos del origen de datos de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="38b61-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-230">Accesibilidad de BLOB en Forward-Only cursor</span><span class="sxs-lookup"><span data-stu-id="38b61-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="38b61-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="38b61-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="38b61-232">Indica si es posible obtener acceso a <strong>campos</strong> BLOB cuando se utiliza un cursor de sólo avance.</span><span class="sxs-lookup"><span data-stu-id="38b61-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-233">Incluir SQL_FLOAT, SQL_DOUBLE y SQL_REAL en las cláusulas WHERE de QBU</span><span class="sxs-lookup"><span data-stu-id="38b61-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="38b61-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="38b61-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="38b61-235">Indica si se pueden incluir valores SQL_FLOAT, SQL_DOUBLE y SQL_REAL en una cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="38b61-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-236">Posición en la última fila después de insertar</span><span class="sxs-lookup"><span data-stu-id="38b61-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="38b61-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="38b61-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="38b61-238">Indica que tras haber insertado un nuevo registro en una tabla, la última fila de la misma se convertirá en la fila actual.</span><span class="sxs-lookup"><span data-stu-id="38b61-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="38b61-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="38b61-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="38b61-241">Indica si la interfaz <strong>IRowsetChange</strong> admite información ampliada.</span><span class="sxs-lookup"><span data-stu-id="38b61-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-242">Tipo de cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="38b61-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="38b61-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="38b61-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="38b61-244">Indica el tipo de cursor usado por el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="38b61-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-245">Generar un conjunto de filas que se puede calcular como referencias</span><span class="sxs-lookup"><span data-stu-id="38b61-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="38b61-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="38b61-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="38b61-247">Indica que el controlador ODBC genera un conjunto de registros que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="38b61-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="38b61-248">Texto del comando</span><span class="sxs-lookup"><span data-stu-id="38b61-248">Command Text</span></span>

<span data-ttu-id="38b61-249">La forma de utilizar el objeto [Command](command-object-ado.md) depende en gran medida del origen de datos y del tipo de consulta o instrucción de comando que acepte.</span><span class="sxs-lookup"><span data-stu-id="38b61-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="38b61-p114">ODBC proporciona una sintaxis específica para llamar a los procedimientos almacenados. Para la propiedad [CommandText](commandtext-property-ado.md) de un objeto **Command**, el argumento *CommandText* del método **Execute** de un objeto [Connection](connection-object-ado.md) o el argumento *Source* del método **Open** de un objeto [Recordset](recordset-object-ado.md), pasa una cadena con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="38b61-p114">ODBC provides a specific syntax for calling stored procedures. For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="38b61-252">Cada **?**</span><span class="sxs-lookup"><span data-stu-id="38b61-252">Each **?**</span></span> <span data-ttu-id="38b61-253">hace referencia a un objeto de la colección [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="38b61-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="38b61-254">El primer **?**</span><span class="sxs-lookup"><span data-stu-id="38b61-254">The first **?**</span></span> <span data-ttu-id="38b61-255">references **Parameters**(0), the next **?**</span><span class="sxs-lookup"><span data-stu-id="38b61-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="38b61-256">parámetros **de** referencias (1), y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="38b61-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="38b61-p116">Las referencias del parámetro son opcionales y dependen de la estructura del procedimiento almacenado. Si desea llamar a un procedimiento almacenado que no define parámetros, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="38b61-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="38b61-259">Si tiene dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="38b61-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="38b61-p117">Si el procedimiento almacenado va a devolver un valor, el valor devuelto se trata como otro parámetro. Si no dispone de parámetros de consulta pero tiene un valor devuelto, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="38b61-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="38b61-262">Por último, si tiene un valor devuelto y dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="38b61-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="38b61-263">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="38b61-263">Recordset Behavior</span></span>

<span data-ttu-id="38b61-264">En las tablas siguientes se enumeran los métodos y las propiedades ADO estándar disponibles en un objeto **Recordset** abierto con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="38b61-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="38b61-265">Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección **Properties** del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.</span><span class="sxs-lookup"><span data-stu-id="38b61-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="38b61-266">Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="38b61-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="38b61-267">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38b61-267">Property</span></span></p></th>
<th><p><span data-ttu-id="38b61-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="38b61-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="38b61-269">Dinámico</span><span class="sxs-lookup"><span data-stu-id="38b61-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="38b61-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="38b61-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="38b61-271">Estática</span><span class="sxs-lookup"><span data-stu-id="38b61-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="38b61-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-273">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-273">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-274">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-274">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-275">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-276">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="38b61-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-278">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-278">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-279">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-279">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-280">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-281">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="38b61-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-283">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-284">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-285">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-286">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="38b61-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-288">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-289">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-290">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-291">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="38b61-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-293">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-293">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-294">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-294">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-295">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-296">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="38b61-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-298">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-299">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-300">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-301">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="38b61-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-303">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-304">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-305">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-306">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="38b61-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-308">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-309">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-310">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-311">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="38b61-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-313">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-314">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-315">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-316">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-317"><a href="filter-property-ado.md">Filtro</a></span><span class="sxs-lookup"><span data-stu-id="38b61-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-318">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-319">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-320">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-321">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="38b61-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-323">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-324">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-325">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-326">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="38b61-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-328">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-329">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-330">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-331">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="38b61-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-333">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-334">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-335">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-336">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="38b61-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-338">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-339">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-339">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-340">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-341">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="38b61-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-343">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-344">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-345">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-346">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="38b61-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-348">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-349">no disponible</span><span class="sxs-lookup"><span data-stu-id="38b61-349">not available</span></span></p></td>
<td><p><span data-ttu-id="38b61-350">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-351">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="38b61-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-353">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-354">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-355">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="38b61-356">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="38b61-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="38b61-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-358">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-359">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-360">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-361">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-362"><a href="status-property-ado-recordset.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="38b61-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-363">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-364">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-365">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="38b61-366">solo lectura</span><span class="sxs-lookup"><span data-stu-id="38b61-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="38b61-367">Las propiedades [AbsolutePosition](absoluteposition-property-ado.md) y [AbsolutePage](absolutepage-property-ado.md) son de sólo escritura cuando se utiliza ADO con la versión 1.0 del Proveedor de Microsoft OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="38b61-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="38b61-368">Disponibilidad de métodos estándar **Recordset** ADO:</span><span class="sxs-lookup"><span data-stu-id="38b61-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="38b61-369">Método</span><span class="sxs-lookup"><span data-stu-id="38b61-369">Method</span></span></p></th>
<th><p><span data-ttu-id="38b61-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="38b61-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="38b61-371">Dinámico</span><span class="sxs-lookup"><span data-stu-id="38b61-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="38b61-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="38b61-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="38b61-373">Estática</span><span class="sxs-lookup"><span data-stu-id="38b61-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="38b61-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-375">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-376">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-377">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-378">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="38b61-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-380">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-381">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-382">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-383">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="38b61-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-385">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-386">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-387">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-388">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="38b61-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-390">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-391">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-392">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-393">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="38b61-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-395">No</span><span class="sxs-lookup"><span data-stu-id="38b61-395">No</span></span></p></td>
<td><p><span data-ttu-id="38b61-396">No</span><span class="sxs-lookup"><span data-stu-id="38b61-396">No</span></span></p></td>
<td><p><span data-ttu-id="38b61-397">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-398">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="38b61-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-400">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-401">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-402">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-403">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-404"><a href="delete-method-ado-recordset.md">Eliminar</a></span><span class="sxs-lookup"><span data-stu-id="38b61-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-405">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-406">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-407">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-408">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="38b61-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-410">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-411">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-412">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-413">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="38b61-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-415">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-416">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-417">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-418">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="38b61-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-420">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-421">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-422">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-423">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="38b61-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-425">No</span><span class="sxs-lookup"><span data-stu-id="38b61-425">No</span></span></p></td>
<td><p><span data-ttu-id="38b61-426">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-427">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-428">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="38b61-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-430">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-431">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-432">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-433">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="38b61-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-435">No</span><span class="sxs-lookup"><span data-stu-id="38b61-435">No</span></span></p></td>
<td><p><span data-ttu-id="38b61-436">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-437">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-438">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="38b61-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="38b61-440">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-441">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-442">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-443">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="38b61-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-445">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-446">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-447">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-448">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="38b61-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-450">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-451">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-452">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-453">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-454"><a href="resync-method-ado.md">Volver a sincronizar</a></span><span class="sxs-lookup"><span data-stu-id="38b61-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-455">No</span><span class="sxs-lookup"><span data-stu-id="38b61-455">No</span></span></p></td>
<td><p><span data-ttu-id="38b61-456">No</span><span class="sxs-lookup"><span data-stu-id="38b61-456">No</span></span></p></td>
<td><p><span data-ttu-id="38b61-457">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-458">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-459"><a href="supports-method-ado.md">Compatible</a></span><span class="sxs-lookup"><span data-stu-id="38b61-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-460">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-461">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-462">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-463">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-464"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="38b61-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-465">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-466">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-467">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-468">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="38b61-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="38b61-470">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-471">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-472">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="38b61-473">Sí</span><span class="sxs-lookup"><span data-stu-id="38b61-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="38b61-474">\*No compatible con las bases de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="38b61-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="38b61-475">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="38b61-475">Dynamic Properties</span></span>

<span data-ttu-id="38b61-476">El Proveedor OLE DB para ODBC inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="38b61-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="38b61-p118">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="38b61-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="38b61-481">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="38b61-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="38b61-482">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="38b61-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38b61-483">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="38b61-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="38b61-484">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="38b61-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="38b61-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="38b61-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="38b61-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="38b61-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="38b61-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="38b61-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="38b61-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="38b61-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="38b61-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="38b61-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="38b61-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="38b61-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="38b61-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="38b61-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="38b61-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="38b61-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="38b61-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="38b61-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="38b61-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="38b61-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="38b61-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="38b61-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="38b61-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="38b61-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="38b61-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="38b61-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="38b61-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="38b61-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="38b61-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="38b61-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="38b61-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="38b61-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="38b61-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="38b61-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="38b61-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="38b61-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="38b61-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="38b61-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="38b61-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="38b61-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="38b61-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="38b61-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="38b61-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="38b61-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="38b61-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="38b61-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="38b61-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="38b61-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="38b61-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="38b61-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="38b61-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="38b61-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="38b61-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="38b61-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="38b61-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="38b61-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="38b61-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="38b61-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="38b61-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="38b61-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="38b61-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="38b61-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="38b61-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="38b61-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="38b61-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="38b61-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-529">Ubicación</span><span class="sxs-lookup"><span data-stu-id="38b61-529">Location</span></span></p></td>
<td><p><span data-ttu-id="38b61-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="38b61-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="38b61-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="38b61-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="38b61-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="38b61-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="38b61-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="38b61-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="38b61-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="38b61-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="38b61-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="38b61-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="38b61-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="38b61-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-539">Mode</span><span class="sxs-lookup"><span data-stu-id="38b61-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="38b61-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="38b61-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="38b61-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="38b61-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="38b61-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="38b61-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="38b61-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="38b61-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="38b61-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="38b61-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="38b61-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="38b61-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="38b61-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="38b61-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="38b61-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="38b61-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="38b61-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="38b61-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="38b61-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="38b61-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="38b61-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="38b61-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="38b61-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="38b61-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="38b61-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="38b61-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="38b61-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="38b61-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="38b61-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="38b61-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="38b61-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="38b61-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="38b61-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="38b61-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="38b61-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="38b61-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="38b61-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="38b61-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-565">Password</span><span class="sxs-lookup"><span data-stu-id="38b61-565">Password</span></span></p></td>
<td><p><span data-ttu-id="38b61-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="38b61-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="38b61-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="38b61-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="38b61-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="38b61-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="38b61-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="38b61-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="38b61-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="38b61-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="38b61-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="38b61-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="38b61-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="38b61-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="38b61-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="38b61-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="38b61-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="38b61-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="38b61-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="38b61-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="38b61-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="38b61-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="38b61-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="38b61-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="38b61-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="38b61-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="38b61-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="38b61-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="38b61-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="38b61-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="38b61-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="38b61-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="38b61-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="38b61-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="38b61-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="38b61-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="38b61-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="38b61-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="38b61-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="38b61-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="38b61-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="38b61-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="38b61-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="38b61-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="38b61-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="38b61-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="38b61-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="38b61-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="38b61-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="38b61-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="38b61-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="38b61-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="38b61-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="38b61-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="38b61-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="38b61-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="38b61-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="38b61-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="38b61-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-605">User ID</span><span class="sxs-lookup"><span data-stu-id="38b61-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="38b61-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="38b61-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-607">User Name</span><span class="sxs-lookup"><span data-stu-id="38b61-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="38b61-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="38b61-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="38b61-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="38b61-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="38b61-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="38b61-611">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="38b61-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="38b61-612">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="38b61-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38b61-613">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="38b61-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="38b61-614">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="38b61-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="38b61-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="38b61-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="38b61-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="38b61-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="38b61-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="38b61-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="38b61-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="38b61-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="38b61-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="38b61-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="38b61-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="38b61-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="38b61-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="38b61-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="38b61-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="38b61-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="38b61-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="38b61-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="38b61-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="38b61-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="38b61-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="38b61-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="38b61-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="38b61-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="38b61-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="38b61-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="38b61-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="38b61-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="38b61-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="38b61-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="38b61-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="38b61-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="38b61-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="38b61-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="38b61-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="38b61-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="38b61-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="38b61-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="38b61-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="38b61-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="38b61-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="38b61-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="38b61-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="38b61-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="38b61-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="38b61-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="38b61-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="38b61-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="38b61-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="38b61-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="38b61-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="38b61-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="38b61-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="38b61-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="38b61-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="38b61-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="38b61-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="38b61-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="38b61-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="38b61-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="38b61-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="38b61-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="38b61-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="38b61-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="38b61-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="38b61-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="38b61-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="38b61-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="38b61-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="38b61-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="38b61-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="38b61-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="38b61-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="38b61-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="38b61-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="38b61-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="38b61-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="38b61-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="38b61-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="38b61-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="38b61-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="38b61-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="38b61-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="38b61-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="38b61-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="38b61-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="38b61-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="38b61-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="38b61-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="38b61-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="38b61-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="38b61-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="38b61-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="38b61-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="38b61-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="38b61-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="38b61-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="38b61-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="38b61-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="38b61-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="38b61-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="38b61-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="38b61-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="38b61-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="38b61-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="38b61-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="38b61-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="38b61-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="38b61-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="38b61-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="38b61-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="38b61-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="38b61-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="38b61-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="38b61-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="38b61-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="38b61-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="38b61-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="38b61-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="38b61-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="38b61-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="38b61-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="38b61-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="38b61-734">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="38b61-734">Command Dynamic Properties</span></span>

<span data-ttu-id="38b61-735">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="38b61-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38b61-736">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="38b61-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="38b61-737">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="38b61-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b61-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="38b61-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="38b61-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="38b61-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="38b61-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="38b61-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="38b61-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="38b61-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="38b61-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="38b61-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="38b61-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="38b61-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="38b61-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="38b61-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="38b61-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="38b61-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="38b61-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="38b61-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="38b61-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="38b61-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="38b61-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="38b61-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="38b61-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="38b61-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="38b61-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="38b61-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="38b61-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="38b61-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="38b61-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="38b61-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="38b61-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="38b61-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="38b61-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="38b61-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="38b61-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="38b61-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="38b61-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="38b61-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="38b61-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="38b61-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="38b61-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="38b61-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="38b61-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="38b61-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="38b61-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="38b61-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="38b61-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="38b61-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="38b61-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="38b61-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="38b61-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="38b61-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="38b61-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="38b61-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="38b61-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="38b61-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="38b61-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="38b61-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="38b61-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="38b61-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="38b61-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="38b61-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="38b61-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="38b61-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="38b61-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="38b61-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="38b61-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="38b61-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="38b61-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="38b61-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="38b61-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="38b61-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="38b61-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="38b61-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="38b61-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="38b61-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="38b61-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="38b61-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="38b61-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="38b61-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="38b61-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="38b61-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="38b61-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="38b61-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="38b61-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="38b61-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="38b61-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="38b61-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="38b61-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="38b61-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="38b61-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="38b61-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="38b61-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="38b61-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="38b61-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="38b61-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="38b61-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="38b61-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="38b61-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="38b61-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="38b61-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="38b61-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="38b61-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="38b61-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="38b61-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="38b61-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="38b61-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="38b61-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="38b61-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="38b61-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="38b61-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="38b61-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="38b61-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="38b61-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="38b61-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="38b61-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="38b61-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="38b61-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="38b61-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="38b61-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="38b61-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="38b61-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="38b61-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="38b61-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="38b61-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b61-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="38b61-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="38b61-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="38b61-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b61-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="38b61-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="38b61-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="38b61-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="38b61-855">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38b61-855">See also</span></span>

<span data-ttu-id="38b61-856">Para obtener más información sobre la implementación específica y la información funcional sobre el proveedor microsoft OLE DB para ODBC, consulte la Guía del programador de [OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) o visite el Centro para desarrolladores de [plataformas de datos.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="38b61-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

