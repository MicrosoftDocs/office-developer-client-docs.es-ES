---
title: ConnectModeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6a09ea4d781e5560e335c2e75fc2da9a5508bae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874009"
---
# <a name="connectmodeenum"></a><span data-ttu-id="96dfc-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="96dfc-102">ConnectModeEnum</span></span>

<span data-ttu-id="96dfc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96dfc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96dfc-104">Especifica los permisos disponibles para modificar datos en un objeto [Connection](connection-object-ado.md), abrir un [Record](record-object-ado.md) o especificar los valores de la propiedad [Mode](mode-property-ado.md) de los objetos **Record** y [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="96dfc-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96dfc-105">Constante</span><span class="sxs-lookup"><span data-stu-id="96dfc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="96dfc-106">Valor</span><span class="sxs-lookup"><span data-stu-id="96dfc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="96dfc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="96dfc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-108"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-109">1</span><span class="sxs-lookup"><span data-stu-id="96dfc-109">1</span></span></p></td>
<td><p><span data-ttu-id="96dfc-110">Indica permisos de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="96dfc-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-112">3</span><span class="sxs-lookup"><span data-stu-id="96dfc-112">3</span></span></p></td>
<td><p><span data-ttu-id="96dfc-113">Indica permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="96dfc-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-115">0 x 400000</span><span class="sxs-lookup"><span data-stu-id="96dfc-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="96dfc-116">Se usa junto con los otros valores de <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>o <strong>adModeShareDenyRead</strong>) para propagar restricciones de uso compartidas a todos los registros secundarios del actual <strong>registro</strong>.</span><span class="sxs-lookup"><span data-stu-id="96dfc-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="96dfc-117">No tiene ningún efecto si el <strong>registro</strong> no tiene todos los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="96dfc-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="96dfc-118">Se genera un error en tiempo de ejecución si se utiliza sólo con <strong>adModeShareDenyNone</strong> .</span><span class="sxs-lookup"><span data-stu-id="96dfc-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="96dfc-119">Sin embargo, se puede usar con <strong>adModeShareDenyNone</strong> cuando se combina con otros valores.</span><span class="sxs-lookup"><span data-stu-id="96dfc-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="96dfc-120">Por ejemplo, puede usar &quot; <strong>adModeUnknown</strong> o <strong>adModeShareDenyNone</strong> o <strong>adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="96dfc-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-122">16</span><span class="sxs-lookup"><span data-stu-id="96dfc-122">16</span></span></p></td>
<td><p><span data-ttu-id="96dfc-p103">Permite a otros usuarios abrir una conexión con cualquier permiso. No se les puede denegar el acceso de lectura ni el de escritura.</span><span class="sxs-lookup"><span data-stu-id="96dfc-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-126">4</span><span class="sxs-lookup"><span data-stu-id="96dfc-126">4</span></span></p></td>
<td><p><span data-ttu-id="96dfc-127">Impide a otros usuarios abrir una conexión con permisos de lectura.</span><span class="sxs-lookup"><span data-stu-id="96dfc-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-129">8</span><span class="sxs-lookup"><span data-stu-id="96dfc-129">8</span></span></p></td>
<td><p><span data-ttu-id="96dfc-130">Impide a otros usuarios abrir una conexión con permisos de escritura.</span><span class="sxs-lookup"><span data-stu-id="96dfc-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-132">12</span><span class="sxs-lookup"><span data-stu-id="96dfc-132">12</span></span></p></td>
<td><p><span data-ttu-id="96dfc-133">Impide a otros usuarios abrir una conexión.</span><span class="sxs-lookup"><span data-stu-id="96dfc-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-135">0</span><span class="sxs-lookup"><span data-stu-id="96dfc-135">0</span></span></p></td>
<td><p><span data-ttu-id="96dfc-p104">Valor predeterminado. Indica que aún no se han establecido los permisos o que no se pueden determinar.</span><span class="sxs-lookup"><span data-stu-id="96dfc-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="96dfc-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="96dfc-139">2</span><span class="sxs-lookup"><span data-stu-id="96dfc-139">2</span></span></p></td>
<td><p><span data-ttu-id="96dfc-140">Indica permisos de sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="96dfc-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="96dfc-141">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="96dfc-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="96dfc-142">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="96dfc-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96dfc-143">Constante</span><span class="sxs-lookup"><span data-stu-id="96dfc-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="96dfc-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="96dfc-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-146">(No existe el equivalente de AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="96dfc-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="96dfc-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="96dfc-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="96dfc-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="96dfc-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96dfc-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="96dfc-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96dfc-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="96dfc-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

