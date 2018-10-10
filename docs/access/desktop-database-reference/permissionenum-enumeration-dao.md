---
title: PermissionEnum Enumeration (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e87482940918f3e12713f2e207e2e590895838a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484928"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="75b41-102">PermissionEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="75b41-102">PermissionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="75b41-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75b41-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75b41-104">Se utiliza con la propiedad **Permissions** para especificar el tipo de permisos.</span><span class="sxs-lookup"><span data-stu-id="75b41-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75b41-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="75b41-105">Name</span></span></p></th>
<th><p><span data-ttu-id="75b41-106">Valor</span><span class="sxs-lookup"><span data-stu-id="75b41-106">Value</span></span></p></th>
<th><p><span data-ttu-id="75b41-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="75b41-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b41-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="75b41-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="75b41-109">1</span><span class="sxs-lookup"><span data-stu-id="75b41-109">1</span></span></p></td>
<td><p><span data-ttu-id="75b41-110">El usuario puede crear documentos nuevos (no es válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="75b41-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="75b41-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="75b41-112">8</span><span class="sxs-lookup"><span data-stu-id="75b41-112">8</span></span></p></td>
<td><p><span data-ttu-id="75b41-113">El usuario puede replicar una base de datos y cambiar su contraseña (no es válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="75b41-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="75b41-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="75b41-115">1</span><span class="sxs-lookup"><span data-stu-id="75b41-115">1</span></span></p></td>
<td><p><span data-ttu-id="75b41-p101">El usuario puede crear nuevas bases de datos. Esta opción sólo es válida en el contenedor de bases de datos en el archivo de información del grupo de trabajo (Systen.mdw). Esta constante no es válida para objetos Document.</span><span class="sxs-lookup"><span data-stu-id="75b41-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="75b41-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="75b41-120">4</span><span class="sxs-lookup"><span data-stu-id="75b41-120">4</span></span></p></td>
<td><p><span data-ttu-id="75b41-121">El usuario tiene acceso exclusivo a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="75b41-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="75b41-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="75b41-123">2</span><span class="sxs-lookup"><span data-stu-id="75b41-123">2</span></span></p></td>
<td><p><span data-ttu-id="75b41-124">El usuario puede abrir la base de datos.</span><span class="sxs-lookup"><span data-stu-id="75b41-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="75b41-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="75b41-126">65536</span><span class="sxs-lookup"><span data-stu-id="75b41-126">65536</span></span></p></td>
<td><p><span data-ttu-id="75b41-127">El usuario puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="75b41-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="75b41-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="75b41-129">128</span><span class="sxs-lookup"><span data-stu-id="75b41-129">128</span></span></p></td>
<td><p><span data-ttu-id="75b41-130">El usuario puede eliminar registros.</span><span class="sxs-lookup"><span data-stu-id="75b41-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="75b41-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="75b41-132">1048575</span><span class="sxs-lookup"><span data-stu-id="75b41-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="75b41-133">El usuario tiene acceso total al objeto.</span><span class="sxs-lookup"><span data-stu-id="75b41-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="75b41-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="75b41-135">32</span><span class="sxs-lookup"><span data-stu-id="75b41-135">32</span></span></p></td>
<td><p><span data-ttu-id="75b41-136">El usuario puede agregar registros.</span><span class="sxs-lookup"><span data-stu-id="75b41-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="75b41-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="75b41-138">0</span><span class="sxs-lookup"><span data-stu-id="75b41-138">0</span></span></p></td>
<td><p><span data-ttu-id="75b41-139">El usuario no tiene acceso al objeto (no es válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="75b41-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="75b41-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="75b41-141">4</span><span class="sxs-lookup"><span data-stu-id="75b41-141">4</span></span></p></td>
<td><p><span data-ttu-id="75b41-142">El usuario puede leer la definición de tabla, incluida la información de índice y de columnas.</span><span class="sxs-lookup"><span data-stu-id="75b41-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="75b41-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="75b41-144">131072</span><span class="sxs-lookup"><span data-stu-id="75b41-144">131072</span></span></p></td>
<td><p><span data-ttu-id="75b41-145">El usuario puede leer la información relacionada con la seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="75b41-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="75b41-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="75b41-147">64</span><span class="sxs-lookup"><span data-stu-id="75b41-147">64</span></span></p></td>
<td><p><span data-ttu-id="75b41-148">El usuario puede modificar registros.</span><span class="sxs-lookup"><span data-stu-id="75b41-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="75b41-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="75b41-150">20</span><span class="sxs-lookup"><span data-stu-id="75b41-150">20</span></span></p></td>
<td><p><span data-ttu-id="75b41-151">El usuario puede recuperar datos del objeto Document.</span><span class="sxs-lookup"><span data-stu-id="75b41-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="75b41-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="75b41-153">65548</span><span class="sxs-lookup"><span data-stu-id="75b41-153">65548</span></span></p></td>
<td><p><span data-ttu-id="75b41-154">El usuario puede modificar o eliminar la definición de tabla, incluida la información de índice y de columnas.</span><span class="sxs-lookup"><span data-stu-id="75b41-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b41-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="75b41-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="75b41-156">524288</span><span class="sxs-lookup"><span data-stu-id="75b41-156">524288</span></span></p></td>
<td><p><span data-ttu-id="75b41-157">El usuario puede cambiar el valor de la propiedad Owner.</span><span class="sxs-lookup"><span data-stu-id="75b41-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b41-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="75b41-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="75b41-159">262144</span><span class="sxs-lookup"><span data-stu-id="75b41-159">262144</span></span></p></td>
<td><p><span data-ttu-id="75b41-160">El usuario puede alterar los permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="75b41-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

