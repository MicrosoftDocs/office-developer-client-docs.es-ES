---
title: Proveedor de Microsoft OLE DB para Servicio de Active Directory de Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23e1cab32fee6103a046219a7cda8c90f02d9f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288942"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="5364f-102">Proveedor de Microsoft OLE DB para el servicio Microsoft Active Directory</span><span class="sxs-lookup"><span data-stu-id="5364f-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="5364f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5364f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5364f-p101">El proveedor de interfaces del servicio de Active Directory (ADSI) de Microsoft permite a ADO conectarse a servicios de directorio heterogéneos mediante ADSI. Esto ofrece a las aplicaciones ADO acceso de solo lectura a los servicios de directorio de Microsoft Windows NT 4.0 y Microsoft Windows 2000, además de a cualquier servicio de directorio compatible con LDAP y a Novell Directory Services. ADSI se basa en un modelo de proveedor, de modo que si hay un nuevo proveedor que ofrece acceso a otro directorio, la aplicación ADO podrá obtener acceso a él sin problemas. El proveedor de ADSI es de subprocesamiento libre y está habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="5364f-p101">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI. This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services. ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly. The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="5364f-108">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="5364f-108">Connection String Parameters</span></span>

<span data-ttu-id="5364f-109">Para conectar con este proveedor, establezca el argumento **Provider** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="5364f-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="5364f-110">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="5364f-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="5364f-111">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="5364f-111">Typical Connection String</span></span>

<span data-ttu-id="5364f-112">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="5364f-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="5364f-113">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="5364f-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5364f-114">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="5364f-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="5364f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5364f-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5364f-116"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="5364f-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="5364f-117">Especifica el Proveedor OLE DB para Servicio de Active Directory de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5364f-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-118"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="5364f-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="5364f-p102">Especifica el nombre de usuario. Si se omite la palabra clave, se utiliza el inicio de sesión actual.</span><span class="sxs-lookup"><span data-stu-id="5364f-p102">Specifies the user name. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="5364f-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="5364f-p103">Especifica la contraseña de usuario. Si se omite la palabra clave, se utiliza el inicio de sesión actual.</span><span class="sxs-lookup"><span data-stu-id="5364f-p103">Specifies the user password. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5364f-124">**Texto del comando**</span><span class="sxs-lookup"><span data-stu-id="5364f-124">**Command Text**</span></span>

<span data-ttu-id="5364f-125">El proveedor reconoce una cadena de texto de comando de cuatro partes en la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="5364f-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5364f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5364f-126">Value</span></span></p></th>
<th><p><span data-ttu-id="5364f-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5364f-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5364f-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="5364f-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="5364f-129">Indica el objeto <strong>ADsPath</strong> desde el que se inicia la búsqueda (es decir, la raíz de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="5364f-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-130"><em>Filter</em></span><span class="sxs-lookup"><span data-stu-id="5364f-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="5364f-131">Indica el filtro de búsqueda en el formato RFC 1960.</span><span class="sxs-lookup"><span data-stu-id="5364f-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-132"><em>Atributos</em></span><span class="sxs-lookup"><span data-stu-id="5364f-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="5364f-133">Indica una lista de los atributos que se van a devolver delimitada por comas.</span><span class="sxs-lookup"><span data-stu-id="5364f-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-134"><em>Scope</em></span><span class="sxs-lookup"><span data-stu-id="5364f-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="5364f-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5364f-135">Optional.</span></span> <span data-ttu-id="5364f-136">Un valor de tipo <strong>String</strong> que especifica el ámbito de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5364f-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="5364f-137">Puede ser uno de los siguientes: Base: buscar solo el objeto base (raíz de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="5364f-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="5364f-138">OneLevel: busque solo un nivel.</span><span class="sxs-lookup"><span data-stu-id="5364f-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="5364f-139">Subárbol: busque todo el subárbol.</span><span class="sxs-lookup"><span data-stu-id="5364f-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5364f-140">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5364f-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="5364f-p105">El proveedor también admite una instrucción SELECT de SQL como texto del comando. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5364f-p105">The provider also supports SQL SELECT for command text. For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="5364f-p106">El proveedor no acepta llamadas a procedimientos almacenados o nombres de tabla simples (por ejemplo, la propiedad [CommandType](commandtype-property-ado.md) siempre será **adCmdText**). Vea la documentación de las Interfaces del servicio de Active Directory para obtener una descripción más completa de los elementos de texto de un comando.</span><span class="sxs-lookup"><span data-stu-id="5364f-p106">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**). See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="5364f-145">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="5364f-145">Recordset Behavior</span></span>

<span data-ttu-id="5364f-146">En las tablas siguientes se enumeran las características disponibles en un objeto [Recordset](recordset-object-ado.md) abierto con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="5364f-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="5364f-147">Solo está disponible el tipo de cursor Estático (**adOpenStatic**).</span><span class="sxs-lookup"><span data-stu-id="5364f-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="5364f-148">Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección [Properties](properties-collection-ado.md) del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.</span><span class="sxs-lookup"><span data-stu-id="5364f-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="5364f-149">Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="5364f-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5364f-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5364f-150">Property</span></span></p></th>
<th><p><span data-ttu-id="5364f-151">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="5364f-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5364f-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="5364f-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-153">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="5364f-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-155">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="5364f-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-157">solo lectura</span><span class="sxs-lookup"><span data-stu-id="5364f-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="5364f-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-159">solo lectura</span><span class="sxs-lookup"><span data-stu-id="5364f-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="5364f-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-161">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="5364f-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-163">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="5364f-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-165">siempre <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="5364f-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="5364f-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-167">siempre <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="5364f-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="5364f-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-169">siempre <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="5364f-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="5364f-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-171">solo lectura</span><span class="sxs-lookup"><span data-stu-id="5364f-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-172"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="5364f-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-173">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-174"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="5364f-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-175">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="5364f-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-177">no disponible</span><span class="sxs-lookup"><span data-stu-id="5364f-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="5364f-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-179">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="5364f-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-181">solo lectura</span><span class="sxs-lookup"><span data-stu-id="5364f-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="5364f-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-183">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="5364f-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-185">solo lectura</span><span class="sxs-lookup"><span data-stu-id="5364f-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="5364f-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-187">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5364f-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-188"><a href="state-property-ado.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="5364f-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-189">solo lectura</span><span class="sxs-lookup"><span data-stu-id="5364f-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-190"><a href="status-property-ado-recordset.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="5364f-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-191">solo lectura</span><span class="sxs-lookup"><span data-stu-id="5364f-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5364f-192">Disponibilidad de métodos estándar **Recordset** ADO:</span><span class="sxs-lookup"><span data-stu-id="5364f-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5364f-193">Método</span><span class="sxs-lookup"><span data-stu-id="5364f-193">Method</span></span></p></th>
<th><p><span data-ttu-id="5364f-194">¿Disponible?</span><span class="sxs-lookup"><span data-stu-id="5364f-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5364f-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="5364f-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-196">No</span><span class="sxs-lookup"><span data-stu-id="5364f-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-197"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="5364f-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-198">No</span><span class="sxs-lookup"><span data-stu-id="5364f-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="5364f-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-200">No</span><span class="sxs-lookup"><span data-stu-id="5364f-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="5364f-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-202">No</span><span class="sxs-lookup"><span data-stu-id="5364f-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="5364f-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-204">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="5364f-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-206">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-207"><a href="delete-method-ado-recordset.md">Eliminar</a></span><span class="sxs-lookup"><span data-stu-id="5364f-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-208">No</span><span class="sxs-lookup"><span data-stu-id="5364f-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="5364f-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-210">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-211"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="5364f-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-212">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="5364f-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-214">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="5364f-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-216">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="5364f-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-218">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="5364f-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-220">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="5364f-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-222">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5364f-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-224">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-225"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="5364f-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-226">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-227"><a href="resync-method-ado.md">Volver a sincronizar</a></span><span class="sxs-lookup"><span data-stu-id="5364f-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-228">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-229"><a href="supports-method-ado.md">Compatible</a></span><span class="sxs-lookup"><span data-stu-id="5364f-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-230">Sí</span><span class="sxs-lookup"><span data-stu-id="5364f-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5364f-231"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="5364f-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-232">No</span><span class="sxs-lookup"><span data-stu-id="5364f-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5364f-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="5364f-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="5364f-234">No</span><span class="sxs-lookup"><span data-stu-id="5364f-234">No</span></span></p></td>
</tr>
</tbody>
</table>

