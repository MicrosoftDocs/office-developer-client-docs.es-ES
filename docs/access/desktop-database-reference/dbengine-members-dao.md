---
title: Miembros de DBEngine (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294284"
---
# <a name="dbengine-members-dao"></a><span data-ttu-id="e939b-102">Miembros de DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="e939b-102">DBEngine members (DAO)</span></span>


<span data-ttu-id="e939b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e939b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e939b-104">El objeto DBEngine es el objeto de nivel superior en el modelo de objetos DAO.</span><span class="sxs-lookup"><span data-stu-id="e939b-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="e939b-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="e939b-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e939b-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="e939b-106">Name</span></span></p></th>
<th><p><span data-ttu-id="e939b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e939b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e939b-108"><strong><a href="dbengine-begintrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-109">Inicia una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="e939b-109">Begins a new transaction.</span></span> <span data-ttu-id="e939b-110"><strong>Database</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e939b-110">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-112">Termina la transacción actual y guarda los cambios.</span><span class="sxs-lookup"><span data-stu-id="e939b-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-114">Copia y compacta una base de datos cerrada, y ofrece la opción de cambiar su versión, el orden de intercalación y el cifrado.</span><span class="sxs-lookup"><span data-stu-id="e939b-114">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="e939b-115">(Sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e939b-115">(Microsoft Access workspaces only).</span></span> <span data-ttu-id="e939b-116">.</span><span class="sxs-lookup"><span data-stu-id="e939b-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-118">Crea un nuevo objeto <strong><a href="database-object-dao.md">Database</a></strong>, guarda la base de datos en el disco y devuelve un objeto <strong>Database</strong> abierto (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e939b-118">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="e939b-119">.</span><span class="sxs-lookup"><span data-stu-id="e939b-119"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-121">Crea un nuevo objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="e939b-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-122"><strong><a href="dbengine-idle-method-dao.md">Usado</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-123">Suspende el procesamiento de datos y habilita el motor de base de datos de Microsoft Access para que realice las tareas pendientes, como la optimización de memoria o los tiempos de espera de paginación (sólo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e939b-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-125">Uno de los valores de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="e939b-125">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="e939b-126"><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e939b-126"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="e939b-127">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e939b-127">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="e939b-128">Abre un objeto <strong><a href="connection-object-dao.md">Connection</a></strong> en un origen de datos ODBC (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="e939b-128">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-130">Abre una base de datos especificada y devuelve una referencia al objeto <strong><a href="database-object-dao.md">Database</a></strong> que la representa.</span><span class="sxs-lookup"><span data-stu-id="e939b-130">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-p105">Proporciona información de conexión para un origen de datos ODBC en el Registro de Windows. El controlador ODBC necesita información de conexión cuando se abre el origen de datos ODBC durante una sesión.</span><span class="sxs-lookup"><span data-stu-id="e939b-p105">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-135">Termina la transacción actual y restablece las bases de datos del objeto <strong>Workspace</strong> al estado que tenían antes de que comenzara la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="e939b-135">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-137">Anula temporalmente los valores para las claves del motor de base de datos de Microsoft Access en el Registro de Windows (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e939b-137">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="e939b-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e939b-138">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e939b-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="e939b-139">Name</span></span></p></th>
<th><p><span data-ttu-id="e939b-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="e939b-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e939b-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-142">Establece la contraseña utilizada para crear el objeto <strong>Workspace</strong> predeterminado cuando se inicializa.</span><span class="sxs-lookup"><span data-stu-id="e939b-142">Sets the password used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="e939b-143"><strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e939b-143">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-145">Establece o devuelve un valor que indica qué tipo de área de trabajo se utilizará en el siguiente objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> que se cree.</span><span class="sxs-lookup"><span data-stu-id="e939b-145">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-147">Establece el nombre de usuario utilizado para crear el objeto <strong>Workspace</strong> predeterminado cuando se inicializa.</span><span class="sxs-lookup"><span data-stu-id="e939b-147">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="e939b-148"><strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e939b-148">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-149"><strong><a href="dbengine-errors-property-dao.md">Errores</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-149"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-150">Devuelve una colección <strong>Errors</strong> que contiene todos los objetos <strong>Error</strong> almacenados para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="e939b-150">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object.</span></span> <span data-ttu-id="e939b-151">Es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e939b-151">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-153">Establece o devuelve información sobre la clave del Registro de Windows que contiene los valores para el motor de base de datos Microsoft Access (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e939b-153">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-155">Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="e939b-155">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-156"><strong><a href="dbengine-properties-property-dao.md">Propiedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-156"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-157">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="e939b-157">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="e939b-158">Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e939b-158">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e939b-159"><strong><a href="dbengine-version-property-dao.md">Versión</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-159"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-160">Devuelve la versión de DAO que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="e939b-160">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="e939b-161"><strong>String</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e939b-161">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e939b-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span><span class="sxs-lookup"><span data-stu-id="e939b-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e939b-163">Devuelve una colección <strong>Workspaces</strong> que contiene todos los objetos <strong>Workspace</strong> activos que no están ocultos.</span><span class="sxs-lookup"><span data-stu-id="e939b-163">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects.</span></span> <span data-ttu-id="e939b-164">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e939b-164">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

