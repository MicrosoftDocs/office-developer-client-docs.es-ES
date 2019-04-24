---
title: Las rightsenum (referencia de base de datos de escritorio de Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306492"
---
# <a name="rightsenum"></a><span data-ttu-id="c5a6e-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="c5a6e-102">RightsEnum</span></span>

<span data-ttu-id="c5a6e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5a6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5a6e-104">Especifica los derechos o los permisos para un grupo o un usuario en un objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5a6e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c5a6e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c5a6e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c5a6e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c5a6e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5a6e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-109">16384</span><span class="sxs-lookup"><span data-stu-id="c5a6e-109">16384</span></span><br />
<span data-ttu-id="c5a6e-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-111">El usuario o el grupo tiene permiso para crear objetos nuevos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-113">65536</span><span class="sxs-lookup"><span data-stu-id="c5a6e-113">65536</span></span><br />
<span data-ttu-id="c5a6e-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-p101">El usuario o el grupo tienen permiso para eliminar datos de un objeto.
Para objetos tal como <strong>Tables</strong>, el usuario tiene permiso para eliminar valores de datos de los registros.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-118">256</span><span class="sxs-lookup"><span data-stu-id="c5a6e-118">256</span></span><br />
<span data-ttu-id="c5a6e-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-p102">El usuario o el grupo tiene permiso para quitar objetos del catálogo.
Por ejemplo, <strong>Tables</strong> se puede eliminar mediante un comando SQL DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-123">512</span><span class="sxs-lookup"><span data-stu-id="c5a6e-123">512</span></span><br />
<span data-ttu-id="c5a6e-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-125">El usuario o el grupo tiene permiso de acceso exclusivo al objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-127">536870912</span><span class="sxs-lookup"><span data-stu-id="c5a6e-127">536870912</span></span><br />
<span data-ttu-id="c5a6e-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-129">El usuario o el grupo tiene permiso para ejecutar el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-131">268435456</span><span class="sxs-lookup"><span data-stu-id="c5a6e-131">268435456</span></span><br />
<span data-ttu-id="c5a6e-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-133">El usuario o el grupo tiene todos los permisos en el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-135">32768</span><span class="sxs-lookup"><span data-stu-id="c5a6e-135">32768</span></span><br />
<span data-ttu-id="c5a6e-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-p103">El usuario o el grupo tiene permiso para insertar el objeto.
Para objetos tales como <strong>Tables</strong>, el usuario tiene permiso para insertar datos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-141">El usuario o el grupo tiene el número máximo de permisos que concede el proveedor.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-141">The user or group has the maximum number of permissions allowed by the provider.</span></span> <span data-ttu-id="c5a6e-142">Los permisos específicos dependen del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-142">Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-144">comprendi</span><span class="sxs-lookup"><span data-stu-id="c5a6e-144">0</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-145">El usuario o el grupo no tiene ningún permiso para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="c5a6e-147">-2147483648</span></span><br />
<span data-ttu-id="c5a6e-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-p105">El usuario o el grupo tiene permiso para leer el objeto.
Para objetos tales como <a href="table-object-adox.md">Tables</a>, el usuario tiene permiso para leer los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-152">1024</span><span class="sxs-lookup"><span data-stu-id="c5a6e-152">1024</span></span><br />
<span data-ttu-id="c5a6e-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-154">El usuario o el grupo tiene permiso para leer el diseño para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-156">131072</span><span class="sxs-lookup"><span data-stu-id="c5a6e-156">131072</span></span><br />
<span data-ttu-id="c5a6e-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-158">El usuario o el grupo puede ver, pero no cambiar, los permisos específicos para un objeto del catálogo.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-160">8192</span><span class="sxs-lookup"><span data-stu-id="c5a6e-160">8192</span></span><br />
<span data-ttu-id="c5a6e-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-162">El usuario o el grupo tiene permiso para hacer referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="c5a6e-164">1073741824</span></span><br />
<span data-ttu-id="c5a6e-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-p106">El usuario o el grupo tiene permiso para actualizar el objeto.
Para objetos tales como <strong>Tables</strong>, el usuario tiene permiso para actualizar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-169">4096</span><span class="sxs-lookup"><span data-stu-id="c5a6e-169">4096</span></span><br />
<span data-ttu-id="c5a6e-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-171">El usuario o el grupo tiene permiso para conceder permisos para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-173">2048</span><span class="sxs-lookup"><span data-stu-id="c5a6e-173">2048</span></span><br />
<span data-ttu-id="c5a6e-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-175">El usuario o el grupo tiene permiso para modificar el diseño para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a6e-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-177">524288</span><span class="sxs-lookup"><span data-stu-id="c5a6e-177">524288</span></span><br />
<span data-ttu-id="c5a6e-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-179">El usuario o el grupo tiene permiso para modificar el propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a6e-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="c5a6e-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a6e-181">262144</span><span class="sxs-lookup"><span data-stu-id="c5a6e-181">262144</span></span><br />
<span data-ttu-id="c5a6e-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="c5a6e-183">El usuario o el grupo puede modificar los permisos específicos para un objeto del catálogo.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

