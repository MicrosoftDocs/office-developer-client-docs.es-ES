---
title: Propiedad Database.Version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611fed16c9020b0a6499427af0788bf9ff050c28
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936563"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="246fc-102">Propiedad Database.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="246fc-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="246fc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="246fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="246fc-p101">En un área de trabajo de Microsoft Access, devuelve la versión del motor de base de datos de Microsoft Jet o Microsoft Access que creó la base de datos. **String** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="246fc-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="246fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="246fc-106">Syntax</span></span>

<span data-ttu-id="246fc-107">*expresión* . Versión</span><span class="sxs-lookup"><span data-stu-id="246fc-107">*expression* .Version</span></span>

<span data-ttu-id="246fc-108">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="246fc-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="246fc-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="246fc-109">Remarks</span></span>

<span data-ttu-id="246fc-110">El valor devuelto es un valor de tipo String que da como resultado un número de versión, con el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="246fc-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="246fc-p102">El área de trabajo de Microsoft Access representa el número de versión en la forma "*principal.secundario*". Por ejemplo, "3.0". El número de versión del producto consta del número de versión (3), un punto y el número de publicación (0).</span><span class="sxs-lookup"><span data-stu-id="246fc-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="246fc-114">En la tabla siguiente se muestra la versión del motor de base de datos que se incluye en diversas versiones de productos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="246fc-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="246fc-115">Motor de base de datos</span><span class="sxs-lookup"><span data-stu-id="246fc-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="246fc-116">Versión (año de publicación)</span><span class="sxs-lookup"><span data-stu-id="246fc-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="246fc-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="246fc-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="246fc-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="246fc-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="246fc-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="246fc-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="246fc-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="246fc-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="246fc-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="246fc-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="246fc-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="246fc-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="246fc-123">1.0</span><span class="sxs-lookup"><span data-stu-id="246fc-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="246fc-124">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="246fc-125">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="246fc-126">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246fc-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="246fc-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="246fc-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="246fc-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="246fc-129">1.1</span><span class="sxs-lookup"><span data-stu-id="246fc-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="246fc-130">3.0</span><span class="sxs-lookup"><span data-stu-id="246fc-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="246fc-131">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="246fc-132">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246fc-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="246fc-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="246fc-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="246fc-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="246fc-135">2.0</span><span class="sxs-lookup"><span data-stu-id="246fc-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="246fc-136">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="246fc-137">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="246fc-138">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246fc-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="246fc-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="246fc-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="246fc-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="246fc-141">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="246fc-142">4.0 (16 bits)</span><span class="sxs-lookup"><span data-stu-id="246fc-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="246fc-143">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="246fc-144">N/D</span><span class="sxs-lookup"><span data-stu-id="246fc-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246fc-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="246fc-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="246fc-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="246fc-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="246fc-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="246fc-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="246fc-148">4.0 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="246fc-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="246fc-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="246fc-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="246fc-150">4.x</span><span class="sxs-lookup"><span data-stu-id="246fc-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246fc-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="246fc-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="246fc-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="246fc-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="246fc-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="246fc-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="246fc-154">5.0</span><span class="sxs-lookup"><span data-stu-id="246fc-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="246fc-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="246fc-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="246fc-156">5.0</span><span class="sxs-lookup"><span data-stu-id="246fc-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246fc-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="246fc-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="246fc-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="246fc-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="246fc-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="246fc-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="246fc-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="246fc-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246fc-161">Motor de base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="246fc-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="246fc-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="246fc-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="246fc-163">2007</span><span class="sxs-lookup"><span data-stu-id="246fc-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

