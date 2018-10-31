---
title: RightsEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 40cd7f789461e5b354186c2d5b8f81ec18344435
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861984"
---
# <a name="rightsenum"></a><span data-ttu-id="7e0dc-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="7e0dc-102">RightsEnum</span></span>

<span data-ttu-id="7e0dc-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e0dc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7e0dc-104">Especifica los derechos o los permisos para un grupo o un usuario en un objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e0dc-105">Constante</span><span class="sxs-lookup"><span data-stu-id="7e0dc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7e0dc-106">Valor</span><span class="sxs-lookup"><span data-stu-id="7e0dc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7e0dc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e0dc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-109">16384</span><span class="sxs-lookup"><span data-stu-id="7e0dc-109">16384</span></span><br />
<span data-ttu-id="7e0dc-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-111">El usuario o el grupo tiene permiso para crear objetos nuevos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-113">65536</span><span class="sxs-lookup"><span data-stu-id="7e0dc-113">65536</span></span><br />
<span data-ttu-id="7e0dc-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-p101">El usuario o el grupo tienen permiso para eliminar datos de un objeto.
Para objetos tal como <strong>Tables</strong>, el usuario tiene permiso para eliminar valores de datos de los registros.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-118">256</span><span class="sxs-lookup"><span data-stu-id="7e0dc-118">256</span></span><br />
<span data-ttu-id="7e0dc-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-p102">El usuario o el grupo tiene permiso para quitar objetos del catálogo.
Por ejemplo, <strong>Tables</strong> se puede eliminar mediante un comando SQL DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-123">512</span><span class="sxs-lookup"><span data-stu-id="7e0dc-123">512</span></span><br />
<span data-ttu-id="7e0dc-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-125">El usuario o el grupo tiene permiso de acceso exclusivo al objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-127">536870912</span><span class="sxs-lookup"><span data-stu-id="7e0dc-127">536870912</span></span><br />
<span data-ttu-id="7e0dc-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-129">El usuario o el grupo tiene permiso para ejecutar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-131">268435456</span><span class="sxs-lookup"><span data-stu-id="7e0dc-131">268435456</span></span><br />
<span data-ttu-id="7e0dc-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-133">El usuario o el grupo tiene todos los permisos en el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-135">32768</span><span class="sxs-lookup"><span data-stu-id="7e0dc-135">32768</span></span><br />
<span data-ttu-id="7e0dc-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-p103">El usuario o el grupo tiene permiso para insertar el objeto.
Para objetos tales como <strong>Tables</strong>, el usuario tiene permiso para insertar datos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-p104">El usuario o el grupo tiene el número máximo de permisos que concede el proveedor.

Los permisos específicos dependen del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-144">0</span><span class="sxs-lookup"><span data-stu-id="7e0dc-144">0</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-145">El usuario o el grupo no tiene ningún permiso para el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="7e0dc-147">-2147483648</span></span><br />
<span data-ttu-id="7e0dc-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-p105">El usuario o el grupo tiene permiso para leer el objeto.
Para objetos tales como <a href="table-object-adox.md">Tables</a>, el usuario tiene permiso para leer los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-152">1024</span><span class="sxs-lookup"><span data-stu-id="7e0dc-152">1024</span></span><br />
<span data-ttu-id="7e0dc-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-154">El usuario o el grupo tiene permiso para leer el diseño para el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-156">131072</span><span class="sxs-lookup"><span data-stu-id="7e0dc-156">131072</span></span><br />
<span data-ttu-id="7e0dc-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-158">El usuario o el grupo puede ver, pero no cambiar, los permisos específicos para un objeto del catálogo.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-160">8192</span><span class="sxs-lookup"><span data-stu-id="7e0dc-160">8192</span></span><br />
<span data-ttu-id="7e0dc-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-162">El usuario o el grupo tiene permiso para hacer referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="7e0dc-164">1073741824</span></span><br />
<span data-ttu-id="7e0dc-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-p106">El usuario o el grupo tiene permiso para actualizar el objeto.
Para objetos tales como <strong>Tables</strong>, el usuario tiene permiso para actualizar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-169">4096</span><span class="sxs-lookup"><span data-stu-id="7e0dc-169">4096</span></span><br />
<span data-ttu-id="7e0dc-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-171">El usuario o el grupo tiene permiso para conceder permisos para el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-173">2048</span><span class="sxs-lookup"><span data-stu-id="7e0dc-173">2048</span></span><br />
<span data-ttu-id="7e0dc-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-175">El usuario o el grupo tiene permiso para modificar el diseño para el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e0dc-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-177">524288</span><span class="sxs-lookup"><span data-stu-id="7e0dc-177">524288</span></span><br />
<span data-ttu-id="7e0dc-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-179">El usuario o el grupo tiene permiso para modificar el propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e0dc-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="7e0dc-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="7e0dc-181">262144</span><span class="sxs-lookup"><span data-stu-id="7e0dc-181">262144</span></span><br />
<span data-ttu-id="7e0dc-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="7e0dc-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="7e0dc-183">El usuario o el grupo puede modificar los permisos específicos para un objeto del catálogo.</span><span class="sxs-lookup"><span data-stu-id="7e0dc-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

