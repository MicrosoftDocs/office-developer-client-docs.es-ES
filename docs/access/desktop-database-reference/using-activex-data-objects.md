---
title: Usar objetos de datos de ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access proporciona tres modelos de objetos para usar en la creación, el mantenimiento y la administración de las bases de datos de Access y sus datos relacionados mediante el uso de Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312743"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="fd552-103">Usar objetos de datos de ActiveX</span><span class="sxs-lookup"><span data-stu-id="fd552-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="fd552-104">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd552-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd552-105">Microsoft Access proporciona tres modelos de objetos para usar en la creación, el mantenimiento y la administración de las bases de datos de Access y sus datos relacionados mediante el uso de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fd552-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="fd552-106">Objetos de datos ActiveX de Microsoft (Microsoft ActiveX Data Objects, ADO)</span><span class="sxs-lookup"><span data-stu-id="fd552-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="fd552-107">ADO contiene los objetos necesarios para crear, mantener y eliminar registros en un origen de datos dado.</span><span class="sxs-lookup"><span data-stu-id="fd552-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="fd552-108">Microsoft ADO ext. for DDL and Security (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fd552-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="fd552-109">ADOX proporciona los objetos de lenguaje de definición de datos (DDL) necesarios para crear una nueva base de datos y los objetos que contiene además de los objetos necesarios para administrar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="fd552-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="fd552-110">Microsoft Jet and Replication Objects 2,5 Library (JRO)</span><span class="sxs-lookup"><span data-stu-id="fd552-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="fd552-111">Como los objetos ADO se diseñaron para trabajar con muchas bases de datos además de las bases de datos Microsoft Jet, la funcionalidad específica de jet se dividió en la biblioteca JRO.</span><span class="sxs-lookup"><span data-stu-id="fd552-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="fd552-112">En la tabla siguiente se muestran la funcionalidad que proporcionan los distintos modelos de objetos comparados con DAO.</span><span class="sxs-lookup"><span data-stu-id="fd552-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="fd552-113">Funcionalidad</span><span class="sxs-lookup"><span data-stu-id="fd552-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="fd552-114">DAO</span><span class="sxs-lookup"><span data-stu-id="fd552-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="fd552-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="fd552-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="fd552-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="fd552-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="fd552-117">JRO</span><span class="sxs-lookup"><span data-stu-id="fd552-117">JRO</span></span><br />
<span data-ttu-id="fd552-118">(Solo mdb)</span><span class="sxs-lookup"><span data-stu-id="fd552-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd552-119">Crear conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="fd552-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="fd552-120">X</span><span class="sxs-lookup"><span data-stu-id="fd552-120">X</span></span></p></td>
<td><p><span data-ttu-id="fd552-121">X</span><span class="sxs-lookup"><span data-stu-id="fd552-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-122">Edite las propiedades de inicio.</span><span class="sxs-lookup"><span data-stu-id="fd552-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="fd552-123">X</span><span class="sxs-lookup"><span data-stu-id="fd552-123">X</span></span></p></td>
<td><p><span data-ttu-id="fd552-124">X \* \*</span><span class="sxs-lookup"><span data-stu-id="fd552-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-125">Admitir ANSI92 SQL. \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fd552-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-126">X</span><span class="sxs-lookup"><span data-stu-id="fd552-126">X</span></span></p></td>
<td><p><span data-ttu-id="fd552-127">X</span><span class="sxs-lookup"><span data-stu-id="fd552-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-128">Crear tablas.</span><span class="sxs-lookup"><span data-stu-id="fd552-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="fd552-129">X</span><span class="sxs-lookup"><span data-stu-id="fd552-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-130">X</span><span class="sxs-lookup"><span data-stu-id="fd552-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-131">Crear una nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="fd552-132">X</span><span class="sxs-lookup"><span data-stu-id="fd552-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-133">Días</span><span class="sxs-lookup"><span data-stu-id="fd552-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-134">Edite las propiedades de la tabla existente.</span><span class="sxs-lookup"><span data-stu-id="fd552-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="fd552-135">X</span><span class="sxs-lookup"><span data-stu-id="fd552-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-136">X</span><span class="sxs-lookup"><span data-stu-id="fd552-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-137">Crear relaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="fd552-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="fd552-138">X</span><span class="sxs-lookup"><span data-stu-id="fd552-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-139">Días</span><span class="sxs-lookup"><span data-stu-id="fd552-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-140">Modificar la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fd552-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="fd552-141">X</span><span class="sxs-lookup"><span data-stu-id="fd552-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-142">Días</span><span class="sxs-lookup"><span data-stu-id="fd552-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-143">Compatibilidad con el atributo de compresión de datos de columna.</span><span class="sxs-lookup"><span data-stu-id="fd552-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-144">X</span><span class="sxs-lookup"><span data-stu-id="fd552-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-145">Editar vistas o consultas SQL básicas almacenadas.</span><span class="sxs-lookup"><span data-stu-id="fd552-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="fd552-146">X</span><span class="sxs-lookup"><span data-stu-id="fd552-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-147">Días</span><span class="sxs-lookup"><span data-stu-id="fd552-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-148">Crear consultas permanentes que son accesibles sólo mediante código.</span><span class="sxs-lookup"><span data-stu-id="fd552-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-149">Días</span><span class="sxs-lookup"><span data-stu-id="fd552-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-150">Crear consultas accesibles por medio de la interfaz de usuario y código del contenedor de base de datos</span><span class="sxs-lookup"><span data-stu-id="fd552-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="fd552-151">X</span><span class="sxs-lookup"><span data-stu-id="fd552-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-152">Compactar o codificar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="fd552-153">X</span><span class="sxs-lookup"><span data-stu-id="fd552-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-154">4</span><span class="sxs-lookup"><span data-stu-id="fd552-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-155">Actualizar caché.</span><span class="sxs-lookup"><span data-stu-id="fd552-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="fd552-156">X</span><span class="sxs-lookup"><span data-stu-id="fd552-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-157">X</span><span class="sxs-lookup"><span data-stu-id="fd552-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-158">Hacer replicable la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="fd552-159">X</span><span class="sxs-lookup"><span data-stu-id="fd552-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-160">X3</span><span class="sxs-lookup"><span data-stu-id="fd552-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-161">Realizar réplicas de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="fd552-162">X</span><span class="sxs-lookup"><span data-stu-id="fd552-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-163">X3</span><span class="sxs-lookup"><span data-stu-id="fd552-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-164">Sincronizar réplicas.</span><span class="sxs-lookup"><span data-stu-id="fd552-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="fd552-165">X</span><span class="sxs-lookup"><span data-stu-id="fd552-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd552-166">X3</span><span class="sxs-lookup"><span data-stu-id="fd552-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-167">Edite las propiedades de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="fd552-168">X</span><span class="sxs-lookup"><span data-stu-id="fd552-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd552-169">Crear propiedades de base de datos personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fd552-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="fd552-170">X</span><span class="sxs-lookup"><span data-stu-id="fd552-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd552-171">Edite las propiedades de columna de tabla.</span><span class="sxs-lookup"><span data-stu-id="fd552-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="fd552-172">X</span><span class="sxs-lookup"><span data-stu-id="fd552-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd552-p101">\* Sólo disponible cuando se trabaja con bases de datos Microsoft Access. Las versiones futuras del proveedor SQL pueden proporcionar estas funciones en proyectos de Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="fd552-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="fd552-175">\*\* Sólo disponible cuando se trabaja con proyectos de Access.</span><span class="sxs-lookup"><span data-stu-id="fd552-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="fd552-176">\*\*\*Aunque el motor de base de datos de Access admite cierto ANSI 92 SQL, todavía no es totalmente compatible con ANSI92.</span><span class="sxs-lookup"><span data-stu-id="fd552-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="fd552-177">1 utiliza el objeto **Connection** para hacer referencia a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="fd552-178">2 usa el objeto **Catalog** para hacer referencia a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="fd552-179">3 usa el objeto **Replica** para hacer referencia a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="fd552-180">4 usa el objeto **JetEngine** para hacer referencia a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fd552-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="fd552-181">A diferencia de DAO, los objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos distintas de jet, siempre que el proveedor de dichas bases de datos admita esa acción.</span><span class="sxs-lookup"><span data-stu-id="fd552-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


