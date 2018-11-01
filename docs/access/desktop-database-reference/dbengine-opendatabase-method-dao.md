---
title: DBEngine.OpenDatabase Method (DAO)
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
ms.openlocfilehash: 45075a612b5d8dc6fabd4a91cc1efdacf37874a0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878944"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="27c04-102">DBEngine.OpenDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="27c04-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="27c04-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27c04-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27c04-104">Abre una base de datos especificada y devuelve una referencia al objeto **[Database](database-object-dao.md)** que la representa.</span><span class="sxs-lookup"><span data-stu-id="27c04-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c04-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27c04-105">Syntax</span></span>

<span data-ttu-id="27c04-106">*expresión* . OpenDatabase (***nombre***, ***Opciones***, ***ReadOnly***, ***Conectar***)</span><span class="sxs-lookup"><span data-stu-id="27c04-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="27c04-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="27c04-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="27c04-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27c04-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27c04-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="27c04-109">Name</span></span></p></th>
<th><p><span data-ttu-id="27c04-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="27c04-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="27c04-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="27c04-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="27c04-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c04-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27c04-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="27c04-113">Name</span></span></p></td>
<td><p><span data-ttu-id="27c04-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="27c04-114">Required</span></span></p></td>
<td><p><span data-ttu-id="27c04-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="27c04-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="27c04-p101">El nombre de un archivo de base de datos de Microsoft Access existente, o el nombre de origen de datos (DSN) de un origen de datos ODBC. Para más información sobre la configuración de este valor, consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="27c04-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c04-118">Options</span><span class="sxs-lookup"><span data-stu-id="27c04-118">Options</span></span></p></td>
<td><p><span data-ttu-id="27c04-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="27c04-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="27c04-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="27c04-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="27c04-121">Establece varias opciones para la base de datos, tal como se especifica en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="27c04-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c04-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="27c04-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="27c04-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="27c04-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="27c04-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="27c04-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="27c04-125"><strong>True</strong> si quiere abrir la base de datos con un acceso de solo lectura o <strong>False</strong> (opción predeterminada) si quiere abrir la base de datos con un acceso de escritura/lectura.</span><span class="sxs-lookup"><span data-stu-id="27c04-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c04-126">Conexión</span><span class="sxs-lookup"><span data-stu-id="27c04-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="27c04-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="27c04-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="27c04-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="27c04-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="27c04-129">Especifica diversa información de conexión, incluidas las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="27c04-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="27c04-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27c04-130">Return value</span></span>

<span data-ttu-id="27c04-131">Base de datos</span><span class="sxs-lookup"><span data-stu-id="27c04-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="27c04-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27c04-132">Remarks</span></span>

<span data-ttu-id="27c04-133">Puede utilizar los valores siguientes para el argumento options.</span><span class="sxs-lookup"><span data-stu-id="27c04-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27c04-134">Configuración</span><span class="sxs-lookup"><span data-stu-id="27c04-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="27c04-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c04-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27c04-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="27c04-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="27c04-137">Abre la base de datos en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="27c04-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c04-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="27c04-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="27c04-139">(Opción predeterminada) Abre la base de datos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="27c04-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="27c04-140">Al abrir una base de datos, se agrega automáticamente a la colección **Databases**.</span><span class="sxs-lookup"><span data-stu-id="27c04-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="27c04-141">Se aplican determinadas consideraciones cuando se utiliza dbname:</span><span class="sxs-lookup"><span data-stu-id="27c04-141">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="27c04-142">Si se refiere a una base de datos que ya está abierta para que tenga acceso a ella otro usuario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="27c04-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="27c04-143">Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="27c04-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="27c04-144">Si es una cadena de longitud cero ("") y *Conectar* es "ODBC;", se muestra un cuadro de diálogo lista de todos los nombres de orígenes de datos ODBC para el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="27c04-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="27c04-145">Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.</span><span class="sxs-lookup"><span data-stu-id="27c04-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <span data-ttu-id="27c04-146">[!NOTA] Cuando acceda a un origen de datos ODBC conectado a un motor de base de datos de Microsoft Access, podrá mejorar el rendimiento de la aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular los objetos [TableDef](tabledef-object-dao.md) uno por uno a tablas concretas del origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="27c04-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


