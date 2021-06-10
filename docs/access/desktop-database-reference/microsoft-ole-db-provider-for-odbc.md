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
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="10342-102">Proveedor de Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="10342-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="10342-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10342-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10342-p101">Para un programador de ADO o RDS, un mundo ideal sería aquel en que cada origen de datos expusiera una interfaz OLE DB, de modo que ADO pudiera llamar directamente al origen de datos. Aunque cada vez más proveedores de bases de datos están implementando interfaces OLE DB, algunos orígenes de datos aún no están expuestos de esta forma. Sin embargo, es posible obtener acceso a prácticamente todos los sistemas DBMS que se usan en la actualidad a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="10342-107">Los controladores ODBC están disponibles para todos los principales DBMS que se utilizan hoy en día, incluidos Microsoft SQL Server, Microsoft Access (motor de bases de datos Microsoft Jet) y Microsoft FoxPro, además de otros productos de base de datos no pertenecientes a Microsoft, como Oracle.</span><span class="sxs-lookup"><span data-stu-id="10342-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="10342-p102">Sin embargo, el Proveedor Microsoft ODBC permite a ADO conectarse a cualquier origen de datos ODBC. El proveedor es de subprocesamiento libre y está habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="10342-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="10342-p103">El proveedor admite transacciones, aunque los diferentes motores DBMS ofrecen diferentes tipos de compatibilidad con ellas. Por ejemplo, Microsoft Access admite las transacciones anidadas de hasta cinco niveles.</span><span class="sxs-lookup"><span data-stu-id="10342-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="10342-112">Éste es el proveedor predeterminado para ADO y admite todas las propiedades y los métodos ADO dependientes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="10342-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="10342-113">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="10342-113">Connection String Parameters</span></span>

<span data-ttu-id="10342-114">Para conectar con este proveedor, establezca el argumento **Provider=** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="10342-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="10342-115">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="10342-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="10342-116">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="10342-116">Typical Connection String</span></span>

<span data-ttu-id="10342-117">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="10342-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="10342-118">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="10342-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10342-119">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="10342-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="10342-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="10342-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="10342-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="10342-122">Especifica el Proveedor OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="10342-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="10342-124">Especifica el nombre del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="10342-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="10342-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="10342-126">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="10342-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="10342-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="10342-128">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="10342-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="10342-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="10342-130">Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</span><span class="sxs-lookup"><span data-stu-id="10342-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10342-131">Dado que éste es el proveedor predeterminado para ADO, si se omite el parámetro **Provider=** de la cadena de conexión, ADO intentará establecer una conexión con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="10342-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="10342-p104">El proveedor no admite ningún parámetro de conexión específico además de los definidos por ADO. No obstante, pasará cualquier parámetro de conexión que no sea de ADO al controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="10342-p105">Dado que se puede omitir el parámetro **Provider**, es posible elaborar una cadena de conexión ADO idéntica a una cadena de conexión ODBC para el mismo origen de datos. Utilice los mismos nombres de parámetro (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), los valores y la sintaxis que cuando elabora una cadena de conexión ODBC. Es posible conectar con o sin un nombre de origen de datos predefinido (DSN) o un FileDSN.</span><span class="sxs-lookup"><span data-stu-id="10342-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="10342-137">**Sintaxis con un DSN o un FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="10342-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="10342-138">**Sintaxis sin ningún DSN (conexión sin DSN):**</span><span class="sxs-lookup"><span data-stu-id="10342-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="10342-p106">Si se utiliza un **DSN** o un **FileDSN**, debe definirse mediante el Administrador de origen de datos ODBC del Panel de control de Windows. En Microsoft Windows 2000, el Administrador ODBC se encuentra en Herramientas administrativas. En versiones anteriores de Windows, el icono Administrador ODBC se denomina **ODBC de 32 bits** o simplemente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="10342-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="10342-142">Como alternativa al establecimiento de un **DSN**, puede especificar el controlador ODBC (**DRIVER=**), como "SQL Server;" el nombre del servidor (**SERVER=**); y el nombre de la base de datos (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="10342-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="10342-143">También puede especificar un nombre de cuenta de usuario (**UID=**) y la contraseña para esa cuenta (**PWD=**) en los parámetros específicos de ODBC o en los parámetros estándar *user* y *password* definidos por ADO.</span><span class="sxs-lookup"><span data-stu-id="10342-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="10342-144">Aunque una **definición de DSN** ya  especifica una base de datos, puede especificar un parámetro *de* base de datos además de **un DSN** para conectarse a una base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="10342-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="10342-145">Es una buena idea incluir siempre *el* parámetro *database* cuando se usa un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="10342-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="10342-146">Eso garantizará la conexión a la base de datos adecuada en caso de que otro usuario haya modificado el parámetro desde la última vez que se comprobó la definición **DSN**.</span><span class="sxs-lookup"><span data-stu-id="10342-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="10342-147">Propiedades Connection específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="10342-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="10342-p108">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="10342-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10342-150">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="10342-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="10342-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="10342-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-152">Procedimientos accesibles</span><span class="sxs-lookup"><span data-stu-id="10342-152">Accessible Procedures</span></span><br />
<span data-ttu-id="10342-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="10342-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="10342-154">Indica si el usuario tiene acceso a procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="10342-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-155">Tablas accesibles</span><span class="sxs-lookup"><span data-stu-id="10342-155">Accessible Tables</span></span><br />
<span data-ttu-id="10342-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="10342-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="10342-157">Indica si el usuario tiene permiso para ejecutar instrucciones SELECT en las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="10342-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-158">Instrucciones Active</span><span class="sxs-lookup"><span data-stu-id="10342-158">Active Statements</span></span><br />
<span data-ttu-id="10342-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="10342-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="10342-160">Indica el número de controladores que puede admitir un controlador ODBC en una conexión.</span><span class="sxs-lookup"><span data-stu-id="10342-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-161">Nombre del controlador</span><span class="sxs-lookup"><span data-stu-id="10342-161">Driver Name</span></span><br />
<span data-ttu-id="10342-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="10342-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="10342-163">Indica el nombre de archivo del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-164">Versión ODBC del controlador</span><span class="sxs-lookup"><span data-stu-id="10342-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="10342-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="10342-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="10342-166">Indica la versión de ODBC que admite este controlador.</span><span class="sxs-lookup"><span data-stu-id="10342-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-167">Uso de archivos</span><span class="sxs-lookup"><span data-stu-id="10342-167">File Usage</span></span><br />
<span data-ttu-id="10342-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="10342-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="10342-169">Indica cómo trata el controlador a un archivo de un origen de datos, como una tabla o como un catálogo.</span><span class="sxs-lookup"><span data-stu-id="10342-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-170">Cláusula Like Escape</span><span class="sxs-lookup"><span data-stu-id="10342-170">Like Escape Clause</span></span><br />
<span data-ttu-id="10342-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="10342-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="10342-172">Indica si el controlador admite la definición y el uso de un carácter de escape para el carácter de porcentaje (%) y de un carácter de subrayado (_) en el predicado LIKE de una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="10342-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-173">Columnas máximas en grupo por</span><span class="sxs-lookup"><span data-stu-id="10342-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="10342-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="10342-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="10342-175">Indica el número máximo de columnas que se puede enumerar en la cláusula GROUP BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="10342-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-176">Columnas máximas en índice</span><span class="sxs-lookup"><span data-stu-id="10342-176">Max Columns in Index</span></span><br />
<span data-ttu-id="10342-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="10342-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="10342-178">Indica el número máximo de columnas que puede ser incluido en un índice.</span><span class="sxs-lookup"><span data-stu-id="10342-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-179">Columnas máximas en orden por</span><span class="sxs-lookup"><span data-stu-id="10342-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="10342-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="10342-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="10342-181">Indica el número máximo de columnas que se puede enumerar en la cláusula ORDER BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="10342-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-182">Columnas máximas en Seleccionar</span><span class="sxs-lookup"><span data-stu-id="10342-182">Max Columns in Select</span></span><br />
<span data-ttu-id="10342-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="10342-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="10342-184">Indica el número máximo de columnas que se puede enumerar en la parte SELECT de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="10342-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-185">Columnas máximas en tabla</span><span class="sxs-lookup"><span data-stu-id="10342-185">Max Columns in Table</span></span><br />
<span data-ttu-id="10342-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="10342-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="10342-187">Indica el número máximo de columnas permitido en una tabla.</span><span class="sxs-lookup"><span data-stu-id="10342-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-188">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="10342-188">Numeric Functions</span></span><br />
<span data-ttu-id="10342-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10342-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10342-p109">Indica las funciones numéricas admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-192">Funcionalidades de unión externa</span><span class="sxs-lookup"><span data-stu-id="10342-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="10342-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="10342-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="10342-194">Indica los tipos de combinaciones externas admitidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="10342-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-195">Combinaciones externas</span><span class="sxs-lookup"><span data-stu-id="10342-195">Outer Joins</span></span><br />
<span data-ttu-id="10342-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="10342-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="10342-197">Indica si el proveedor admite combinaciones externas.</span><span class="sxs-lookup"><span data-stu-id="10342-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-198">Caracteres especiales</span><span class="sxs-lookup"><span data-stu-id="10342-198">Special Characters</span></span><br />
<span data-ttu-id="10342-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="10342-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="10342-200">Indica qué caracteres tienen un significado especial para el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-201">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="10342-201">Stored Procedures</span></span><br />
<span data-ttu-id="10342-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="10342-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="10342-203">Indica si hay procedimientos almacenados disponibles para ser utilizados con este controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-204">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="10342-204">String Functions</span></span><br />
<span data-ttu-id="10342-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10342-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10342-p110">Indica qué funciones de cadena son admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-208">Funciones del sistema</span><span class="sxs-lookup"><span data-stu-id="10342-208">System Functions</span></span><br />
<span data-ttu-id="10342-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10342-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10342-p111">Indica las funciones del sistema admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-212">Funciones de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="10342-212">Time/Date Functions</span></span><br />
<span data-ttu-id="10342-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10342-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10342-p112">Indica las funciones de fecha y hora admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-216">SQL Compatibilidad con gramática</span><span class="sxs-lookup"><span data-stu-id="10342-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="10342-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="10342-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="10342-218">Indica la gramática SQL admitida por el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="10342-219">Propiedades Recordset y Command específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="10342-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="10342-p113">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección **Properties** de los objetos **Recordset** y **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="10342-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10342-222">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="10342-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="10342-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="10342-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-224">Actualizaciones/eliminaciones/inserciones basadas en consultas</span><span class="sxs-lookup"><span data-stu-id="10342-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="10342-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="10342-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="10342-226">Indica si se pueden realizar actualizaciones, eliminaciones e inserciones mediante consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="10342-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-227">Tipo de simultaneidad ODBC</span><span class="sxs-lookup"><span data-stu-id="10342-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="10342-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="10342-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="10342-229">Indica el método utilizado para minimizar los problemas potenciales causados por el intento de dos usuarios de obtener acceso a los mismos datos del origen de datos de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="10342-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-230">Accesibilidad blob en Forward-Only cursor</span><span class="sxs-lookup"><span data-stu-id="10342-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="10342-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="10342-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="10342-232">Indica si es posible obtener acceso a <strong>campos</strong> BLOB cuando se utiliza un cursor de sólo avance.</span><span class="sxs-lookup"><span data-stu-id="10342-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-233">Incluir SQL_FLOAT, SQL_DOUBLE y SQL_REAL en las cláusulas WHERE de QBU</span><span class="sxs-lookup"><span data-stu-id="10342-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="10342-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="10342-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="10342-235">Indica si se pueden incluir valores SQL_FLOAT, SQL_DOUBLE y SQL_REAL en una cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="10342-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-236">Posición en la última fila después de insertar</span><span class="sxs-lookup"><span data-stu-id="10342-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="10342-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="10342-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="10342-238">Indica que tras haber insertado un nuevo registro en una tabla, la última fila de la misma se convertirá en la fila actual.</span><span class="sxs-lookup"><span data-stu-id="10342-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="10342-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="10342-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="10342-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="10342-241">Indica si la interfaz <strong>IRowsetChange</strong> admite información ampliada.</span><span class="sxs-lookup"><span data-stu-id="10342-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-242">Tipo de cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="10342-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="10342-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="10342-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="10342-244">Indica el tipo de cursor usado por el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="10342-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-245">Generar un conjunto de filas que se puede serializar</span><span class="sxs-lookup"><span data-stu-id="10342-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="10342-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="10342-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="10342-247">Indica que el controlador ODBC genera un conjunto de registros que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="10342-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="10342-248">Texto del comando</span><span class="sxs-lookup"><span data-stu-id="10342-248">Command Text</span></span>

<span data-ttu-id="10342-249">La forma de utilizar el objeto [Command](command-object-ado.md) depende en gran medida del origen de datos y del tipo de consulta o instrucción de comando que acepte.</span><span class="sxs-lookup"><span data-stu-id="10342-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="10342-p114">ODBC proporciona una sintaxis específica para llamar a los procedimientos almacenados. Para la propiedad [CommandText](commandtext-property-ado.md) de un objeto **Command**, el argumento *CommandText* del método **Execute** de un objeto [Connection](connection-object-ado.md) o el argumento *Source* del método **Open** de un objeto [Recordset](recordset-object-ado.md), pasa una cadena con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="10342-p114">ODBC provides a specific syntax for calling stored procedures. For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="10342-p115">Cada **?** hace referencia a un objeto de la colección [Parameters](parameters-collection-ado.md). El primer **?** hace referencia a **Parameters**(0), el siguiente **?** a **Parameters**(1) y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="10342-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="10342-p116">Las referencias del parámetro son opcionales y dependen de la estructura del procedimiento almacenado. Si desea llamar a un procedimiento almacenado que no define parámetros, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="10342-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="10342-259">Si tiene dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="10342-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="10342-p117">Si el procedimiento almacenado va a devolver un valor, el valor devuelto se trata como otro parámetro. Si no dispone de parámetros de consulta pero tiene un valor devuelto, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="10342-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="10342-262">Por último, si tiene un valor devuelto y dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="10342-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="10342-263">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="10342-263">Recordset Behavior</span></span>

<span data-ttu-id="10342-264">En las tablas siguientes se enumeran los métodos y las propiedades ADO estándar disponibles en un objeto **Recordset** abierto con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="10342-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="10342-265">Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección **Properties** del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.</span><span class="sxs-lookup"><span data-stu-id="10342-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="10342-266">Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="10342-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="10342-267">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10342-267">Property</span></span></p></th>
<th><p><span data-ttu-id="10342-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="10342-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="10342-269">Dinámico</span><span class="sxs-lookup"><span data-stu-id="10342-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="10342-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="10342-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="10342-271">Estática</span><span class="sxs-lookup"><span data-stu-id="10342-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="10342-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="10342-273">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-273">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-274">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-274">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-275">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-276">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="10342-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="10342-278">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-278">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-279">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-279">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-280">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-281">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="10342-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="10342-283">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-284">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-285">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-286">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="10342-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="10342-288">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-289">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-290">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-291">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="10342-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="10342-293">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-293">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-294">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-294">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-295">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-296">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="10342-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="10342-298">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-299">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-300">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-301">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="10342-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="10342-303">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-304">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-305">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-306">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="10342-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="10342-308">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-309">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-310">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-311">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="10342-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="10342-313">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-314">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-315">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-316">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="10342-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="10342-318">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-319">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-320">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-321">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="10342-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="10342-323">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-324">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-325">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-326">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="10342-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="10342-328">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-329">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-330">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-331">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="10342-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="10342-333">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-334">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-335">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-336">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="10342-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="10342-338">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-339">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-339">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-340">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-341">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="10342-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="10342-343">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-344">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-345">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-346">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="10342-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="10342-348">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-349">no disponible</span><span class="sxs-lookup"><span data-stu-id="10342-349">not available</span></span></p></td>
<td><p><span data-ttu-id="10342-350">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-351">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="10342-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="10342-353">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-354">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-355">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="10342-356">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10342-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-357"><a href="state-property-ado.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="10342-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="10342-358">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-359">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-360">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-361">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-362"><a href="status-property-ado-recordset.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="10342-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="10342-363">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-364">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-365">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="10342-366">solo lectura</span><span class="sxs-lookup"><span data-stu-id="10342-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10342-367">Las propiedades [AbsolutePosition](absoluteposition-property-ado.md) y [AbsolutePage](absolutepage-property-ado.md) son de sólo escritura cuando se utiliza ADO con la versión 1.0 del Proveedor de Microsoft OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="10342-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="10342-368">Disponibilidad de métodos estándar **Recordset** ADO:</span><span class="sxs-lookup"><span data-stu-id="10342-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="10342-369">Método</span><span class="sxs-lookup"><span data-stu-id="10342-369">Method</span></span></p></th>
<th><p><span data-ttu-id="10342-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="10342-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="10342-371">Dinámico</span><span class="sxs-lookup"><span data-stu-id="10342-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="10342-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="10342-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="10342-373">Estática</span><span class="sxs-lookup"><span data-stu-id="10342-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="10342-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="10342-375">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-376">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-377">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-378">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="10342-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="10342-380">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-381">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-382">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-383">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="10342-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="10342-385">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-386">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-387">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-388">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="10342-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="10342-390">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-391">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-392">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-393">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="10342-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="10342-395">No</span><span class="sxs-lookup"><span data-stu-id="10342-395">No</span></span></p></td>
<td><p><span data-ttu-id="10342-396">No</span><span class="sxs-lookup"><span data-stu-id="10342-396">No</span></span></p></td>
<td><p><span data-ttu-id="10342-397">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-398">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="10342-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="10342-400">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-401">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-402">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-403">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-404"><a href="delete-method-ado-recordset.md">Eliminar</a></span><span class="sxs-lookup"><span data-stu-id="10342-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="10342-405">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-406">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-407">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-408">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="10342-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="10342-410">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-411">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-412">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-413">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="10342-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="10342-415">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-416">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-417">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-418">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="10342-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="10342-420">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-421">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-422">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-423">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="10342-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="10342-425">No</span><span class="sxs-lookup"><span data-stu-id="10342-425">No</span></span></p></td>
<td><p><span data-ttu-id="10342-426">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-427">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-428">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="10342-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="10342-430">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-431">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-432">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-433">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="10342-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="10342-435">No</span><span class="sxs-lookup"><span data-stu-id="10342-435">No</span></span></p></td>
<td><p><span data-ttu-id="10342-436">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-437">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-438">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="10342-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="10342-440">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-441">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-442">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-443">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="10342-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="10342-445">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-446">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-447">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-448">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="10342-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="10342-450">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-451">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-452">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-453">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-454"><a href="resync-method-ado.md">Volver a sincronizar</a></span><span class="sxs-lookup"><span data-stu-id="10342-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="10342-455">No</span><span class="sxs-lookup"><span data-stu-id="10342-455">No</span></span></p></td>
<td><p><span data-ttu-id="10342-456">No</span><span class="sxs-lookup"><span data-stu-id="10342-456">No</span></span></p></td>
<td><p><span data-ttu-id="10342-457">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-458">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-459"><a href="supports-method-ado.md">Compatible</a></span><span class="sxs-lookup"><span data-stu-id="10342-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="10342-460">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-461">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-462">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-463">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-464"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="10342-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="10342-465">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-466">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-467">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-468">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="10342-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="10342-470">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-471">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-472">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="10342-473">Sí</span><span class="sxs-lookup"><span data-stu-id="10342-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10342-474">\*No compatible con las bases de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="10342-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="10342-475">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="10342-475">Dynamic Properties</span></span>

<span data-ttu-id="10342-476">El Proveedor OLE DB para ODBC inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="10342-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="10342-p118">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="10342-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="10342-481">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="10342-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="10342-482">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="10342-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10342-483">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="10342-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="10342-484">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="10342-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="10342-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="10342-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="10342-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="10342-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="10342-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="10342-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="10342-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="10342-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="10342-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="10342-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="10342-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="10342-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="10342-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="10342-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="10342-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="10342-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="10342-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="10342-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="10342-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="10342-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="10342-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="10342-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="10342-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="10342-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="10342-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="10342-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="10342-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="10342-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="10342-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="10342-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="10342-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="10342-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="10342-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="10342-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="10342-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="10342-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="10342-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="10342-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="10342-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="10342-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="10342-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="10342-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="10342-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="10342-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="10342-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="10342-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="10342-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="10342-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="10342-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="10342-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="10342-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="10342-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="10342-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="10342-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="10342-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="10342-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="10342-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="10342-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="10342-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="10342-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="10342-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="10342-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="10342-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="10342-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="10342-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="10342-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-529">Ubicación</span><span class="sxs-lookup"><span data-stu-id="10342-529">Location</span></span></p></td>
<td><p><span data-ttu-id="10342-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="10342-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="10342-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="10342-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="10342-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="10342-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="10342-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="10342-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="10342-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="10342-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="10342-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="10342-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="10342-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="10342-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-539">Mode</span><span class="sxs-lookup"><span data-stu-id="10342-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="10342-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="10342-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="10342-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="10342-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="10342-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="10342-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="10342-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="10342-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="10342-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="10342-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10342-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="10342-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="10342-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="10342-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="10342-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="10342-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="10342-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="10342-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="10342-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="10342-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="10342-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="10342-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="10342-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="10342-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="10342-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="10342-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="10342-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="10342-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10342-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="10342-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="10342-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="10342-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="10342-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="10342-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="10342-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="10342-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="10342-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="10342-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-565">Password</span><span class="sxs-lookup"><span data-stu-id="10342-565">Password</span></span></p></td>
<td><p><span data-ttu-id="10342-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="10342-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="10342-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="10342-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="10342-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="10342-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="10342-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="10342-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="10342-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="10342-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="10342-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="10342-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="10342-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="10342-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="10342-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="10342-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="10342-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="10342-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="10342-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="10342-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="10342-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="10342-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="10342-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="10342-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="10342-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="10342-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="10342-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="10342-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="10342-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="10342-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="10342-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="10342-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="10342-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="10342-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="10342-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="10342-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="10342-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="10342-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="10342-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="10342-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="10342-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="10342-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="10342-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="10342-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="10342-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="10342-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="10342-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="10342-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="10342-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="10342-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="10342-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="10342-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="10342-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="10342-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="10342-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="10342-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="10342-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="10342-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="10342-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-605">User ID</span><span class="sxs-lookup"><span data-stu-id="10342-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="10342-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="10342-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-607">User Name</span><span class="sxs-lookup"><span data-stu-id="10342-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="10342-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="10342-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="10342-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="10342-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="10342-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="10342-611">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="10342-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="10342-612">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="10342-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10342-613">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="10342-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="10342-614">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="10342-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="10342-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="10342-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="10342-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="10342-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="10342-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10342-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="10342-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="10342-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="10342-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="10342-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="10342-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="10342-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="10342-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="10342-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="10342-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="10342-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10342-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="10342-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="10342-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="10342-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="10342-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10342-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="10342-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="10342-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10342-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="10342-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="10342-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="10342-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="10342-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="10342-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10342-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="10342-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10342-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10342-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="10342-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10342-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10342-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="10342-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10342-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="10342-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="10342-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="10342-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="10342-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="10342-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="10342-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="10342-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="10342-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10342-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="10342-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10342-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10342-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="10342-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10342-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10342-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="10342-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10342-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10342-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="10342-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10342-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="10342-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10342-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="10342-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10342-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10342-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="10342-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10342-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10342-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="10342-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10342-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10342-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10342-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10342-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="10342-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10342-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="10342-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="10342-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="10342-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="10342-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="10342-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="10342-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="10342-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="10342-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="10342-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="10342-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="10342-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="10342-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="10342-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="10342-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="10342-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="10342-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="10342-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="10342-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="10342-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="10342-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="10342-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="10342-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="10342-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="10342-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10342-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="10342-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="10342-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10342-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="10342-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="10342-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="10342-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="10342-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="10342-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="10342-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="10342-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="10342-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="10342-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="10342-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="10342-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="10342-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="10342-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="10342-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10342-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="10342-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="10342-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="10342-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10342-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="10342-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="10342-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="10342-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10342-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="10342-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="10342-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="10342-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="10342-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="10342-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="10342-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="10342-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10342-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="10342-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10342-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="10342-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="10342-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="10342-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="10342-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="10342-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="10342-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="10342-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="10342-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="10342-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10342-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10342-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10342-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="10342-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="10342-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10342-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="10342-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="10342-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="10342-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="10342-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="10342-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="10342-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10342-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10342-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10342-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="10342-734">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="10342-734">Command Dynamic Properties</span></span>

<span data-ttu-id="10342-735">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="10342-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10342-736">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="10342-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="10342-737">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="10342-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10342-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="10342-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="10342-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="10342-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="10342-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="10342-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10342-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="10342-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="10342-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="10342-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="10342-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="10342-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="10342-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="10342-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="10342-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="10342-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="10342-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10342-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="10342-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="10342-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="10342-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="10342-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10342-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="10342-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="10342-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10342-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="10342-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="10342-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="10342-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="10342-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="10342-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10342-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="10342-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10342-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10342-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="10342-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10342-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10342-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="10342-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10342-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="10342-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="10342-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="10342-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="10342-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="10342-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="10342-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="10342-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="10342-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10342-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="10342-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10342-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10342-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="10342-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10342-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10342-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="10342-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10342-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10342-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="10342-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10342-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="10342-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10342-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="10342-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10342-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10342-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="10342-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10342-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10342-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="10342-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10342-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10342-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10342-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10342-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="10342-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10342-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="10342-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="10342-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="10342-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="10342-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="10342-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="10342-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="10342-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="10342-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="10342-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="10342-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="10342-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="10342-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="10342-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="10342-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="10342-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="10342-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="10342-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="10342-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="10342-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="10342-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="10342-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="10342-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="10342-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="10342-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10342-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="10342-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="10342-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10342-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="10342-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="10342-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="10342-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="10342-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="10342-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="10342-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="10342-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="10342-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="10342-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="10342-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="10342-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="10342-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="10342-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="10342-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="10342-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10342-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="10342-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="10342-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="10342-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10342-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="10342-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="10342-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="10342-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10342-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="10342-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="10342-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="10342-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="10342-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="10342-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="10342-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="10342-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10342-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="10342-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10342-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="10342-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="10342-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="10342-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="10342-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="10342-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="10342-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="10342-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="10342-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="10342-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="10342-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10342-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10342-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10342-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="10342-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="10342-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10342-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="10342-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10342-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="10342-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="10342-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="10342-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10342-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10342-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10342-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10342-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="10342-855">Vea también</span><span class="sxs-lookup"><span data-stu-id="10342-855">See also</span></span>

<span data-ttu-id="10342-856">Para obtener más información sobre la implementación específica y la información funcional sobre el proveedor microsoft OLE DB para ODBC, consulte la Guía del programador de [OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) o visite el Centro de [desarrolladores](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)de plataforma de datos .</span><span class="sxs-lookup"><span data-stu-id="10342-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

