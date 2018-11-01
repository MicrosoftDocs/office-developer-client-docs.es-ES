---
title: Proveedor de Microsoft OLE DB para ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66ef27165e6f5823cc97a295643dfc2ae5c205c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883186"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="a8a82-102">Proveedor de Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="a8a82-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="a8a82-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8a82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8a82-p101">Para un programador de ADO o RDS, un mundo ideal sería aquel en que cada origen de datos expusiera una interfaz OLE DB, de modo que ADO pudiera llamar directamente al origen de datos. Aunque cada vez más proveedores de bases de datos están implementando interfaces OLE DB, algunos orígenes de datos aún no están expuestos de esta forma. Sin embargo, es posible obtener acceso a prácticamente todos los sistemas DBMS que se usan en la actualidad a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="a8a82-107">Los controladores ODBC están disponibles para todos los principales DBMS que se utilizan hoy en día, incluidos Microsoft SQL Server, Microsoft Access (motor de bases de datos Microsoft Jet) y Microsoft FoxPro, además de otros productos de base de datos no pertenecientes a Microsoft, como Oracle.</span><span class="sxs-lookup"><span data-stu-id="a8a82-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="a8a82-p102">Sin embargo, el Proveedor Microsoft ODBC permite a ADO conectarse a cualquier origen de datos ODBC. El proveedor es de subprocesamiento libre y está habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="a8a82-p103">El proveedor admite transacciones, aunque los diferentes motores DBMS ofrecen diferentes tipos de compatibilidad con ellas. Por ejemplo, Microsoft Access admite las transacciones anidadas de hasta cinco niveles.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="a8a82-112">Éste es el proveedor predeterminado para ADO y admite todas las propiedades y los métodos ADO dependientes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a8a82-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="a8a82-113">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="a8a82-113">Connection String Parameters</span></span>

<span data-ttu-id="a8a82-114">Para conectar con este proveedor, establezca el argumento **Provider=** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="a8a82-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="a8a82-115">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="a8a82-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="a8a82-116">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="a8a82-116">Typical Connection String</span></span>

<span data-ttu-id="a8a82-117">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="a8a82-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="a8a82-118">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="a8a82-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8a82-119">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="a8a82-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="a8a82-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8a82-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="a8a82-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="a8a82-122">Especifica el Proveedor OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="a8a82-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="a8a82-124">Especifica el nombre del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="a8a82-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="a8a82-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="a8a82-126">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8a82-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="a8a82-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="a8a82-128">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8a82-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="a8a82-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="a8a82-130">Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</span><span class="sxs-lookup"><span data-stu-id="a8a82-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8a82-131">Dado que éste es el proveedor predeterminado para ADO, si se omite el parámetro **Provider=** de la cadena de conexión, ADO intentará establecer una conexión con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="a8a82-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="a8a82-p104">El proveedor no admite ningún parámetro de conexión específico además de los definidos por ADO. No obstante, pasará cualquier parámetro de conexión que no sea de ADO al controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="a8a82-p105">Dado que se puede omitir el parámetro **Provider**, es posible elaborar una cadena de conexión ADO idéntica a una cadena de conexión ODBC para el mismo origen de datos. Utilice los mismos nombres de parámetro (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), los valores y la sintaxis que cuando elabora una cadena de conexión ODBC. Es posible conectar con o sin un nombre de origen de datos predefinido (DSN) o un FileDSN.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="a8a82-137">**Sintaxis con un DSN o un FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="a8a82-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="a8a82-138">**Sintaxis sin ningún DSN (conexión sin DSN):**</span><span class="sxs-lookup"><span data-stu-id="a8a82-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="a8a82-p106">Si se utiliza un **DSN** o un **FileDSN**, debe definirse mediante el Administrador de origen de datos ODBC del Panel de control de Windows. En Microsoft Windows 2000, el Administrador ODBC se encuentra en Herramientas administrativas. En versiones anteriores de Windows, el icono Administrador ODBC se denomina **ODBC de 32 bits** o simplemente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="a8a82-142">Como alternativa al establecimiento de un **DSN**, puede especificar el controlador ODBC (**DRIVER=**), como "SQL Server;" el nombre del servidor (**SERVER=**); y el nombre de la base de datos (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="a8a82-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="a8a82-143">También puede especificar un nombre de cuenta de usuario (**UID=**) y la contraseña para esa cuenta (**PWD=**) en los parámetros específicos de ODBC o en los parámetros estándar *user* y *password* definidos por ADO.</span><span class="sxs-lookup"><span data-stu-id="a8a82-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="a8a82-144">Aunque una definición **DSN** ya especifica una base de datos, puede especificar *un* parámetro de *base de datos* además de un **DSN** para conectarse a una base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="a8a82-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="a8a82-145">Es una buena idea incluir siempre *el* parámetro de *base de datos* al utilizar un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="a8a82-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="a8a82-146">Eso garantizará la conexión a la base de datos adecuada en caso de que otro usuario haya modificado el parámetro desde la última vez que se comprobó la definición **DSN**.</span><span class="sxs-lookup"><span data-stu-id="a8a82-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="a8a82-147">Propiedades Connection específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="a8a82-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="a8a82-p108">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8a82-150">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8a82-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="a8a82-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8a82-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-152">Accessible Procedures</span><span class="sxs-lookup"><span data-stu-id="a8a82-152">Accessible Procedures</span></span><br />
<span data-ttu-id="a8a82-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="a8a82-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-154">Indica si el usuario tiene acceso a procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="a8a82-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-155">Tablas accesibles</span><span class="sxs-lookup"><span data-stu-id="a8a82-155">Accessible Tables</span></span><br />
<span data-ttu-id="a8a82-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="a8a82-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-157">Indica si el usuario tiene permiso para ejecutar instrucciones SELECT en las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a8a82-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-158">Instrucciones activas</span><span class="sxs-lookup"><span data-stu-id="a8a82-158">Active Statements</span></span><br />
<span data-ttu-id="a8a82-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="a8a82-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-160">Indica el número de controladores que puede admitir un controlador ODBC en una conexión.</span><span class="sxs-lookup"><span data-stu-id="a8a82-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-161">Nombre del controlador</span><span class="sxs-lookup"><span data-stu-id="a8a82-161">Driver Name</span></span><br />
<span data-ttu-id="a8a82-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="a8a82-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-163">Indica el nombre de archivo del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-164">Versión del controlador ODBC</span><span class="sxs-lookup"><span data-stu-id="a8a82-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="a8a82-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="a8a82-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-166">Indica la versión de ODBC que admite este controlador.</span><span class="sxs-lookup"><span data-stu-id="a8a82-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-167">Uso de archivos</span><span class="sxs-lookup"><span data-stu-id="a8a82-167">File Usage</span></span><br />
<span data-ttu-id="a8a82-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="a8a82-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-169">Indica cómo trata el controlador a un archivo de un origen de datos, como una tabla o como un catálogo.</span><span class="sxs-lookup"><span data-stu-id="a8a82-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-170">Al igual que la cláusula Escape</span><span class="sxs-lookup"><span data-stu-id="a8a82-170">Like Escape Clause</span></span><br />
<span data-ttu-id="a8a82-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="a8a82-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-172">Indica si el controlador admite la definición y el uso de un carácter de escape para el carácter de porcentaje (%) y de un carácter de subrayado (_) en el predicado LIKE de una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="a8a82-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-173">Max Columns in Group By</span><span class="sxs-lookup"><span data-stu-id="a8a82-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="a8a82-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="a8a82-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-175">Indica el número máximo de columnas que se puede enumerar en la cláusula GROUP BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="a8a82-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-176">Número máximo de columnas en el índice</span><span class="sxs-lookup"><span data-stu-id="a8a82-176">Max Columns in Index</span></span><br />
<span data-ttu-id="a8a82-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="a8a82-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-178">Indica el número máximo de columnas que puede ser incluido en un índice.</span><span class="sxs-lookup"><span data-stu-id="a8a82-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-179">Max Columns in Order By</span><span class="sxs-lookup"><span data-stu-id="a8a82-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="a8a82-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="a8a82-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-181">Indica el número máximo de columnas que se puede enumerar en la cláusula ORDER BY de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="a8a82-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-182">Número máximo de columnas en Seleccionar</span><span class="sxs-lookup"><span data-stu-id="a8a82-182">Max Columns in Select</span></span><br />
<span data-ttu-id="a8a82-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="a8a82-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-184">Indica el número máximo de columnas que se puede enumerar en la parte SELECT de una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="a8a82-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-185">Número máximo de columnas de tabla</span><span class="sxs-lookup"><span data-stu-id="a8a82-185">Max Columns in Table</span></span><br />
<span data-ttu-id="a8a82-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="a8a82-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-187">Indica el número máximo de columnas permitido en una tabla.</span><span class="sxs-lookup"><span data-stu-id="a8a82-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-188">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="a8a82-188">Numeric Functions</span></span><br />
<span data-ttu-id="a8a82-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a8a82-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-p109">Indica las funciones numéricas admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-192">Outer Join Capabilities</span><span class="sxs-lookup"><span data-stu-id="a8a82-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="a8a82-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="a8a82-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-194">Indica los tipos de combinaciones externas admitidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a8a82-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-195">Combinaciones externas</span><span class="sxs-lookup"><span data-stu-id="a8a82-195">Outer Joins</span></span><br />
<span data-ttu-id="a8a82-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="a8a82-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-197">Indica si el proveedor admite combinaciones externas.</span><span class="sxs-lookup"><span data-stu-id="a8a82-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-198">Caracteres especiales</span><span class="sxs-lookup"><span data-stu-id="a8a82-198">Special Characters</span></span><br />
<span data-ttu-id="a8a82-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="a8a82-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-200">Indica qué caracteres tienen un significado especial para el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-201">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="a8a82-201">Stored Procedures</span></span><br />
<span data-ttu-id="a8a82-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="a8a82-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-203">Indica si hay procedimientos almacenados disponibles para ser utilizados con este controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-204">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="a8a82-204">String Functions</span></span><br />
<span data-ttu-id="a8a82-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a8a82-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-p110">Indica qué funciones de cadena son admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-208">Funciones del sistema</span><span class="sxs-lookup"><span data-stu-id="a8a82-208">System Functions</span></span><br />
<span data-ttu-id="a8a82-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a8a82-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-p111">Indica las funciones del sistema admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-212">Funciones de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="a8a82-212">Time/Date Functions</span></span><br />
<span data-ttu-id="a8a82-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a8a82-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-p112">Indica las funciones de fecha y hora admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-216">Compatibilidad con la gramática SQL</span><span class="sxs-lookup"><span data-stu-id="a8a82-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="a8a82-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="a8a82-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-218">Indica la gramática SQL admitida por el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="a8a82-219">Propiedades Recordset y Command específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="a8a82-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="a8a82-p113">El Proveedor OLE DB para ODBC agrega varias propiedades a la colección **Properties** de los objetos **Recordset** y **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8a82-222">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8a82-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="a8a82-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8a82-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-224">Query Based Updates/Deletes/Inserts</span><span class="sxs-lookup"><span data-stu-id="a8a82-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="a8a82-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="a8a82-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-226">Indica si se pueden realizar actualizaciones, eliminaciones e inserciones mediante consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="a8a82-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-227">ODBC Concurrency Type</span><span class="sxs-lookup"><span data-stu-id="a8a82-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="a8a82-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="a8a82-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-229">Indica el método utilizado para minimizar los problemas potenciales causados por el intento de dos usuarios de obtener acceso a los mismos datos del origen de datos de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="a8a82-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-230">Accesibilidad BLOB en el cursor de sólo avance</span><span class="sxs-lookup"><span data-stu-id="a8a82-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="a8a82-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="a8a82-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-232">Indica si es posible obtener acceso a <strong>campos</strong> BLOB cuando se utiliza un cursor de sólo avance.</span><span class="sxs-lookup"><span data-stu-id="a8a82-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-233">Incluir SQL_FLOAT, SQL_DOUBLE y SQL_REAL en QBU WHERE clauses</span><span class="sxs-lookup"><span data-stu-id="a8a82-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="a8a82-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="a8a82-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-235">Indica si se pueden incluir valores SQL_FLOAT, SQL_DOUBLE y SQL_REAL en una cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="a8a82-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-236">Posición en la última fila después de insertar</span><span class="sxs-lookup"><span data-stu-id="a8a82-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="a8a82-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="a8a82-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-238">Indica que tras haber insertado un nuevo registro en una tabla, la última fila de la misma se convertirá en la fila actual.</span><span class="sxs-lookup"><span data-stu-id="a8a82-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="a8a82-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="a8a82-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-241">Indica si la interfaz <strong>IRowsetChange</strong> admite información ampliada.</span><span class="sxs-lookup"><span data-stu-id="a8a82-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-242">Tipo de Cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="a8a82-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="a8a82-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="a8a82-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-244">Indica el tipo de cursor usado por el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8a82-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-245">Generar un conjunto de filas que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="a8a82-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="a8a82-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="a8a82-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="a8a82-247">Indica que el controlador ODBC genera un conjunto de registros que se puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="a8a82-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="a8a82-248">Texto del comando</span><span class="sxs-lookup"><span data-stu-id="a8a82-248">Command Text</span></span>

<span data-ttu-id="a8a82-249">La forma de utilizar el objeto [Command](command-object-ado.md) depende en gran medida del origen de datos y del tipo de consulta o instrucción de comando que acepte.</span><span class="sxs-lookup"><span data-stu-id="a8a82-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="a8a82-250">ODBC proporciona una sintaxis específica para llamar a los procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="a8a82-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="a8a82-251">Para la propiedad [CommandText](commandtext-property-ado.md) de un objeto **Command** , el argumento *CommandText* del método **Execute** en un objeto [Connection](connection-object-ado.md) o el argumento *Source* en el método **Open** en un [objeto Recordset](recordset-object-ado.md) objeto, pasa en una cadena con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="a8a82-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="a8a82-p115">Cada **?** hace referencia a un objeto de la colección [Parameters](parameters-collection-ado.md). El primer **?** hace referencia a **Parameters**(0), el siguiente **?** a **Parameters**(1) y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="a8a82-p116">Las referencias del parámetro son opcionales y dependen de la estructura del procedimiento almacenado. Si desea llamar a un procedimiento almacenado que no define parámetros, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="a8a82-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="a8a82-259">Si tiene dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="a8a82-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="a8a82-p117">Si el procedimiento almacenado va a devolver un valor, el valor devuelto se trata como otro parámetro. Si no dispone de parámetros de consulta pero tiene un valor devuelto, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="a8a82-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="a8a82-262">Por último, si tiene un valor devuelto y dos parámetros de consulta, la cadena tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="a8a82-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="a8a82-263">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="a8a82-263">Recordset Behavior</span></span>

<span data-ttu-id="a8a82-264">En las tablas siguientes se enumeran los métodos y las propiedades ADO estándar disponibles en un objeto **Recordset** abierto con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="a8a82-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="a8a82-265">Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección **Properties** del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.</span><span class="sxs-lookup"><span data-stu-id="a8a82-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="a8a82-266">Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="a8a82-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="a8a82-267">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8a82-267">Property</span></span></p></th>
<th><p><span data-ttu-id="a8a82-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="a8a82-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="a8a82-269">Dinámico</span><span class="sxs-lookup"><span data-stu-id="a8a82-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="a8a82-270">Conjunto de claves</span><span class="sxs-lookup"><span data-stu-id="a8a82-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="a8a82-271">Estático</span><span class="sxs-lookup"><span data-stu-id="a8a82-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-273">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-273">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-274">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-274">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-275">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-276">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-278">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-278">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-279">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-279">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-280">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-281">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-283">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-284">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-285">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-286">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-288">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-289">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-290">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-291">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-293">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-293">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-294">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-294">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-295">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-296">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-298">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-299">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-300">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-301">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-303">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-304">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-305">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-306">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-308">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-309">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-310">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-311">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-313">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-314">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-315">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-316">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-318">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-319">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-320">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-321">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-323">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-324">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-325">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-326">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-328">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-329">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-330">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-331">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-333">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-334">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-335">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-336">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-338">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-339">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-339">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-340">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-341">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-343">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-344">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-345">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-346">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-348">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-349">no disponible</span><span class="sxs-lookup"><span data-stu-id="a8a82-349">not available</span></span></p></td>
<td><p><span data-ttu-id="a8a82-350">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-351">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-353">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-354">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-355">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="a8a82-356">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a8a82-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-358">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-359">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-360">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-361">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-363">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-364">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-365">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="a8a82-366">sólo lectura</span><span class="sxs-lookup"><span data-stu-id="a8a82-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8a82-367">Las propiedades [AbsolutePosition](absoluteposition-property-ado.md) y [AbsolutePage](absolutepage-property-ado.md) son de sólo escritura cuando se utiliza ADO con la versión 1.0 del Proveedor de Microsoft OLE DB para ODBC.</span><span class="sxs-lookup"><span data-stu-id="a8a82-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="a8a82-368">Disponibilidad de métodos estándar **Recordset** ADO:</span><span class="sxs-lookup"><span data-stu-id="a8a82-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="a8a82-369">Método</span><span class="sxs-lookup"><span data-stu-id="a8a82-369">Method</span></span></p></th>
<th><p><span data-ttu-id="a8a82-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="a8a82-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="a8a82-371">Dinámico</span><span class="sxs-lookup"><span data-stu-id="a8a82-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="a8a82-372">Conjunto de claves</span><span class="sxs-lookup"><span data-stu-id="a8a82-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="a8a82-373">Estático</span><span class="sxs-lookup"><span data-stu-id="a8a82-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-375">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-376">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-377">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-378">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-380">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-381">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-382">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-383">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-385">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-386">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-387">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-388">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-390">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-391">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-392">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-393">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-395">No</span><span class="sxs-lookup"><span data-stu-id="a8a82-395">No</span></span></p></td>
<td><p><span data-ttu-id="a8a82-396">No</span><span class="sxs-lookup"><span data-stu-id="a8a82-396">No</span></span></p></td>
<td><p><span data-ttu-id="a8a82-397">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-398">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-400">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-401">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-402">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-403">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-405">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-406">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-407">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-408">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-410">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-411">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-412">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-413">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-414"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-415">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-416">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-417">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-418">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-420">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-421">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-422">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-423">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-425">No</span><span class="sxs-lookup"><span data-stu-id="a8a82-425">No</span></span></p></td>
<td><p><span data-ttu-id="a8a82-426">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-427">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-428">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-430">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-431">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-432">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-433">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-435">No</span><span class="sxs-lookup"><span data-stu-id="a8a82-435">No</span></span></p></td>
<td><p><span data-ttu-id="a8a82-436">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-437">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-438">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="a8a82-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="a8a82-440">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-441">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-442">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-443">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-445">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-446">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-447">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-448">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-450">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-451">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-452">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-453">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-455">No</span><span class="sxs-lookup"><span data-stu-id="a8a82-455">No</span></span></p></td>
<td><p><span data-ttu-id="a8a82-456">No</span><span class="sxs-lookup"><span data-stu-id="a8a82-456">No</span></span></p></td>
<td><p><span data-ttu-id="a8a82-457">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-458">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-459"><a href="supports-method-ado.md">Admite</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-460">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-461">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-462">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-463">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-464"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-465">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-466">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-467">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-468">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="a8a82-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a8a82-470">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-471">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-472">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-473">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a82-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8a82-474">\*No compatible con las bases de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a8a82-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="a8a82-475">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="a8a82-475">Dynamic Properties</span></span>

<span data-ttu-id="a8a82-476">El Proveedor OLE DB para ODBC inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.</span><span class="sxs-lookup"><span data-stu-id="a8a82-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="a8a82-p118">Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a8a82-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="a8a82-481">Propiedades dinámicas de Connection</span><span class="sxs-lookup"><span data-stu-id="a8a82-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="a8a82-482">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="a8a82-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8a82-483">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a8a82-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a8a82-484">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a8a82-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="a8a82-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="a8a82-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="a8a82-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="a8a82-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="a8a82-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="a8a82-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="a8a82-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="a8a82-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="a8a82-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a8a82-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a8a82-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a8a82-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="a8a82-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="a8a82-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="a8a82-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="a8a82-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="a8a82-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="a8a82-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="a8a82-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="a8a82-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="a8a82-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="a8a82-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="a8a82-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a8a82-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="a8a82-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="a8a82-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="a8a82-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="a8a82-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="a8a82-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="a8a82-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="a8a82-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="a8a82-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="a8a82-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="a8a82-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a8a82-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a8a82-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="a8a82-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="a8a82-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="a8a82-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="a8a82-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="a8a82-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="a8a82-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="a8a82-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="a8a82-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="a8a82-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="a8a82-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="a8a82-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="a8a82-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="a8a82-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="a8a82-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="a8a82-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="a8a82-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="a8a82-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="a8a82-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="a8a82-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="a8a82-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a8a82-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a8a82-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a8a82-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="a8a82-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="a8a82-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="a8a82-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="a8a82-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="a8a82-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="a8a82-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-529">Location</span><span class="sxs-lookup"><span data-stu-id="a8a82-529">Location</span></span></p></td>
<td><p><span data-ttu-id="a8a82-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="a8a82-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="a8a82-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="a8a82-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="a8a82-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="a8a82-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="a8a82-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="a8a82-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="a8a82-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="a8a82-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="a8a82-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="a8a82-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="a8a82-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="a8a82-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-539">Mode</span><span class="sxs-lookup"><span data-stu-id="a8a82-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="a8a82-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="a8a82-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="a8a82-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="a8a82-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="a8a82-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="a8a82-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="a8a82-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a8a82-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a8a82-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="a8a82-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="a8a82-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="a8a82-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="a8a82-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="a8a82-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="a8a82-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="a8a82-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="a8a82-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a8a82-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="a8a82-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="a8a82-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="a8a82-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="a8a82-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="a8a82-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="a8a82-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="a8a82-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="a8a82-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="a8a82-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="a8a82-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a8a82-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="a8a82-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="a8a82-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="a8a82-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="a8a82-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="a8a82-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-565">Password</span><span class="sxs-lookup"><span data-stu-id="a8a82-565">Password</span></span></p></td>
<td><p><span data-ttu-id="a8a82-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="a8a82-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="a8a82-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="a8a82-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="a8a82-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="a8a82-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="a8a82-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="a8a82-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="a8a82-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="a8a82-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="a8a82-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="a8a82-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="a8a82-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a8a82-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="a8a82-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="a8a82-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a8a82-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="a8a82-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="a8a82-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="a8a82-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="a8a82-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="a8a82-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="a8a82-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="a8a82-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="a8a82-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="a8a82-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="a8a82-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="a8a82-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="a8a82-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="a8a82-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="a8a82-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="a8a82-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="a8a82-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="a8a82-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="a8a82-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="a8a82-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="a8a82-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a8a82-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="a8a82-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="a8a82-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="a8a82-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="a8a82-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="a8a82-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="a8a82-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="a8a82-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a8a82-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="a8a82-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="a8a82-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="a8a82-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="a8a82-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="a8a82-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="a8a82-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="a8a82-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="a8a82-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="a8a82-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="a8a82-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="a8a82-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-605">User ID</span><span class="sxs-lookup"><span data-stu-id="a8a82-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="a8a82-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="a8a82-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-607">User Name</span><span class="sxs-lookup"><span data-stu-id="a8a82-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="a8a82-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="a8a82-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="a8a82-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="a8a82-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="a8a82-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="a8a82-611">Propiedades dinámicas del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="a8a82-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="a8a82-612">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a8a82-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8a82-613">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a8a82-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a8a82-614">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a8a82-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="a8a82-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a8a82-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a8a82-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a8a82-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a8a82-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="a8a82-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a8a82-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a8a82-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a8a82-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a8a82-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a8a82-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="a8a82-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a8a82-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a8a82-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a8a82-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="a8a82-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a8a82-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="a8a82-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a8a82-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a8a82-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a8a82-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a8a82-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a8a82-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a8a82-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a8a82-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a8a82-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a8a82-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a8a82-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a8a82-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a8a82-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a8a82-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a8a82-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a8a82-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a8a82-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a8a82-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a8a82-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a8a82-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a8a82-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a8a82-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a8a82-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a8a82-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a8a82-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a8a82-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a8a82-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a8a82-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a8a82-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a8a82-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a8a82-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a8a82-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a8a82-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a8a82-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a8a82-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="a8a82-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="a8a82-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="a8a82-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a8a82-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a8a82-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="a8a82-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a8a82-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a8a82-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a8a82-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a8a82-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a8a82-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a8a82-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a8a82-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a8a82-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="a8a82-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a8a82-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a8a82-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="a8a82-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a8a82-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a8a82-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="a8a82-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a8a82-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a8a82-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="a8a82-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a8a82-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a8a82-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="a8a82-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a8a82-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="a8a82-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a8a82-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a8a82-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a8a82-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="a8a82-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a8a82-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a8a82-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a8a82-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="a8a82-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a8a82-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a8a82-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a8a82-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a8a82-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a8a82-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a8a82-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="a8a82-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a8a82-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a8a82-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a8a82-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a8a82-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="a8a82-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="a8a82-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="a8a82-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a8a82-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a8a82-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a8a82-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a8a82-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="a8a82-734">Propiedades dinámicas de Command</span><span class="sxs-lookup"><span data-stu-id="a8a82-734">Command Dynamic Properties</span></span>

<span data-ttu-id="a8a82-735">Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="a8a82-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8a82-736">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a8a82-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a8a82-737">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a8a82-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="a8a82-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a8a82-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a8a82-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a8a82-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a8a82-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="a8a82-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a8a82-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a8a82-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a8a82-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a8a82-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a8a82-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="a8a82-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a8a82-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a8a82-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a8a82-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="a8a82-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a8a82-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="a8a82-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a8a82-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a8a82-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a8a82-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a8a82-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a8a82-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a8a82-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a8a82-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a8a82-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a8a82-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a8a82-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a8a82-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a8a82-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a8a82-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a8a82-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a8a82-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a8a82-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a8a82-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a8a82-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a8a82-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a8a82-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a8a82-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a8a82-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a8a82-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a8a82-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a8a82-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a8a82-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a8a82-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a8a82-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a8a82-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a8a82-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a8a82-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a8a82-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a8a82-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a8a82-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a8a82-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a8a82-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="a8a82-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a8a82-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="a8a82-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="a8a82-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a8a82-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a8a82-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="a8a82-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a8a82-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a8a82-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a8a82-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a8a82-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a8a82-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a8a82-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a8a82-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a8a82-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="a8a82-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a8a82-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a8a82-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="a8a82-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a8a82-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a8a82-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="a8a82-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a8a82-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a8a82-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="a8a82-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a8a82-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="a8a82-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a8a82-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a8a82-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="a8a82-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a8a82-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a8a82-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="a8a82-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a8a82-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a8a82-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a8a82-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a8a82-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="a8a82-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a8a82-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a8a82-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a8a82-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="a8a82-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a8a82-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a8a82-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a8a82-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a8a82-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a8a82-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a82-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="a8a82-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a8a82-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a8a82-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="a8a82-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a8a82-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a8a82-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a8a82-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a8a82-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="a8a82-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="a8a82-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a8a82-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8a82-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="a8a82-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a8a82-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a8a82-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8a82-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a8a82-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a8a82-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a8a82-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a8a82-855">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8a82-855">See also</span></span>

<span data-ttu-id="a8a82-856">Para obtener información detallada acerca de implementación específico e información funcional acerca el proveedor Microsoft OLE DB para ODBC, consulte la [Guía del programador de OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) o visite el [Centro de desarrolladores de plataforma de datos](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="a8a82-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

