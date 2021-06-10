---
title: Bloque de datos ForEachRecord
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292331"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="d45f9-102">Bloque de datos ForEachRecord</span><span class="sxs-lookup"><span data-stu-id="d45f9-102">ForEachRecord data block</span></span>

<span data-ttu-id="d45f9-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d45f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d45f9-104">Un **bloque de datos ForEachRecord** repite un conjunto de instrucciones para cada registro de un dominio.</span><span class="sxs-lookup"><span data-stu-id="d45f9-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="d45f9-105">El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="d45f9-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="d45f9-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="d45f9-106">Setting</span></span>

<span data-ttu-id="d45f9-107">La acción **ParaCadaRegistro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d45f9-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d45f9-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="d45f9-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="d45f9-109">Necesario</span><span class="sxs-lookup"><span data-stu-id="d45f9-109">Required</span></span></p></th>
<th><p><span data-ttu-id="d45f9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d45f9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d45f9-111"><strong>In</strong></span><span class="sxs-lookup"><span data-stu-id="d45f9-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="d45f9-112">Sí</span><span class="sxs-lookup"><span data-stu-id="d45f9-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="d45f9-113">Una cadena que identifica el dominio de los registros en los que se operará.</span><span class="sxs-lookup"><span data-stu-id="d45f9-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="d45f9-114">El <em>argumento In</em> puede contener el nombre de la tabla, una consulta select o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="d45f9-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="d45f9-115"><strong>NOTA:</strong>el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="d45f9-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45f9-116"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="d45f9-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="d45f9-117">No</span><span class="sxs-lookup"><span data-stu-id="d45f9-117">No</span></span></p></td>
<td><p><span data-ttu-id="d45f9-118">Expresión de cadena usada para restringir el intervalo de datos en el que se realiza el bloque de datos <strong>ForEachRecord.</strong></span><span class="sxs-lookup"><span data-stu-id="d45f9-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="d45f9-119">Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE.</span><span class="sxs-lookup"><span data-stu-id="d45f9-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="d45f9-120">Si se omite criteria, el bloque de datos <strong>ForEachRecord</strong> funciona en todo el dominio especificado por el <em>argumento In.</em></span><span class="sxs-lookup"><span data-stu-id="d45f9-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="d45f9-121">Cualquier campo que se incluya en los criterios debe ser también un campo del argumento <em>En</em>.</span><span class="sxs-lookup"><span data-stu-id="d45f9-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45f9-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="d45f9-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="d45f9-123">No</span><span class="sxs-lookup"><span data-stu-id="d45f9-123">No</span></span></p></td>
<td><p><span data-ttu-id="d45f9-124">Cadena que proporciona un nombre alternativo para el dominio especificado por el <em>argumento In.</em></span><span class="sxs-lookup"><span data-stu-id="d45f9-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="d45f9-125">A menudo se usa para acortar el nombre de tabla de las referencias posteriores para evitar posibles referencias ambiguas. Si no se especifica <em>Alias,</em> se usará el nombre de la tabla o consulta como alias.</span><span class="sxs-lookup"><span data-stu-id="d45f9-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d45f9-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d45f9-126">Remarks</span></span>

<span data-ttu-id="d45f9-127">Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.</span><span class="sxs-lookup"><span data-stu-id="d45f9-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

