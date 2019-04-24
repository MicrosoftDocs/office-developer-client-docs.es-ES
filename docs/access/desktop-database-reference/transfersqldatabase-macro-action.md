---
title: TransferirBaseDeDatosSQL (acción de macro)
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5ed20555726d0a6f63f0e48fb154cedb411ef8cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306849"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="72584-102">TransferirBaseDeDatosSQL (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="72584-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="72584-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72584-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72584-104">En un proyecto de Access, se puede utilizar la acción **TransferirBaseDeDatosSQL** para transferir una base de datos de Microsoft SQL Server 7.0 o posterior a otra base de datos de SQL Server 7.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="72584-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="72584-105">Para obtener más información acerca de la transferencia de una base de datos, vea la documentación de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72584-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="72584-106">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="72584-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="72584-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="72584-107">Setting</span></span>

<span data-ttu-id="72584-108">La acción **TransferirBaseDeDatosSQL** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="72584-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72584-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="72584-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="72584-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="72584-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72584-111"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="72584-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="72584-112">El nombre de la base de datos de SQL Server 7.0 o posterior donde se están copiando los datos.</span><span class="sxs-lookup"><span data-stu-id="72584-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72584-113"><strong>Base de datos</strong></span><span class="sxs-lookup"><span data-stu-id="72584-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="72584-114">El nombre de la nueva base de datos que se creará en el servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="72584-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72584-115"><strong>Usar conexión de confianza</strong></span><span class="sxs-lookup"><span data-stu-id="72584-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="72584-116">Especifica si existe o no una conexión de confianza con SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72584-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="72584-117">Si presenta el valor <strong>Sí</strong>, entonces existe una conexión de confianza y no se necesitan los argumentos <strong>Inicio de sesión</strong> y <strong>Contraseña</strong>.</span><span class="sxs-lookup"><span data-stu-id="72584-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="72584-118">Si tiene el valor <strong>No</strong>, entonces es necesario especificar también los argumentos <strong>Inicio de sesión</strong> y <strong>Contraseña</strong>.</span><span class="sxs-lookup"><span data-stu-id="72584-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="72584-119">La opción predeterminada es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="72584-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="72584-120">Cuando se usa una conexión de confianza, la seguridad de SQL Server se integra con la seguridad del sistema operativo Windows para proporcionar un único inicio de sesión en la red y en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="72584-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72584-121"><strong>Sesión</strong></span><span class="sxs-lookup"><span data-stu-id="72584-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="72584-122">El nombre de inicio de sesión en el servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="72584-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72584-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="72584-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="72584-p103">La contraseña para el argumento <strong>Inicio de sesión</strong>. Esta contraseña se almacena como texto en el proyecto de Access, pero se oculta durante la operación de transferencia de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="72584-p103">The password for the <strong>Login</strong> argument. This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72584-126"><strong>Transferir datos de copia</strong></span><span class="sxs-lookup"><span data-stu-id="72584-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="72584-p104">Especifica si se deben incluir datos en la operación de transferencia de la base de datos. El valor <strong>Sí</strong> indica que se incluyen todos los datos en todas las tablas, junto con todas las estructuras de datos, propiedades extendidas y objetos de base de datos. La opción <strong>No</strong> indica que no se incluyen los datos en las tablas. En el servidor de destino sólo se crean la estructura de la tabla y las propiedades extendidas, junto con todos los objetos de base de datos (excepto diagramas de base de datos). La opción predeterminada es <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="72584-p104">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="72584-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72584-132">Remarks</span></span>

<span data-ttu-id="72584-133">No es posible realizar otras operaciones mientras se transfiere la base de datos.</span><span class="sxs-lookup"><span data-stu-id="72584-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="72584-134">La acción **TransferirBaseDeDatosSQL** copia de forma predeterminada datos, definiciones de datos, objetos de base de datos y propiedades extendidas (tales como valores predeterminados, restricciones de texto y valores de búsqueda).</span><span class="sxs-lookup"><span data-stu-id="72584-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="72584-135">Existen ciertos requisitos para transferir una base de datos:</span><span class="sxs-lookup"><span data-stu-id="72584-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="72584-136">El usuario debe ser un administrador del sistema en el servidor de destino (esto no es necesario en el servidor de origen).</span><span class="sxs-lookup"><span data-stu-id="72584-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="72584-137">El servidor SQL Server conectado actualmente al proyecto de Access y el servidor de destino al que se está transfiriendo la base de datos debe ser SQL Server versión 7.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="72584-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="72584-138">Los servidores vinculados no se transfieren durante una operación de transferencia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="72584-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="72584-139">Para ejecutar la acción **TransferirBaseDeDatosSQL** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferSQLDatabase** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="72584-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

