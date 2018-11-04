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
ms.openlocfilehash: eb3f6795ba2e64ebd6be1b04d6aa6aecccef781b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950093"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="b5259-102">Método DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="b5259-102">DBEngine.OpenDatabase method (DAO)</span></span>

<span data-ttu-id="b5259-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5259-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5259-104">Abre una base de datos especificada y devuelve una referencia al objeto **[Database](database-object-dao.md)** que la representa.</span><span class="sxs-lookup"><span data-stu-id="b5259-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5259-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5259-105">Syntax</span></span>

<span data-ttu-id="b5259-106">*expresión* . OpenDatabase (***nombre***, ***Opciones***, ***ReadOnly***, ***Conectar***)</span><span class="sxs-lookup"><span data-stu-id="b5259-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="b5259-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b5259-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5259-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5259-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5259-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="b5259-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b5259-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b5259-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b5259-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b5259-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5259-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5259-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b5259-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b5259-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b5259-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b5259-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="b5259-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b5259-p101">El nombre de un archivo de base de datos de Microsoft Access existente, o el nombre de origen de datos (DSN) de un origen de datos ODBC. Para más información sobre la configuración de este valor, consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="b5259-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5259-118"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="b5259-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="b5259-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="b5259-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b5259-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b5259-121">Establece varias opciones para la base de datos, tal como se especifica en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b5259-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5259-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="b5259-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="b5259-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="b5259-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b5259-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b5259-125"><strong>True</strong> si quiere abrir la base de datos con un acceso de solo lectura o <strong>False</strong> (opción predeterminada) si quiere abrir la base de datos con un acceso de escritura/lectura.</span><span class="sxs-lookup"><span data-stu-id="b5259-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5259-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="b5259-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="b5259-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="b5259-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b5259-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b5259-129">Especifica diversa información de conexión, incluidas las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="b5259-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b5259-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5259-130">Return value</span></span>

<span data-ttu-id="b5259-131">Base de datos</span><span class="sxs-lookup"><span data-stu-id="b5259-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="b5259-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5259-132">Remarks</span></span>

<span data-ttu-id="b5259-133">Puede utilizar los valores siguientes para el argumento options.</span><span class="sxs-lookup"><span data-stu-id="b5259-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5259-134">Configuración</span><span class="sxs-lookup"><span data-stu-id="b5259-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="b5259-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5259-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5259-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="b5259-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="b5259-137">Abre la base de datos en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b5259-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5259-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="b5259-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="b5259-139">(Opción predeterminada) Abre la base de datos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="b5259-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5259-140">Al abrir una base de datos, se agrega automáticamente a la colección **Databases**.</span><span class="sxs-lookup"><span data-stu-id="b5259-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="b5259-141">Se aplican determinadas consideraciones cuando se utiliza dbname:</span><span class="sxs-lookup"><span data-stu-id="b5259-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="b5259-142">Si se refiere a una base de datos que ya está abierta para que tenga acceso a ella otro usuario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b5259-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="b5259-143">Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b5259-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="b5259-144">Si es una cadena de longitud cero ("") y *Conectar* es "ODBC;", se muestra un cuadro de diálogo lista de todos los nombres de orígenes de datos ODBC para el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="b5259-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="b5259-145">Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.</span><span class="sxs-lookup"><span data-stu-id="b5259-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="b5259-146">[!NOTA] Cuando acceda a un origen de datos ODBC conectado a un motor de base de datos de Microsoft Access, podrá mejorar el rendimiento de la aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular los objetos [TableDef](tabledef-object-dao.md) uno por uno a tablas concretas del origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="b5259-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


