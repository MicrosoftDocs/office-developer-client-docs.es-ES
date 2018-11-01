---
title: Tipos de datos equivalentes de ANSI SQL
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cac58601277079f6843df6ac9ac7bcae7824b18a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869529"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="05c6c-102">Tipos de datos equivalentes de ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="05c6c-102">Equivalent ANSI SQL Data Types</span></span>


<span data-ttu-id="05c6c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05c6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05c6c-p101">En la siguiente tabla se incluyen los tipos de datos ANSI SQL, los tipos de datos SQL equivalentes del motor de base de datos de Microsoft Access y sus sinónimos válidos. También se incluyen los tipos de datos equivalentes de Microsoft® SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05c6c-p101">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms. It also lists the equivalent Microsoft® SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05c6c-106">Tipo de datos de ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="05c6c-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="05c6c-107">Tipo de datos de Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="05c6c-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="05c6c-108">
Sinónimo</span><span class="sxs-lookup"><span data-stu-id="05c6c-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="05c6c-109">Tipo de datos de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="05c6c-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="05c6c-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="05c6c-111">BINARY (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-112">VARBINARY, BINARIO DEBIDO A DISTINTOS DEBIDO A DISTINTOS BITS</span><span class="sxs-lookup"><span data-stu-id="05c6c-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="05c6c-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="05c6c-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="05c6c-115">BIT (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="05c6c-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="05c6c-117">BIT</span><span class="sxs-lookup"><span data-stu-id="05c6c-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="05c6c-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="05c6c-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="05c6c-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="05c6c-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="05c6c-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="05c6c-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="05c6c-123">COUNTER (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="05c6c-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="05c6c-125">(vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-126">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="05c6c-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="05c6c-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="05c6c-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="05c6c-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="05c6c-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="05c6c-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="05c6c-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="05c6c-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="05c6c-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="05c6c-132">DATE, TIME (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="05c6c-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-134">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="05c6c-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="05c6c-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="05c6c-136">GUID</span><span class="sxs-lookup"><span data-stu-id="05c6c-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="05c6c-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="05c6c-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="05c6c-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="05c6c-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="05c6c-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="05c6c-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="05c6c-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="05c6c-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="05c6c-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-142">REAL</span><span class="sxs-lookup"><span data-stu-id="05c6c-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="05c6c-143">REAL</span><span class="sxs-lookup"><span data-stu-id="05c6c-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="05c6c-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="05c6c-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="05c6c-145">REAL</span><span class="sxs-lookup"><span data-stu-id="05c6c-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="05c6c-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="05c6c-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="05c6c-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="05c6c-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="05c6c-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="05c6c-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="05c6c-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="05c6c-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="05c6c-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="05c6c-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="05c6c-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="05c6c-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="05c6c-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="05c6c-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="05c6c-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="05c6c-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="05c6c-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="05c6c-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="05c6c-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="05c6c-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="05c6c-159">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="05c6c-160">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-161">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="05c6c-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="05c6c-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="05c6c-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="05c6c-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="05c6c-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="05c6c-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05c6c-165">No admitido</span><span class="sxs-lookup"><span data-stu-id="05c6c-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="05c6c-166">TEXTO (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="05c6c-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05c6c-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="05c6c-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="05c6c-170">CHAR (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="05c6c-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="05c6c-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="05c6c-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="05c6c-p102">El tipo de datos BIT de ANSI SQL no se corresponde con el tipo de datos BIT de Microsoft Access SQL. En su lugar, se corresponde con el tipo de datos BINARY. No hay equivalente en ANSI SQL para el tipo de datos BIT de Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="05c6c-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="05c6c-176">TIMESTAMP ya no se admite como sinónimo de DATETIME.</span><span class="sxs-lookup"><span data-stu-id="05c6c-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="05c6c-p103">NUMERIC ya no se admite como sinónimo de FLOAT o DOUBLE. Ahora, NUMERIC se usa como sinónimo de DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="05c6c-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="05c6c-179">Los campos LONGTEXT siempre se almacenan en el formato de representación Unicode.</span><span class="sxs-lookup"><span data-stu-id="05c6c-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="05c6c-p104">Si se usa el nombre de tipo de datos TEXT sin especificar la longitud opcional, por ejemplo TEXT(25), se crea un campo LONGTEXT. Esto permite escribir [instrucciones CREATE TABLE](create-table-statement-microsoft-access-sql.md) que produzcan tipos de datos coherentes con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05c6c-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="05c6c-182">Los campos CHAR siempre se almacenan en el formato de representación Unicode, que es el equivalente del tipo de datos NATIONAL CHAR de ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="05c6c-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="05c6c-p105">Si se usa el nombre de tipo de datos TEXT y se especifica la longitud opcional, por ejemplo TEXT(25), el tipo de datos del campo es equivalente al tipo de datos CHAR. Esto conserva la compatibilidad con versiones anteriores para la mayoría de las aplicaciones de Microsoft Jet a la vez que permite conciliar el tipo de datos TEXT (sin especificar la longitud) con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05c6c-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


