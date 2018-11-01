---
title: Usar objetos de datos ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y la administración de las bases de datos de Access y sus datos relacionados, mediante el uso de Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7e8e7e6abeea9cca86c928760eddb990517a207
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887512"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="6d945-103">Usar objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="6d945-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="6d945-104">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d945-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d945-105">Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y la administración de las bases de datos de Access y sus datos relacionados, mediante el uso de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6d945-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="6d945-106">Objetos de datos ActiveX de Microsoft (Microsoft ActiveX Data Objects, ADO)</span><span class="sxs-lookup"><span data-stu-id="6d945-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="6d945-107">ADO contiene los objetos necesarios para crear, mantener y eliminar registros en un origen de datos dado.</span><span class="sxs-lookup"><span data-stu-id="6d945-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="6d945-108">Microsoft ADO Ext. DDL y seguridad (ADOX)</span><span class="sxs-lookup"><span data-stu-id="6d945-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="6d945-109">ADOX proporciona los objetos de lenguaje de definición de datos (DDL) necesarios para crear una nueva base de datos y los objetos que contiene además de los objetos necesarios para administrar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="6d945-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="6d945-110">Biblioteca de Microsoft Jet y Replication Objects 2.5 (JRO)</span><span class="sxs-lookup"><span data-stu-id="6d945-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="6d945-111">Debido a que los objetos ADO fueron diseñados para trabajar con muchas bases de datos además de las bases de datos Microsoft Jet, funciones específicas de Jet se incluyeron como parte de la biblioteca JRO.</span><span class="sxs-lookup"><span data-stu-id="6d945-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="6d945-112">En la tabla siguiente se muestran la funcionalidad que proporcionan los distintos modelos de objetos comparados con DAO.</span><span class="sxs-lookup"><span data-stu-id="6d945-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="6d945-113">Característica</span><span class="sxs-lookup"><span data-stu-id="6d945-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="6d945-114">DAO</span><span class="sxs-lookup"><span data-stu-id="6d945-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="6d945-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="6d945-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="6d945-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="6d945-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="6d945-117">JRO</span><span class="sxs-lookup"><span data-stu-id="6d945-117">JRO</span></span><br />
<span data-ttu-id="6d945-118">(Sólo para MDB)</span><span class="sxs-lookup"><span data-stu-id="6d945-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d945-119">Crear conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="6d945-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="6d945-120">X</span><span class="sxs-lookup"><span data-stu-id="6d945-120">X</span></span></p></td>
<td><p><span data-ttu-id="6d945-121">X</span><span class="sxs-lookup"><span data-stu-id="6d945-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-122">Editar propiedades de inicio.</span><span class="sxs-lookup"><span data-stu-id="6d945-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="6d945-123">X</span><span class="sxs-lookup"><span data-stu-id="6d945-123">X</span></span></p></td>
<td><p><span data-ttu-id="6d945-124">X\*\*</span><span class="sxs-lookup"><span data-stu-id="6d945-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-125">Admitir ANSI92 SQL.\* \*\*</span><span class="sxs-lookup"><span data-stu-id="6d945-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-126">X</span><span class="sxs-lookup"><span data-stu-id="6d945-126">X</span></span></p></td>
<td><p><span data-ttu-id="6d945-127">X</span><span class="sxs-lookup"><span data-stu-id="6d945-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-128">Crear tablas.</span><span class="sxs-lookup"><span data-stu-id="6d945-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="6d945-129">X</span><span class="sxs-lookup"><span data-stu-id="6d945-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-130">X</span><span class="sxs-lookup"><span data-stu-id="6d945-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-131">Crear nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="6d945-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="6d945-132">X</span><span class="sxs-lookup"><span data-stu-id="6d945-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-133">X\*</span><span class="sxs-lookup"><span data-stu-id="6d945-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-134">Editar propiedades de tabla existente.</span><span class="sxs-lookup"><span data-stu-id="6d945-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="6d945-135">X</span><span class="sxs-lookup"><span data-stu-id="6d945-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-136">X</span><span class="sxs-lookup"><span data-stu-id="6d945-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-137">Crear relaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="6d945-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="6d945-138">X</span><span class="sxs-lookup"><span data-stu-id="6d945-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-139">X\*</span><span class="sxs-lookup"><span data-stu-id="6d945-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-140">Editar configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6d945-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="6d945-141">X</span><span class="sxs-lookup"><span data-stu-id="6d945-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-142">X\*</span><span class="sxs-lookup"><span data-stu-id="6d945-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-143">Compatibilidad con el atributo Compression para datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="6d945-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-144">X</span><span class="sxs-lookup"><span data-stu-id="6d945-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-145">Editar almacenados, básica consultas o vistas SQL.</span><span class="sxs-lookup"><span data-stu-id="6d945-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="6d945-146">X</span><span class="sxs-lookup"><span data-stu-id="6d945-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-147">X\*</span><span class="sxs-lookup"><span data-stu-id="6d945-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-148">Crear consultas permanentes que son accesibles sólo mediante código.</span><span class="sxs-lookup"><span data-stu-id="6d945-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-149">X\*</span><span class="sxs-lookup"><span data-stu-id="6d945-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-150">Crear consultas accesibles por medio de la interfaz de usuario y código del contenedor de base de datos</span><span class="sxs-lookup"><span data-stu-id="6d945-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="6d945-151">X</span><span class="sxs-lookup"><span data-stu-id="6d945-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-152">Compactar o codificar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6d945-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="6d945-153">X</span><span class="sxs-lookup"><span data-stu-id="6d945-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-154">X4</span><span class="sxs-lookup"><span data-stu-id="6d945-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-155">Actualizar la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="6d945-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="6d945-156">X</span><span class="sxs-lookup"><span data-stu-id="6d945-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-157">X</span><span class="sxs-lookup"><span data-stu-id="6d945-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-158">¿Hacer replicable la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6d945-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="6d945-159">X</span><span class="sxs-lookup"><span data-stu-id="6d945-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-160">X3</span><span class="sxs-lookup"><span data-stu-id="6d945-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-161">Hacer réplicas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6d945-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="6d945-162">X</span><span class="sxs-lookup"><span data-stu-id="6d945-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-163">X3</span><span class="sxs-lookup"><span data-stu-id="6d945-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-164">Sincronizar réplicas.</span><span class="sxs-lookup"><span data-stu-id="6d945-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="6d945-165">X</span><span class="sxs-lookup"><span data-stu-id="6d945-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6d945-166">X3</span><span class="sxs-lookup"><span data-stu-id="6d945-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-167">Editar propiedades de base de datos.</span><span class="sxs-lookup"><span data-stu-id="6d945-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="6d945-168">X</span><span class="sxs-lookup"><span data-stu-id="6d945-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d945-169">Crear propiedades de base de datos personalizada.</span><span class="sxs-lookup"><span data-stu-id="6d945-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="6d945-170">X</span><span class="sxs-lookup"><span data-stu-id="6d945-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d945-171">Editar propiedades de columna de tabla.</span><span class="sxs-lookup"><span data-stu-id="6d945-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="6d945-172">X</span><span class="sxs-lookup"><span data-stu-id="6d945-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6d945-p101">\* Sólo disponible cuando se trabaja con bases de datos Microsoft Access. Las versiones futuras del proveedor SQL pueden proporcionar estas funciones en proyectos de Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="6d945-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="6d945-175">\*\* Sólo disponible cuando se trabaja con proyectos de Access.</span><span class="sxs-lookup"><span data-stu-id="6d945-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="6d945-176">\*\*\*Aunque el motor de base de datos de Access admite en parte ANSI 92 SQL, todavía no es totalmente compatible con ANSI92.</span><span class="sxs-lookup"><span data-stu-id="6d945-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="6d945-177">1 objeto usa **conexión** a base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="6d945-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="6d945-178">Objeto usa **catálogo** 2 a base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="6d945-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="6d945-179">Objeto usa **réplica** 3 a base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="6d945-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="6d945-180">Objeto usa **JetEngine** 4 a base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="6d945-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="6d945-181">A diferencia de DAO, objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos que no sean de Jet de siempre y cuando el proveedor para las bases de datos admite esa acción.</span><span class="sxs-lookup"><span data-stu-id="6d945-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


