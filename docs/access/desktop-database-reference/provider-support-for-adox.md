---
title: Soporte del proveedor para ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301102"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="e90fe-102">Soporte del proveedor para ADOX</span><span class="sxs-lookup"><span data-stu-id="e90fe-102">Provider support for ADOX</span></span>


<span data-ttu-id="e90fe-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e90fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e90fe-p101">Algunas características de ADOX no son compatibles; depende de cuál sea su proveedor de datos de OLE DB. ADOX es totalmente compatible con [Proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). A continuación, se indican las características no compatibles con [Proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md), [Proveedor de Microsoft OLE DB para ODBC](microsoft-ole-db-provider-for-odbc.md) o [Proveedor de Microsoft OLE DB para Oracle](microsoft-ole-db-provider-for-oracle.md). ADOX no es compatible con ningún otro proveedor de Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e90fe-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="e90fe-108">Proveedor de Microsoft OLE DB para SQL Server</span><span class="sxs-lookup"><span data-stu-id="e90fe-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e90fe-109">Objeto o colección</span><span class="sxs-lookup"><span data-stu-id="e90fe-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="e90fe-110">Restricción de uso</span><span class="sxs-lookup"><span data-stu-id="e90fe-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-111">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-112">El método <strong>Create</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-113">Colección <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-114">Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="e90fe-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-115">Colección <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-116"><strong>Views</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-117">Colección <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-118">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-119">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-120">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-121">Colección <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-122">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-123">Colección <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-124"><strong>Users</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-125">Colección <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-126"><strong>Groups</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="e90fe-127">Proveedor de Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="e90fe-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e90fe-128">Objeto o colección</span><span class="sxs-lookup"><span data-stu-id="e90fe-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="e90fe-129">Restricción de uso</span><span class="sxs-lookup"><span data-stu-id="e90fe-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-130">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-131">El método <strong>Create</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-132">Colección <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-133">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="e90fe-134">Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="e90fe-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-135">Colección <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-136">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-137">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-138">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-139">Colección <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-140">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-141">Colección <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-142">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-143">Colección <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-144"><strong>Users</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-145">Colección <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-146"><strong>Groups</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="e90fe-147">Proveedor de Microsoft OLE DB para Oracle</span><span class="sxs-lookup"><span data-stu-id="e90fe-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e90fe-148">Objeto o colección</span><span class="sxs-lookup"><span data-stu-id="e90fe-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="e90fe-149">Restricción de uso</span><span class="sxs-lookup"><span data-stu-id="e90fe-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-150">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-151">El método <strong>Create</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-152">Colección <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-153">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="e90fe-154">Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="e90fe-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-155">Colección <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-156">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-157">Objeto <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-158">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-159">Objeto <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-160">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-161">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e90fe-162">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-163">Colección <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-164">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-165">Colección <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-166">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e90fe-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90fe-167">Colección <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-168"><strong>Users</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90fe-169">Colección <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="e90fe-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="e90fe-170"><strong>Groups</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e90fe-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

