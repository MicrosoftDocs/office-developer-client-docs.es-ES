---
title: Tipos de datos equivalentes de ANSI SQL
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d1a07e3a7565e15fc5689bf73fe066a3529d3234
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946282"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="bba86-102">Tipos de datos equivalentes de ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="bba86-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="bba86-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bba86-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bba86-104">En la siguiente tabla se incluyen los tipos de datos ANSI SQL, los tipos de datos SQL equivalentes del motor de base de datos de Microsoft Access y sus sinónimos válidos.</span><span class="sxs-lookup"><span data-stu-id="bba86-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="bba86-105">También se enumeran los tipos de datos Microsoft SQL Server™ equivalentes.</span><span class="sxs-lookup"><span data-stu-id="bba86-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bba86-106">Tipo de datos de ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="bba86-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="bba86-107">Tipo de datos de Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="bba86-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="bba86-108">
Sinónimo</span><span class="sxs-lookup"><span data-stu-id="bba86-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="bba86-109">Tipo de datos de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="bba86-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bba86-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="bba86-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="bba86-111">BINARY (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-112">VARBINARY, BINARIO DEBIDO A DISTINTOS DEBIDO A DISTINTOS BITS</span><span class="sxs-lookup"><span data-stu-id="bba86-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="bba86-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="bba86-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bba86-115">BIT (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="bba86-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="bba86-117">BIT</span><span class="sxs-lookup"><span data-stu-id="bba86-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba86-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bba86-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="bba86-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="bba86-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="bba86-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="bba86-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="bba86-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bba86-123">COUNTER (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="bba86-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="bba86-125">(vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba86-126">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bba86-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="bba86-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="bba86-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="bba86-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="bba86-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="bba86-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="bba86-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="bba86-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="bba86-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="bba86-132">DATE, TIME (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="bba86-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba86-134">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bba86-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="bba86-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="bba86-136">GUID</span><span class="sxs-lookup"><span data-stu-id="bba86-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="bba86-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="bba86-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="bba86-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="bba86-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="bba86-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="bba86-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="bba86-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="bba86-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="bba86-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba86-142">REAL</span><span class="sxs-lookup"><span data-stu-id="bba86-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="bba86-143">REAL</span><span class="sxs-lookup"><span data-stu-id="bba86-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="bba86-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="bba86-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="bba86-145">REAL</span><span class="sxs-lookup"><span data-stu-id="bba86-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="bba86-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="bba86-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bba86-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="bba86-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bba86-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba86-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="bba86-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="bba86-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="bba86-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="bba86-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="bba86-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="bba86-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="bba86-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="bba86-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="bba86-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="bba86-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="bba86-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="bba86-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="bba86-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="bba86-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba86-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="bba86-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="bba86-159">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bba86-160">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-161">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bba86-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="bba86-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="bba86-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="bba86-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="bba86-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="bba86-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba86-165">No admitido</span><span class="sxs-lookup"><span data-stu-id="bba86-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bba86-166">TEXTO (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="bba86-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba86-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="bba86-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="bba86-170">CHAR (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="bba86-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bba86-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="bba86-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="bba86-p102">El tipo de datos BIT de ANSI SQL no se corresponde con el tipo de datos BIT de Microsoft Access SQL. En su lugar, se corresponde con el tipo de datos BINARY. No hay equivalente en ANSI SQL para el tipo de datos BIT de Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="bba86-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="bba86-176">TIMESTAMP ya no se admite como sinónimo de DATETIME.</span><span class="sxs-lookup"><span data-stu-id="bba86-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="bba86-p103">NUMERIC ya no se admite como sinónimo de FLOAT o DOUBLE. Ahora, NUMERIC se usa como sinónimo de DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="bba86-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="bba86-179">Los campos LONGTEXT siempre se almacenan en el formato de representación Unicode.</span><span class="sxs-lookup"><span data-stu-id="bba86-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="bba86-p104">Si se usa el nombre de tipo de datos TEXT sin especificar la longitud opcional, por ejemplo TEXT(25), se crea un campo LONGTEXT. Esto permite escribir [instrucciones CREATE TABLE](create-table-statement-microsoft-access-sql.md) que produzcan tipos de datos coherentes con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bba86-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="bba86-182">Los campos CHAR siempre se almacenan en el formato de representación Unicode, que es el equivalente del tipo de datos NATIONAL CHAR de ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="bba86-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="bba86-p105">Si se usa el nombre de tipo de datos TEXT y se especifica la longitud opcional, por ejemplo TEXT(25), el tipo de datos del campo es equivalente al tipo de datos CHAR. Esto conserva la compatibilidad con versiones anteriores para la mayoría de las aplicaciones de Microsoft Jet a la vez que permite conciliar el tipo de datos TEXT (sin especificar la longitud) con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bba86-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


