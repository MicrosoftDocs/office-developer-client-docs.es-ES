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
# <a name="provider-support-for-adox"></a><span data-ttu-id="8697c-102">Soporte del proveedor para ADOX</span><span class="sxs-lookup"><span data-stu-id="8697c-102">Provider support for ADOX</span></span>


<span data-ttu-id="8697c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8697c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8697c-p101">Algunas características de ADOX no son compatibles; depende de cuál sea su proveedor de datos de OLE DB. ADOX es totalmente compatible con [Proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). A continuación, se indican las características no compatibles con [Proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md), [Proveedor de Microsoft OLE DB para ODBC](microsoft-ole-db-provider-for-odbc.md) o [Proveedor de Microsoft OLE DB para Oracle](microsoft-ole-db-provider-for-oracle.md). ADOX no es compatible con ningún otro proveedor de Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8697c-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="8697c-108">Proveedor de Microsoft OLE DB para SQL Server</span><span class="sxs-lookup"><span data-stu-id="8697c-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8697c-109">Objeto o colección</span><span class="sxs-lookup"><span data-stu-id="8697c-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="8697c-110">Restricción de uso</span><span class="sxs-lookup"><span data-stu-id="8697c-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8697c-111">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-112">El método <strong>Create</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-113">Colección <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-114">Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="8697c-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-115">Colección <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-116"><strong>Views</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-117">Colección <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-118">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-119">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-120">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-121">Colección <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-122">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-123">Colección <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-124"><strong>Users</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-125">Colección <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-126"><strong>Groups</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="8697c-127">Proveedor de Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="8697c-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8697c-128">Objeto o colección</span><span class="sxs-lookup"><span data-stu-id="8697c-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="8697c-129">Restricción de uso</span><span class="sxs-lookup"><span data-stu-id="8697c-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8697c-130">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-131">El método <strong>Create</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-132">Colección <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-133">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="8697c-134">Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="8697c-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-135">Colección <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-136">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-137">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-138">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-139">Colección <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-140">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-141">Colección <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-142">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-143">Colección <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-144"><strong>Users</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-145">Colección <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-146"><strong>Groups</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="8697c-147">Proveedor de Microsoft OLE DB para Oracle</span><span class="sxs-lookup"><span data-stu-id="8697c-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8697c-148">Objeto o colección</span><span class="sxs-lookup"><span data-stu-id="8697c-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="8697c-149">Restricción de uso</span><span class="sxs-lookup"><span data-stu-id="8697c-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8697c-150">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-151">El método <strong>Create</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-152">Colección <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-153">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="8697c-154">Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="8697c-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-155">Colección <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-156">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-157">Objeto <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-158">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-159">Objeto <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-160">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-161">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8697c-162">La propiedad <strong>Comando</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-163">Colección <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-164">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-165">Colección <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-166">Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8697c-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8697c-167">Colección <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-168"><strong>Users</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8697c-169">Colección <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="8697c-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8697c-170"><strong>Groups</strong> no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8697c-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

