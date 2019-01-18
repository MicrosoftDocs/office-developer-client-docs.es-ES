---
title: Bloque de datos ParaCadaRegistro
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706348"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="9b74a-102">Bloque de datos ParaCadaRegistro</span><span class="sxs-lookup"><span data-stu-id="9b74a-102">ForEachRecord data block</span></span>

<span data-ttu-id="9b74a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b74a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b74a-104">Un bloque de datos **ParaCadaRegistro** repite un conjunto de instrucciones para cada registro en un dominio.</span><span class="sxs-lookup"><span data-stu-id="9b74a-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="9b74a-105">[!NOTA] El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="9b74a-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="9b74a-106">Valores</span><span class="sxs-lookup"><span data-stu-id="9b74a-106">Setting</span></span>

<span data-ttu-id="9b74a-107">La acción **ParaCadaRegistro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="9b74a-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b74a-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="9b74a-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="9b74a-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9b74a-109">Required</span></span></p></th>
<th><p><span data-ttu-id="9b74a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b74a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b74a-111"><strong>En </strong></span><span class="sxs-lookup"><span data-stu-id="9b74a-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="9b74a-112">Sí</span><span class="sxs-lookup"><span data-stu-id="9b74a-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="9b74a-113">Una cadena que identifica el dominio de registros que se va a funcionar en.</span><span class="sxs-lookup"><span data-stu-id="9b74a-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="9b74a-114">El argumento <em>en</em> puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="9b74a-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="9b74a-115"><strong>Nota</strong>: el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="9b74a-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b74a-116"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="9b74a-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="9b74a-117">No</span><span class="sxs-lookup"><span data-stu-id="9b74a-117">No</span></span></p></td>
<td><p><span data-ttu-id="9b74a-118">Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos <strong>ParaCadaRegistro</strong> se lleva a cabo.</span><span class="sxs-lookup"><span data-stu-id="9b74a-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="9b74a-119">Por ejemplo, criterios con frecuencia es equivalente a la cláusula WHERE en una expresión SQL, sin la palabra donde.</span><span class="sxs-lookup"><span data-stu-id="9b74a-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="9b74a-120">Si se omite criterios, el bloque de datos <strong>ParaCadaRegistro</strong> funciona en todo el dominio especificado por el argumento <em>en</em> .</span><span class="sxs-lookup"><span data-stu-id="9b74a-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="9b74a-121">Cualquier campo que se incluya en criterios debe ser también un campo de <em>en</em>.</span><span class="sxs-lookup"><span data-stu-id="9b74a-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b74a-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="9b74a-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="9b74a-123">No</span><span class="sxs-lookup"><span data-stu-id="9b74a-123">No</span></span></p></td>
<td><p><span data-ttu-id="9b74a-124">Una cadena que proporciona un nombre alternativo para el dominio especificado por el argumento <em>en</em> .</span><span class="sxs-lookup"><span data-stu-id="9b74a-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="9b74a-125">A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas. Si no se especifica el <em>Alias</em> , se usará el nombre de la tabla o consulta como el alias.</span><span class="sxs-lookup"><span data-stu-id="9b74a-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9b74a-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b74a-126">Remarks</span></span>

<span data-ttu-id="9b74a-127">Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.</span><span class="sxs-lookup"><span data-stu-id="9b74a-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

