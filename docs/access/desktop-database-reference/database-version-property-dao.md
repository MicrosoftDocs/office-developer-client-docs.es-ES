---
title: Propiedad Database. version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41b408f63522902fd1d4f806090eef7563a3492a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294655"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="47d35-102">Propiedad Database. version (DAO)</span><span class="sxs-lookup"><span data-stu-id="47d35-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="47d35-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47d35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47d35-104">En un área de trabajo de Microsoft Access, devuelve la versión del motor de base de datos de Microsoft Jet o Microsoft Access que creó la base de datos.</span><span class="sxs-lookup"><span data-stu-id="47d35-104">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database.</span></span> <span data-ttu-id="47d35-105">**String** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="47d35-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d35-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47d35-106">Syntax</span></span>

<span data-ttu-id="47d35-107">*expresión* . Versi</span><span class="sxs-lookup"><span data-stu-id="47d35-107">*expression* .Version</span></span>

<span data-ttu-id="47d35-108">*expresión* Variable que representa un objeto **Database** .</span><span class="sxs-lookup"><span data-stu-id="47d35-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d35-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47d35-109">Remarks</span></span>

<span data-ttu-id="47d35-110">El valor devuelto es un valor de tipo String que da como resultado un número de versión, con el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="47d35-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="47d35-p102">El área de trabajo de Microsoft Access representa el número de versión en la forma "*principal.secundario*". Por ejemplo, "3.0". El número de versión del producto consta del número de versión (3), un punto y el número de publicación (0).</span><span class="sxs-lookup"><span data-stu-id="47d35-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="47d35-114">En la tabla siguiente se muestra la versión del motor de base de datos que se incluye en diversas versiones de productos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="47d35-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

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
<th><p><span data-ttu-id="47d35-115">Motor de base de datos</span><span class="sxs-lookup"><span data-stu-id="47d35-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="47d35-116">Versión (año de publicación)</span><span class="sxs-lookup"><span data-stu-id="47d35-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="47d35-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="47d35-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="47d35-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="47d35-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="47d35-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="47d35-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="47d35-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="47d35-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47d35-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="47d35-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="47d35-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="47d35-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="47d35-123">1.0</span><span class="sxs-lookup"><span data-stu-id="47d35-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="47d35-124">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="47d35-125">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="47d35-126">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47d35-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="47d35-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="47d35-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="47d35-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="47d35-129">1.1</span><span class="sxs-lookup"><span data-stu-id="47d35-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="47d35-130">3,0</span><span class="sxs-lookup"><span data-stu-id="47d35-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="47d35-131">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="47d35-132">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47d35-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="47d35-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="47d35-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="47d35-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="47d35-135">2.0</span><span class="sxs-lookup"><span data-stu-id="47d35-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="47d35-136">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="47d35-137">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="47d35-138">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47d35-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="47d35-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="47d35-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="47d35-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="47d35-141">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="47d35-142">4.0 (16 bits)</span><span class="sxs-lookup"><span data-stu-id="47d35-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="47d35-143">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="47d35-144">N/D</span><span class="sxs-lookup"><span data-stu-id="47d35-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47d35-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="47d35-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="47d35-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="47d35-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="47d35-147">‘95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="47d35-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="47d35-148">4.0 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="47d35-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="47d35-149">‘95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="47d35-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="47d35-150">4.x</span><span class="sxs-lookup"><span data-stu-id="47d35-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47d35-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="47d35-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="47d35-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="47d35-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="47d35-153">‘97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="47d35-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="47d35-154">5,0</span><span class="sxs-lookup"><span data-stu-id="47d35-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="47d35-155">‘97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="47d35-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="47d35-156">5,0</span><span class="sxs-lookup"><span data-stu-id="47d35-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47d35-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="47d35-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="47d35-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="47d35-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="47d35-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="47d35-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="47d35-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="47d35-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47d35-161">Motor de base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="47d35-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="47d35-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="47d35-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="47d35-163">2007</span><span class="sxs-lookup"><span data-stu-id="47d35-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

