---
title: Miembros del área de trabajo (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a2105c13f5f7ce9a75e7e18e20477d8b283543a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302600"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="ae9d7-102">Miembros del área de trabajo (DAO)</span><span class="sxs-lookup"><span data-stu-id="ae9d7-102">Workspace members (DAO)</span></span>


<span data-ttu-id="ae9d7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae9d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae9d7-p101">Un objeto Workspace define una sesión con nombre para un usuario. Contiene bases de datos abiertas y proporciona mecanismos para transacciones simultáneas y, en áreas de trabajo de Microsoft Access, compatibilidad con grupos de trabajo seguros.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-p101">A Workspace object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="ae9d7-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="ae9d7-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae9d7-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae9d7-107">Name</span></span></p></th>
<th><p><span data-ttu-id="ae9d7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae9d7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-109"><strong><a href="workspace-begintrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-110">Inicia una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-110">Begins a new transaction.</span></span> <span data-ttu-id="ae9d7-111"><strong>Database</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-111">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d7-112"><strong><a href="workspace-close-method-dao.md">Cerrar</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-113">Cierra un objeto <strong>Workspace</strong> abierto.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-115">Termina la transacción actual y guarda los cambios.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d7-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-117">Crea un nuevo objeto <strong><a href="database-object-dao.md">Database</a></strong>, guarda la base de datos en el disco y devuelve un objeto <strong>Database</strong> abierto (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ae9d7-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-119"><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-119"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="ae9d7-120">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="ae9d7-121">Abre un objeto <strong><a href="connection-object-dao.md">Connection</a></strong> en un origen de datos ODBC (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="ae9d7-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d7-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-123">Abre una base de datos determinada en un objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> y devuelve una referencia al objeto <strong><a href="database-object-dao.md">Database</a></strong> que lo representa.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-125">Termina la transacción actual y restablece las bases de datos del objeto <strong>Workspace</strong> al estado que tenían antes de que comenzara la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="ae9d7-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae9d7-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae9d7-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae9d7-127">Name</span></span></p></th>
<th><p><span data-ttu-id="ae9d7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae9d7-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-130">Devuelve una colección <strong>Connections</strong> que representa las conexiones actuales del objeto <strong>Workspace</strong> especificado.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-130">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="ae9d7-131">Es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-131">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d7-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-133">Devuelve una colección <strong>Databases</strong> que representa las bases de datos abiertas del objeto <strong>Workspace</strong> especificado.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-133">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="ae9d7-134">Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae9d7-134">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-136"><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-136"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="ae9d7-137">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-137">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="ae9d7-138">Establece o devuelve el tipo de controlador de cursor utilizado en la conexión creada por los métodos <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> o <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="ae9d7-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d7-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">Isolateodbctrans (</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-140">Establece o devuelve un valor que indica si varias transacciones que implican los mismos motores de base de datos de Microsoft Access conectados al origen de datos ODBC están aisladas (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ae9d7-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-142">Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d7-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-p107">Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d7-147"><strong><a href="workspace-properties-property-dao.md">Propiedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-148">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-148">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="ae9d7-149">Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-149">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d7-150"><strong><a href="workspace-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="ae9d7-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ae9d7-151">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-151">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="ae9d7-152"><strong>Integer</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ae9d7-152">Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

