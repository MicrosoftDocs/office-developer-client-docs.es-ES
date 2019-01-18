---
title: CopiarArchivoDeBaseDeDatos (acción de macro)
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3c98d8795bb7039c0ae158414401dc5d754066f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699446"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="11724-102">CopiarArchivoDeBaseDeDatos (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="11724-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="11724-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11724-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11724-104">La acción **CopiarArchivoDeBaseDeDatos** se puede usar para realizar una copia de la base de datos de Microsoft SQL Server 7.0 o posterior que está conectada al proyecto de Access.</span><span class="sxs-lookup"><span data-stu-id="11724-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="11724-105">Access desasocia la base de datos actual y, a continuación, adjunta al servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="11724-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="11724-106">Para obtener más información acerca de cómo se desasocia y asocia una base de datos, vea la documentación de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="11724-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="11724-107">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="11724-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="11724-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="11724-108">Setting</span></span>

<span data-ttu-id="11724-109">La acción **CopiarArchivoDeBaseDeDatos** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="11724-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11724-110">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="11724-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="11724-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="11724-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11724-112"><strong>Nombre de archivo de la base de datos</strong></span><span class="sxs-lookup"><span data-stu-id="11724-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="11724-p102">El nombre del nuevo Archivo de datos maestro. La ruta predeterminada para el archivo es la ubicación actual del archivo de proyecto de Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="11724-p102">The name of the new Master Data File. The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11724-115"><strong>Sobrescribir archivo existente</strong></span><span class="sxs-lookup"><span data-stu-id="11724-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="11724-p103">Especifica si hay que reemplazar o no un archivo existente con el mismo nombre. Si se establece en <strong>Sí</strong> y el nombre del archivo ya existe, se sobrescribe el archivo. Si se establece en <strong>No</strong> y el nombre del archivo ya existe, no se sobrescribe el archivo y falla la acción. Si el archivo no existe aún, se ignora esta configuración. El valor predeterminado es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="11724-p103">Specifies whether or not to replace an existing file with the same name. If set to <strong>Yes</strong> and the filename already exists, the file is overwritten. If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails. If the file does not already exist, this setting is ignored. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11724-121"><strong>Desconectar todos los usuarios</strong></span><span class="sxs-lookup"><span data-stu-id="11724-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="11724-p104">Especifica si Access debe obligar a los usuarios a salir de la base de datos. Si se establece en <strong>Sí</strong>, todos los usuarios que estén conectados a la base de datos se desconectan para que pueda realizarse la operación de copia de la base de datos. Si se establece en <strong>No</strong> y hay uno o más usuarios conectados a la base de datos, se produce un error en la operación de copia de la base de datos. El valor predeterminado es <strong>No</strong>. 

</span><span class="sxs-lookup"><span data-stu-id="11724-p104">Specifies whether or not Access should force users off the database. If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed. If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails. The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="11724-126"><strong>Advertencia</strong>: desconectar usuarios de una base de datos sin una advertencia adecuada puede provocar una pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="11724-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="11724-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11724-127">Remarks</span></span>

<span data-ttu-id="11724-128">La operación de copia se realiza de manera sincrónica, por lo que no se pueden realizar otras operaciones hasta que la copia de la base de datos haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="11724-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="11724-129">La acción **CopiarArchivoDeBaseDeDatos** no solo copia datos, definiciones de datos y objetos de base de datos, sino también copia propiedades extendidas, como valores predeterminados, restricciones de texto y valores de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="11724-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="11724-130">Requisitos para copiar una base de datos:</span><span class="sxs-lookup"><span data-stu-id="11724-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="11724-131">Debe desconectar todas las aplicaciones y los usuarios antes de copiar el archivo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="11724-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="11724-132">Todos los objetos y las vistas excepto el Panel de navegación deben cerrarse.</span><span class="sxs-lookup"><span data-stu-id="11724-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="11724-133">La base de datos actual no se debe replicar.</span><span class="sxs-lookup"><span data-stu-id="11724-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="11724-134">La base de datos del servidor de origen debe ser Microsoft SQL Server versión 7.0 o superior, o SQL Server 2000 Desktop Engine en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="11724-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="11724-135">La base de datos de SQL Server del servidor de origen debe ser una base de datos de un solo archivo.</span><span class="sxs-lookup"><span data-stu-id="11724-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="11724-136">Debe ser miembro del rol sysadmin tanto en el equipo SQL Server de origen como en el de destino.</span><span class="sxs-lookup"><span data-stu-id="11724-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="11724-137">Para ejecutar la acción **CopiarArchivoDeBaseDeDatos** en un módulo de Visual Basic para Aplicaciones, utilice el método **CopyDatabaseFile** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="11724-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

