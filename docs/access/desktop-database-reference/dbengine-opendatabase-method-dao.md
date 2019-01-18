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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708532"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="405e0-102">Método DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="405e0-102">DBEngine.OpenDatabase method (DAO)</span></span>

<span data-ttu-id="405e0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="405e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="405e0-104">Abre una base de datos especificada y devuelve una referencia al objeto **[Database](database-object-dao.md)** que la representa.</span><span class="sxs-lookup"><span data-stu-id="405e0-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="405e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="405e0-105">Syntax</span></span>

<span data-ttu-id="405e0-106">*expresión* . OpenDatabase (***nombre***, ***Opciones***, ***ReadOnly***, ***Conectar***)</span><span class="sxs-lookup"><span data-stu-id="405e0-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="405e0-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="405e0-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="405e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="405e0-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="405e0-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="405e0-109">Name</span></span></p></th>
<th><p><span data-ttu-id="405e0-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="405e0-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="405e0-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="405e0-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="405e0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="405e0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="405e0-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="405e0-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="405e0-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="405e0-114">Required</span></span></p></td>
<td><p><span data-ttu-id="405e0-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="405e0-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="405e0-p101">El nombre de un archivo de base de datos de Microsoft Access existente, o el nombre de origen de datos (DSN) de un origen de datos ODBC. Para más información sobre la configuración de este valor, consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="405e0-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="405e0-118"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="405e0-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="405e0-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="405e0-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="405e0-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="405e0-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="405e0-121">Establece varias opciones para la base de datos, tal como se especifica en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="405e0-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="405e0-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="405e0-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="405e0-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="405e0-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="405e0-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="405e0-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="405e0-125"><strong>True</strong> si quiere abrir la base de datos con un acceso de solo lectura o <strong>False</strong> (opción predeterminada) si quiere abrir la base de datos con un acceso de escritura/lectura.</span><span class="sxs-lookup"><span data-stu-id="405e0-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="405e0-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="405e0-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="405e0-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="405e0-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="405e0-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="405e0-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="405e0-129">Especifica diversa información de conexión, incluidas las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="405e0-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="405e0-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="405e0-130">Return value</span></span>

<span data-ttu-id="405e0-131">Base de datos</span><span class="sxs-lookup"><span data-stu-id="405e0-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="405e0-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="405e0-132">Remarks</span></span>

<span data-ttu-id="405e0-133">Puede utilizar los valores siguientes para el argumento options.</span><span class="sxs-lookup"><span data-stu-id="405e0-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="405e0-134">Valor</span><span class="sxs-lookup"><span data-stu-id="405e0-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="405e0-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="405e0-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="405e0-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="405e0-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="405e0-137">Abre la base de datos en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="405e0-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="405e0-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="405e0-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="405e0-139">(Opción predeterminada) Abre la base de datos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="405e0-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="405e0-140">Al abrir una base de datos, se agrega automáticamente a la colección **Databases**.</span><span class="sxs-lookup"><span data-stu-id="405e0-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="405e0-141">Se aplican determinadas consideraciones cuando se utiliza dbname:</span><span class="sxs-lookup"><span data-stu-id="405e0-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="405e0-142">Si se refiere a una base de datos que ya está abierta para que tenga acceso a ella otro usuario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="405e0-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="405e0-143">Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="405e0-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="405e0-144">Si es una cadena de longitud cero ("") y *Conectar* es "ODBC;", se muestra un cuadro de diálogo lista de todos los nombres de orígenes de datos ODBC para el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="405e0-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="405e0-145">Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.</span><span class="sxs-lookup"><span data-stu-id="405e0-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="405e0-146">[!NOTA] Cuando acceda a un origen de datos ODBC conectado a un motor de base de datos de Microsoft Access, podrá mejorar el rendimiento de la aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular los objetos [TableDef](tabledef-object-dao.md) uno por uno a tablas concretas del origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="405e0-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


