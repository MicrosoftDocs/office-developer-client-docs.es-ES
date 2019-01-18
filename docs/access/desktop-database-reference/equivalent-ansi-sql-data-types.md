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
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699383"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="b37f3-102">Tipos de datos equivalentes de ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="b37f3-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="b37f3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b37f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b37f3-104">En la siguiente tabla se incluyen los tipos de datos ANSI SQL, los tipos de datos SQL equivalentes del motor de base de datos de Microsoft Access y sus sinónimos válidos.</span><span class="sxs-lookup"><span data-stu-id="b37f3-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="b37f3-105">También se enumeran los tipos de datos Microsoft SQL Server™ equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b37f3-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b37f3-106">Tipo de datos de ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="b37f3-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="b37f3-107">Tipo de datos de Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="b37f3-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="b37f3-108">
Sinónimo</span><span class="sxs-lookup"><span data-stu-id="b37f3-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="b37f3-109">Tipo de datos de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="b37f3-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="b37f3-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="b37f3-111">BINARY (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-112">VARBINARY, BINARIO DEBIDO A DISTINTOS DEBIDO A DISTINTOS BITS</span><span class="sxs-lookup"><span data-stu-id="b37f3-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="b37f3-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="b37f3-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b37f3-115">BIT (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="b37f3-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="b37f3-117">BIT</span><span class="sxs-lookup"><span data-stu-id="b37f3-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b37f3-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="b37f3-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="b37f3-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="b37f3-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="b37f3-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="b37f3-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b37f3-123">COUNTER (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="b37f3-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="b37f3-125">(vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-126">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b37f3-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="b37f3-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="b37f3-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b37f3-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="b37f3-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="b37f3-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="b37f3-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="b37f3-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="b37f3-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="b37f3-132">DATE, TIME (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="b37f3-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-134">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b37f3-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="b37f3-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="b37f3-136">GUID</span><span class="sxs-lookup"><span data-stu-id="b37f3-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="b37f3-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="b37f3-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b37f3-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="b37f3-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b37f3-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="b37f3-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="b37f3-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="b37f3-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b37f3-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-142">REAL</span><span class="sxs-lookup"><span data-stu-id="b37f3-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="b37f3-143">REAL</span><span class="sxs-lookup"><span data-stu-id="b37f3-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="b37f3-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="b37f3-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="b37f3-145">REAL</span><span class="sxs-lookup"><span data-stu-id="b37f3-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="b37f3-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="b37f3-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b37f3-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="b37f3-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b37f3-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="b37f3-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="b37f3-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="b37f3-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="b37f3-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="b37f3-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="b37f3-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="b37f3-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="b37f3-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="b37f3-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="b37f3-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="b37f3-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="b37f3-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="b37f3-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="b37f3-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="b37f3-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="b37f3-159">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b37f3-160">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-161">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b37f3-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="b37f3-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="b37f3-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="b37f3-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="b37f3-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="b37f3-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b37f3-165">No admitido</span><span class="sxs-lookup"><span data-stu-id="b37f3-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b37f3-166">TEXTO (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="b37f3-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b37f3-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="b37f3-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="b37f3-170">CHAR (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (vea las notas)</span><span class="sxs-lookup"><span data-stu-id="b37f3-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b37f3-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="b37f3-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="b37f3-p102">El tipo de datos BIT de ANSI SQL no se corresponde con el tipo de datos BIT de Microsoft Access SQL. En su lugar, se corresponde con el tipo de datos BINARY. No hay equivalente en ANSI SQL para el tipo de datos BIT de Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="b37f3-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="b37f3-176">TIMESTAMP ya no se admite como sinónimo de DATETIME.</span><span class="sxs-lookup"><span data-stu-id="b37f3-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="b37f3-p103">NUMERIC ya no se admite como sinónimo de FLOAT o DOUBLE. Ahora, NUMERIC se usa como sinónimo de DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="b37f3-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="b37f3-179">Los campos LONGTEXT siempre se almacenan en el formato de representación Unicode.</span><span class="sxs-lookup"><span data-stu-id="b37f3-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="b37f3-p104">Si se usa el nombre de tipo de datos TEXT sin especificar la longitud opcional, por ejemplo TEXT(25), se crea un campo LONGTEXT. Esto permite escribir [instrucciones CREATE TABLE](create-table-statement-microsoft-access-sql.md) que produzcan tipos de datos coherentes con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b37f3-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="b37f3-182">Los campos CHAR siempre se almacenan en el formato de representación Unicode, que es el equivalente del tipo de datos NATIONAL CHAR de ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="b37f3-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="b37f3-p105">Si se usa el nombre de tipo de datos TEXT y se especifica la longitud opcional, por ejemplo TEXT(25), el tipo de datos del campo es equivalente al tipo de datos CHAR. Esto conserva la compatibilidad con versiones anteriores para la mayoría de las aplicaciones de Microsoft Jet a la vez que permite conciliar el tipo de datos TEXT (sin especificar la longitud) con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b37f3-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


