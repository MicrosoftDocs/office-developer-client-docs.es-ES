---
title: Proveedor de Microsoft OLE DB para Servicio de Active Directory de Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ad3b3163a2169d90072335d5bc827700b99c73f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484221"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="7d9c3-102">Proveedor de Microsoft OLE DB para Servicio de Active Directory de Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d9c3-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="7d9c3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d9c3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7d9c3-p101">El proveedor de interfaces del servicio de Active Directory (ADSI) de Microsoft permite a ADO conectarse a servicios de directorio heterogéneos mediante ADSI. Esto ofrece a las aplicaciones ADO acceso de solo lectura a los servicios de directorio de Microsoft Windows NT 4.0 y Microsoft Windows 2000, además de a cualquier servicio de directorio compatible con LDAP y a Novell Directory Services. ADSI se basa en un modelo de proveedor, de modo que si hay un nuevo proveedor que ofrece acceso a otro directorio, la aplicación ADO podrá obtener acceso a él sin problemas. El proveedor de ADSI es de subprocesamiento libre y está habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-p101">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI. This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services. ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly. The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="7d9c3-108">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="7d9c3-108">Connection String Parameters</span></span>

<span data-ttu-id="7d9c3-109">Para conectar con este proveedor, establezca el argumento **Provider** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="7d9c3-110">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="7d9c3-111">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="7d9c3-111">Typical Connection String</span></span>

<span data-ttu-id="7d9c3-112">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="7d9c3-113">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d9c3-114">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="7d9c3-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="7d9c3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d9c3-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-116"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="7d9c3-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-117">Especifica el Proveedor OLE DB para Servicio de Active Directory de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-118"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="7d9c3-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-p102">Especifica el nombre de usuario. Si se omite la palabra clave, se utiliza el inicio de sesión actual.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-p102">Specifies the user name. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="7d9c3-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-p103">Especifica la contraseña de usuario. Si se omite la palabra clave, se utiliza el inicio de sesión actual.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-p103">Specifies the user password. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d9c3-124">**Texto del comando**</span><span class="sxs-lookup"><span data-stu-id="7d9c3-124">**Command Text**</span></span>

<span data-ttu-id="7d9c3-125">El proveedor reconoce una cadena de texto de comando de cuatro partes en la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d9c3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7d9c3-126">Value</span></span></p></th>
<th><p><span data-ttu-id="7d9c3-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d9c3-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="7d9c3-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-129">Indica el objeto <strong>ADsPath</strong> desde el que se inicia la búsqueda (es decir, la raíz de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="7d9c3-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-130"><em>Filter</em></span><span class="sxs-lookup"><span data-stu-id="7d9c3-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-131">Indica el filtro de búsqueda en el formato RFC 1960.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-132"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="7d9c3-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-133">Indica una lista de los atributos que se van a devolver delimitada por comas.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-134"><em>Scope</em></span><span class="sxs-lookup"><span data-stu-id="7d9c3-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-135">Optional.</span></span> <span data-ttu-id="7d9c3-136">Una <strong>cadena</strong> que especifica el ámbito de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="7d9c3-137">Puede ser una de las siguientes opciones: Base: sólo busca el objeto base (raíz de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="7d9c3-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="7d9c3-138">OneLevel: Busca en un solo nivel.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="7d9c3-139">Subárbol: Buscar en todo el subárbol.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d9c3-140">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="7d9c3-p105">El proveedor también admite una instrucción SELECT de SQL como texto del comando. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-p105">The provider also supports SQL SELECT for command text. For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="7d9c3-p106">El proveedor no acepta llamadas a procedimientos almacenados o nombres de tabla simples (por ejemplo, la propiedad [CommandType](commandtype-property-ado.md) siempre será **adCmdText**). Vea la documentación de las Interfaces del servicio de Active Directory para obtener una descripción más completa de los elementos de texto de un comando.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-p106">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**). See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="7d9c3-145">Comportamiento del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="7d9c3-145">Recordset Behavior</span></span>

<span data-ttu-id="7d9c3-146">En las tablas siguientes se enumeran las características disponibles en un objeto [Recordset](recordset-object-ado.md) abierto con este proveedor.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="7d9c3-147">El tipo de cursor estático (**adOpenStatic**) está disponible.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="7d9c3-148">Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección [Properties](properties-collection-ado.md) del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.</span><span class="sxs-lookup"><span data-stu-id="7d9c3-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="7d9c3-149">Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d9c3-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d9c3-150">Property</span></span></p></th>
<th><p><span data-ttu-id="7d9c3-151">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="7d9c3-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-153">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-155">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-157">solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-159">solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-161">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-163">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-165">siempre <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="7d9c3-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-167">siempre <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="7d9c3-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-169">siempre <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="7d9c3-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-171">solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-172"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-173">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-174"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-175">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-177">No disponible</span><span class="sxs-lookup"><span data-stu-id="7d9c3-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-179">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-181">solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-183">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-185">solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-187">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-188"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-189">solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-190"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-191">solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d9c3-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d9c3-192">Disponibilidad de métodos estándar **Recordset** ADO:</span><span class="sxs-lookup"><span data-stu-id="7d9c3-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d9c3-193">Método</span><span class="sxs-lookup"><span data-stu-id="7d9c3-193">Method</span></span></p></th>
<th><p><span data-ttu-id="7d9c3-194">¿Disponible?</span><span class="sxs-lookup"><span data-stu-id="7d9c3-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-196">No</span><span class="sxs-lookup"><span data-stu-id="7d9c3-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-197"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-198">No</span><span class="sxs-lookup"><span data-stu-id="7d9c3-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-200">No</span><span class="sxs-lookup"><span data-stu-id="7d9c3-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-202">No</span><span class="sxs-lookup"><span data-stu-id="7d9c3-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-204">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-206">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-207"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-208">No</span><span class="sxs-lookup"><span data-stu-id="7d9c3-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-210">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-211"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-212">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-214">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-216">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-218">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-220">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-222">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-224">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-225"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-226">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-227"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-228">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-229"><a href="supports-method-ado.md">Admite</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-230">Sí</span><span class="sxs-lookup"><span data-stu-id="7d9c3-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d9c3-231"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-232">No</span><span class="sxs-lookup"><span data-stu-id="7d9c3-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d9c3-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="7d9c3-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="7d9c3-234">No</span><span class="sxs-lookup"><span data-stu-id="7d9c3-234">No</span></span></p></td>
</tr>
</tbody>
</table>
