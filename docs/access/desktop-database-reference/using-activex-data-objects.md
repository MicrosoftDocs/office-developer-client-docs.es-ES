---
title: Utilizar objetos de datos ActiveX
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484457"
---
# <a name="using-activex-data-objects"></a><span data-ttu-id="481e1-102">Utilizar objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="481e1-102">Using ActiveX Data Objects</span></span>


<span data-ttu-id="481e1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="481e1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="481e1-104">Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y administración de bases de datos de Access y de sus datos relacionados, mediante la utilización de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="481e1-104">Microsoft Access provides three object models to use in the creation, maintaining and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="481e1-105">Objetos de datos ActiveX de Microsoft (Microsoft ActiveX Data Objects, ADO)</span><span class="sxs-lookup"><span data-stu-id="481e1-105">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="481e1-106">ADO contiene los objetos necesarios para crear, mantener y eliminar registros en un origen de datos dado.</span><span class="sxs-lookup"><span data-stu-id="481e1-106">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="481e1-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span><span class="sxs-lookup"><span data-stu-id="481e1-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span></span>

<span data-ttu-id="481e1-108">ADOX proporciona los objetos del lenguaje de definición de datos (Data Definition Language, DDL) necesarios para crear una nueva base de datos y los objetos que contiene además de los objetos necesarios para administrar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="481e1-108">ADOX provides the Data Definition Language(DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

<span data-ttu-id="481e1-109">**Microsoft Jet and Replication Objects 2,5 Library (JRO)**</span><span class="sxs-lookup"><span data-stu-id="481e1-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span></span>

<span data-ttu-id="481e1-110">Puesto que los objetos ADO fueron diseñados para trabajar con muchas bases de datos además de bases de datos Microsoft Jet, las funciones específicas de Jet se incluyeron como parte de la biblioteca JRO.</span><span class="sxs-lookup"><span data-stu-id="481e1-110">Since ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="481e1-111">En la tabla siguiente se muestran la funcionalidad que proporcionan los distintos modelos de objetos comparados con DAO.</span><span class="sxs-lookup"><span data-stu-id="481e1-111">The following table lists the functionality provided by each compared to DAO.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="481e1-112">Característica</span><span class="sxs-lookup"><span data-stu-id="481e1-112">Functionality</span></span></p></th>
<th><p><span data-ttu-id="481e1-113">DAO</span><span class="sxs-lookup"><span data-stu-id="481e1-113">DAO</span></span></p></th>
<th><p><span data-ttu-id="481e1-114">ADO1</span><span class="sxs-lookup"><span data-stu-id="481e1-114">ADO1</span></span></p></th>
<th><p><span data-ttu-id="481e1-115">ADOX2</span><span class="sxs-lookup"><span data-stu-id="481e1-115">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="481e1-116">JRO</span><span class="sxs-lookup"><span data-stu-id="481e1-116">JRO</span></span><br />
<span data-ttu-id="481e1-117">(Sólo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="481e1-117">(MDB's Only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="481e1-118">Crear conjuntos de registros</span><span class="sxs-lookup"><span data-stu-id="481e1-118">Create Recordsets</span></span></p></td>
<td><p><span data-ttu-id="481e1-119">X</span><span class="sxs-lookup"><span data-stu-id="481e1-119">X</span></span></p></td>
<td><p><span data-ttu-id="481e1-120">X</span><span class="sxs-lookup"><span data-stu-id="481e1-120">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-121">Modificar propiedades de inicio</span><span class="sxs-lookup"><span data-stu-id="481e1-121">Edit Startup properties</span></span></p></td>
<td><p><span data-ttu-id="481e1-122">X</span><span class="sxs-lookup"><span data-stu-id="481e1-122">X</span></span></p></td>
<td><p><span data-ttu-id="481e1-123">X\*\*</span><span class="sxs-lookup"><span data-stu-id="481e1-123">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-124">Admitir ANSI92 SQL\*\*\*</span><span class="sxs-lookup"><span data-stu-id="481e1-124">Support ANSI92 SQL\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-125">X</span><span class="sxs-lookup"><span data-stu-id="481e1-125">X</span></span></p></td>
<td><p><span data-ttu-id="481e1-126">X</span><span class="sxs-lookup"><span data-stu-id="481e1-126">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-127">Crear tablas</span><span class="sxs-lookup"><span data-stu-id="481e1-127">Create Tables</span></span></p></td>
<td><p><span data-ttu-id="481e1-128">X</span><span class="sxs-lookup"><span data-stu-id="481e1-128">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-129">X</span><span class="sxs-lookup"><span data-stu-id="481e1-129">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-130">Crear nueva base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-130">Create New Database</span></span></p></td>
<td><p><span data-ttu-id="481e1-131">X</span><span class="sxs-lookup"><span data-stu-id="481e1-131">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-132">X\*</span><span class="sxs-lookup"><span data-stu-id="481e1-132">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-133">Modificar propiedades de tabla existente</span><span class="sxs-lookup"><span data-stu-id="481e1-133">Edit Existing Table properties</span></span></p></td>
<td><p><span data-ttu-id="481e1-134">X</span><span class="sxs-lookup"><span data-stu-id="481e1-134">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-135">X</span><span class="sxs-lookup"><span data-stu-id="481e1-135">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-136">Crear relaciones de tablas</span><span class="sxs-lookup"><span data-stu-id="481e1-136">Create table relationships</span></span></p></td>
<td><p><span data-ttu-id="481e1-137">X</span><span class="sxs-lookup"><span data-stu-id="481e1-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-138">X\*</span><span class="sxs-lookup"><span data-stu-id="481e1-138">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-139">Modificar la configuración de seguridad</span><span class="sxs-lookup"><span data-stu-id="481e1-139">Edit security settings</span></span></p></td>
<td><p><span data-ttu-id="481e1-140">X</span><span class="sxs-lookup"><span data-stu-id="481e1-140">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-141">X\*</span><span class="sxs-lookup"><span data-stu-id="481e1-141">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-142">Compatibilidad con el atributo Compression para datos de columnas</span><span class="sxs-lookup"><span data-stu-id="481e1-142">Support for Compression attribute for column data</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-143">X</span><span class="sxs-lookup"><span data-stu-id="481e1-143">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-144">Modificar consultas o vistas SQL básicas almacenadas</span><span class="sxs-lookup"><span data-stu-id="481e1-144">Edit stored, basic SQL queries or views</span></span></p></td>
<td><p><span data-ttu-id="481e1-145">X</span><span class="sxs-lookup"><span data-stu-id="481e1-145">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-146">X\*</span><span class="sxs-lookup"><span data-stu-id="481e1-146">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-147">Crear consultas permanentes que son accesibles sólo mediante código.</span><span class="sxs-lookup"><span data-stu-id="481e1-147">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-148">X\*</span><span class="sxs-lookup"><span data-stu-id="481e1-148">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-149">Crear consultas accesibles por medio de la interfaz de usuario y código del contenedor de base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-149">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="481e1-150">X</span><span class="sxs-lookup"><span data-stu-id="481e1-150">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-151">Compactar o codificar la base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-151">Compact/Encode database</span></span></p></td>
<td><p><span data-ttu-id="481e1-152">X</span><span class="sxs-lookup"><span data-stu-id="481e1-152">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-153">X4</span><span class="sxs-lookup"><span data-stu-id="481e1-153">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-154">Actualizar la caché</span><span class="sxs-lookup"><span data-stu-id="481e1-154">Refresh Cache</span></span></p></td>
<td><p><span data-ttu-id="481e1-155">X</span><span class="sxs-lookup"><span data-stu-id="481e1-155">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-156">X</span><span class="sxs-lookup"><span data-stu-id="481e1-156">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-157">Hacer replicable la base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-157">Make Database Replicable</span></span></p></td>
<td><p><span data-ttu-id="481e1-158">X</span><span class="sxs-lookup"><span data-stu-id="481e1-158">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-159">X3</span><span class="sxs-lookup"><span data-stu-id="481e1-159">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-160">Hacer réplicas de la base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-160">Make Database Replicas</span></span></p></td>
<td><p><span data-ttu-id="481e1-161">X</span><span class="sxs-lookup"><span data-stu-id="481e1-161">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-162">X3</span><span class="sxs-lookup"><span data-stu-id="481e1-162">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-163">Sincronizar réplicas</span><span class="sxs-lookup"><span data-stu-id="481e1-163">Synchronize Replicas</span></span></p></td>
<td><p><span data-ttu-id="481e1-164">X</span><span class="sxs-lookup"><span data-stu-id="481e1-164">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="481e1-165">X3</span><span class="sxs-lookup"><span data-stu-id="481e1-165">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-166">Modificar las propiedades de base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-166">Edit Database properties</span></span></p></td>
<td><p><span data-ttu-id="481e1-167">X</span><span class="sxs-lookup"><span data-stu-id="481e1-167">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="481e1-168">Crear propiedades personalizadas de base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-168">Create custom database properties</span></span></p></td>
<td><p><span data-ttu-id="481e1-169">X</span><span class="sxs-lookup"><span data-stu-id="481e1-169">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="481e1-170">Modificar propiedades de columna de tabla</span><span class="sxs-lookup"><span data-stu-id="481e1-170">Edit table column properties</span></span></p></td>
<td><p><span data-ttu-id="481e1-171">X</span><span class="sxs-lookup"><span data-stu-id="481e1-171">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="481e1-p101">\* Sólo disponible cuando se trabaja con bases de datos Microsoft Access. Las versiones futuras del proveedor SQL pueden proporcionar estas funciones en proyectos de Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="481e1-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="481e1-174">\*\* Sólo disponible cuando se trabaja con proyectos de Access.</span><span class="sxs-lookup"><span data-stu-id="481e1-174">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="481e1-175">\*\*\* Aunque el motor de base de datos de Access admite en parte ANSI 92 SQL, todavía no es totalmente compatible con ANSI92.</span><span class="sxs-lookup"><span data-stu-id="481e1-175">\*\*\* Though the Access database engine does support some ANSI 92 SQL it is not yet fully ANSI92 compliant.</span></span>

<span data-ttu-id="481e1-176">1Utiliza el objeto **Connection** para hacer referencia a la base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-176">1 Uses **Connection** object to reference to database</span></span>

<span data-ttu-id="481e1-177">2Utiliza el objeto **Catalog** para hacer referencia a la base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-177">2 Uses **Catalog** object to reference database</span></span>

<span data-ttu-id="481e1-178">3Utiliza el objeto **Replica** para hacer referencia a la base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-178">3 Uses **Replica** object to reference database</span></span>

<span data-ttu-id="481e1-179">4Utiliza el objeto **JetEngine** para hacer referencia a la base de datos</span><span class="sxs-lookup"><span data-stu-id="481e1-179">4 Uses **JetEngine** object to reference database</span></span>


> [!NOTE]
> <P><span data-ttu-id="481e1-180">[!NOTA] A diferencia de DAO, los objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos diferentes de Jet, siempre que el proveedor de éstas admita esa acción.</span><span class="sxs-lookup"><span data-stu-id="481e1-180">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other then Jet as long as the provider for those databases supports that action.</span></span></P>


