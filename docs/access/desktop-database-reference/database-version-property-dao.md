---
title: Database.Version Property (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ce28decf2d20c608067a2fa3791d8dce0ce61f8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876270"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="2e2e6-102">Database.Version Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-102">Database.Version Property (DAO)</span></span>


<span data-ttu-id="2e2e6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e2e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e2e6-p101">En un área de trabajo de Microsoft Access, devuelve la versión del motor de base de datos de Microsoft Jet o Microsoft Access que creó la base de datos. **String** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2e2e6-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2e6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e2e6-106">Syntax</span></span>

<span data-ttu-id="2e2e6-107">*expresión* . Versión</span><span class="sxs-lookup"><span data-stu-id="2e2e6-107">*expression* .Version</span></span>

<span data-ttu-id="2e2e6-108">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="2e2e6-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2e6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e2e6-109">Remarks</span></span>

<span data-ttu-id="2e2e6-110">El valor devuelto es un valor de tipo String que da como resultado un número de versión, con el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="2e2e6-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

  - <span data-ttu-id="2e2e6-p102">El área de trabajo de Microsoft Access representa el número de versión en la forma "*principal.secundario*". Por ejemplo, "3.0". El número de versión del producto consta del número de versión (3), un punto y el número de publicación (0).</span><span class="sxs-lookup"><span data-stu-id="2e2e6-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="2e2e6-114">En la tabla siguiente se muestra la versión del motor de base de datos que se incluye en diversas versiones de productos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2e2e6-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

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
<th><p><span data-ttu-id="2e2e6-115">Motor de base de datos</span><span class="sxs-lookup"><span data-stu-id="2e2e6-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="2e2e6-116">Versión (año de publicación)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="2e2e6-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="2e2e6-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="2e2e6-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2e2e6-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="2e2e6-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="2e2e6-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="2e2e6-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="2e2e6-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e2e6-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2e2e6-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-123">1.0</span><span class="sxs-lookup"><span data-stu-id="2e2e6-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-124">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-125">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-126">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e2e6-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2e2e6-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-129">1.1</span><span class="sxs-lookup"><span data-stu-id="2e2e6-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-130">3.0</span><span class="sxs-lookup"><span data-stu-id="2e2e6-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-131">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-132">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e2e6-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2e2e6-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-135">2.0</span><span class="sxs-lookup"><span data-stu-id="2e2e6-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-136">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-137">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-138">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e2e6-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2e2e6-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-141">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-142">4.0 (16 bits)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-143">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-144">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2e6-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e2e6-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2e2e6-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-148">4.0 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-150">4.x</span><span class="sxs-lookup"><span data-stu-id="2e2e6-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e2e6-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2e2e6-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-154">5.0</span><span class="sxs-lookup"><span data-stu-id="2e2e6-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-156">5.0</span><span class="sxs-lookup"><span data-stu-id="2e2e6-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e2e6-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2e2e6-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2e2e6-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e2e6-161">Motor de base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="2e2e6-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="2e2e6-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="2e2e6-163">2007</span><span class="sxs-lookup"><span data-stu-id="2e2e6-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

