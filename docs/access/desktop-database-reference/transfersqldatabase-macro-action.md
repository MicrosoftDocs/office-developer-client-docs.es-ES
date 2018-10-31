---
title: TransferirBaseDeDatosSQL (acción de macro)
TOCTitle: TransferSQLDatabase Macro Action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8066c7e8ae827d7ae5a521682f2100bc11c9a6f8
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862894"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="7c9b6-102">TransferirBaseDeDatosSQL (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="7c9b6-102">TransferSQLDatabase Macro Action</span></span>


<span data-ttu-id="7c9b6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c9b6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7c9b6-104">En un proyecto de Access, se puede utilizar la acción **TransferirBaseDeDatosSQL** para transferir una base de datos de Microsoft SQL Server 7.0 o posterior a otra base de datos de SQL Server 7.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="7c9b6-105">Para obtener más información sobre la transferencia de una base de datos, vea la documentación de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-105">For more information about transferring a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <span data-ttu-id="7c9b6-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



## <a name="setting"></a><span data-ttu-id="7c9b6-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="7c9b6-108">Setting</span></span>

<span data-ttu-id="7c9b6-109">La acción **TransferirBaseDeDatosSQL** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-109">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c9b6-110">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="7c9b6-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7c9b6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c9b6-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c9b6-112"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7c9b6-112"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c9b6-113">El nombre de la base de datos de SQL Server 7.0 o posterior donde se están copiando los datos.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-113">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c9b6-114"><strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="7c9b6-114"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="7c9b6-115">El nombre de la nueva base de datos que se creará en el servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-115">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c9b6-116"><strong>Usar conexión de confianza</strong></span><span class="sxs-lookup"><span data-stu-id="7c9b6-116"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="7c9b6-117">Especifica si existe o no es una conexión de confianza para el servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-117">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="7c9b6-118">Si establece en <strong>Yes</strong>, a continuación, hay una conexión de confianza y no se necesitan los argumentos <strong>Inicio de sesión</strong> y la <strong>contraseña</strong> .</span><span class="sxs-lookup"><span data-stu-id="7c9b6-118">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="7c9b6-119">Si se establece en <strong>No</strong>, el <strong>Inicio de sesión</strong> y la <strong>contraseña</strong> argumentos es necesario.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-119">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="7c9b6-120">El valor predeterminado es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-120">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="7c9b6-121">Cuando se usa una conexión de confianza, la seguridad de SQL Server se integra con la seguridad del sistema operativo Windows para proporcionar un único inicio de sesión de la red y la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-121">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c9b6-122"><strong>Conexión</strong></span><span class="sxs-lookup"><span data-stu-id="7c9b6-122"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="7c9b6-123">El nombre de inicio de sesión en el servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-123">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c9b6-124"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="7c9b6-124"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="7c9b6-p104">La contraseña para el argumento <strong>Inicio de sesión</strong>. Esta contraseña se almacena como texto en el proyecto de Access, pero se oculta durante la operación de transferencia de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-p104">The password for the <strong>Login</strong> argument. This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c9b6-127"><strong>Transferir datos de copia</strong></span><span class="sxs-lookup"><span data-stu-id="7c9b6-127"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="7c9b6-p105">Especifica si se deben incluir datos en la operación de transferencia de la base de datos. El valor <strong>Sí</strong> indica que se incluyen todos los datos en todas las tablas, junto con todas las estructuras de datos, propiedades extendidas y objetos de base de datos. La opción <strong>No</strong> indica que no se incluyen los datos en las tablas. En el servidor de destino sólo se crean la estructura de la tabla y las propiedades extendidas, junto con todos los objetos de base de datos (excepto diagramas de base de datos). La opción predeterminada es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-p105">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7c9b6-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c9b6-133">Remarks</span></span>

<span data-ttu-id="7c9b6-134">No es posible realizar otras operaciones mientras se transfiere la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-134">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="7c9b6-135">La acción **TransferirBaseDeDatosSQL** copia de forma predeterminada datos, definiciones de datos, objetos de base de datos y propiedades extendidas (tales como valores predeterminados, restricciones de texto y valores de búsqueda).</span><span class="sxs-lookup"><span data-stu-id="7c9b6-135">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="7c9b6-136">Existen ciertos requisitos para transferir una base de datos:</span><span class="sxs-lookup"><span data-stu-id="7c9b6-136">There are requirements for transferring a database:</span></span>

  - <span data-ttu-id="7c9b6-137">El usuario debe ser un administrador del sistema en el servidor de destino (esto no es necesario en el servidor de origen).</span><span class="sxs-lookup"><span data-stu-id="7c9b6-137">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

<!-- end list -->

  - <span data-ttu-id="7c9b6-138">El servidor SQL Server conectado actualmente al proyecto de Access y el servidor de destino al que se está transfiriendo la base de datos debe ser SQL Server versión 7.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-138">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7c9b6-139">[!NOTA] Los servidores vinculados no se transfieren durante una operación de transferencia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-139">Linked servers are not transferred during a database transfer operation.</span></span></P>



<span data-ttu-id="7c9b6-140">Para ejecutar la acción **TransferirBaseDeDatosSQL** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferSQLDatabase** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="7c9b6-140">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

