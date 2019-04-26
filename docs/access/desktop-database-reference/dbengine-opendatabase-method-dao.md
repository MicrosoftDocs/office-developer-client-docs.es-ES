---
title: Método DBEngine.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1cd4188931999284a6454064a0906b64cf1f519a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294256"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="69ac3-102">Método DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="69ac3-102">DBEngine.OpenDatabase Method (DAO)</span></span>

<span data-ttu-id="69ac3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69ac3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69ac3-104">Abre una base de datos determinada y devuelve una referencia al objeto **[Database](database-object-dao.md)** que lo representa.</span><span class="sxs-lookup"><span data-stu-id="69ac3-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ac3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69ac3-105">Syntax</span></span>

<span data-ttu-id="69ac3-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="69ac3-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="69ac3-107">*expression* Variable que representa un objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="69ac3-107">*expression*  A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="69ac3-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="69ac3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69ac3-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="69ac3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="69ac3-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="69ac3-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="69ac3-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="69ac3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="69ac3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="69ac3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69ac3-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="69ac3-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="69ac3-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="69ac3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="69ac3-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="69ac3-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="69ac3-p101">El nombre de un archivo de base de datos de Microsoft Access existente, o el nombre de origen de datos (DSN) de un origen de datos ODBC. Para más información sobre la configuración de este valor, consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="69ac3-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69ac3-118"><em>Opciones</em></span><span class="sxs-lookup"><span data-stu-id="69ac3-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="69ac3-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="69ac3-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="69ac3-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="69ac3-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="69ac3-121">Establece varias opciones para la base de datos, tal como se especifica en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="69ac3-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69ac3-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="69ac3-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="69ac3-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="69ac3-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="69ac3-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="69ac3-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="69ac3-125"><strong>True</strong> si quiere abrir la base de datos con un acceso de solo lectura o <strong>False</strong> (opción predeterminada) si quiere abrir la base de datos con un acceso de escritura/lectura.</span><span class="sxs-lookup"><span data-stu-id="69ac3-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69ac3-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="69ac3-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="69ac3-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="69ac3-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="69ac3-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="69ac3-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="69ac3-129">Especifica diversa información de conexión, incluidas las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="69ac3-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="69ac3-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69ac3-130">Return value</span></span>

<span data-ttu-id="69ac3-131">Base de datos</span><span class="sxs-lookup"><span data-stu-id="69ac3-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="69ac3-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69ac3-132">Remarks</span></span>

<span data-ttu-id="69ac3-133">Puede utilizar los valores siguientes para el argumento opciones.</span><span class="sxs-lookup"><span data-stu-id="69ac3-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69ac3-134">Valor</span><span class="sxs-lookup"><span data-stu-id="69ac3-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="69ac3-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="69ac3-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69ac3-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="69ac3-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="69ac3-137">Abre la base de datos en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="69ac3-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69ac3-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="69ac3-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="69ac3-139">(Opción predeterminada) Abre la base de datos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="69ac3-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69ac3-140">Al abrir una base de datos, se agrega automáticamente a la colección **Databases**.</span><span class="sxs-lookup"><span data-stu-id="69ac3-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="69ac3-141">Al usar dbname, debe tener en cuenta ciertos aspectos:</span><span class="sxs-lookup"><span data-stu-id="69ac3-141">Some considerations apply when you use  dbname:</span></span>

- <span data-ttu-id="69ac3-142">Si hace referencia a una base de datos que ya está abierta para que acceda otro usuario, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="69ac3-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="69ac3-143">Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="69ac3-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="69ac3-144">Si es una cadena de longitud cero ("") y *connect* es "ODBC;", se mostrará un cuadro de diálogo con una lista de todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="69ac3-144">If it's a zero-length string ("") and connect is "ODBC;"

, a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="69ac3-145">Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.</span><span class="sxs-lookup"><span data-stu-id="69ac3-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="69ac3-146">Cuando acceda a un origen de datos ODBC conectado a un motor de base de datos de Microsoft Access, podrá mejorar el rendimiento de la aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular los objetos [TableDef](tabledef-object-dao.md) uno por uno a tablas concretas del origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="69ac3-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


