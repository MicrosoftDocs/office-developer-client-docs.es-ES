---
title: Bloque de datos ParaCadaRegistro
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd16b91bb3d6ca0d206be0a63bb73e6f9176da8e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921029"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="a9c47-102">Bloque de datos ParaCadaRegistro</span><span class="sxs-lookup"><span data-stu-id="a9c47-102">ForEachRecord data block</span></span>


<span data-ttu-id="a9c47-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9c47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9c47-104">Un bloque de datos **ParaCadaRegistro** repite un conjunto de instrucciones para cada registro en un dominio.</span><span class="sxs-lookup"><span data-stu-id="a9c47-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a9c47-105">[!NOTA] El bloque de datos <STRONG>ParaCadaRegistro</STRONG> solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="a9c47-105">The <STRONG>ForEachRecord</STRONG> data block is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="a9c47-106">Valores</span><span class="sxs-lookup"><span data-stu-id="a9c47-106">Setting</span></span>

<span data-ttu-id="a9c47-107">La acción **ParaCadaRegistro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a9c47-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9c47-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="a9c47-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="a9c47-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a9c47-109">Required</span></span></p></th>
<th><p><span data-ttu-id="a9c47-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9c47-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9c47-111"><strong>En </strong></span><span class="sxs-lookup"><span data-stu-id="a9c47-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="a9c47-112">Sí</span><span class="sxs-lookup"><span data-stu-id="a9c47-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="a9c47-113">Una cadena que identifica el dominio de registros que se va a funcionar en.</span><span class="sxs-lookup"><span data-stu-id="a9c47-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="a9c47-114">El argumento <em>en</em> puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="a9c47-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="a9c47-115">El dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC .</span><span class="sxs-lookup"><span data-stu-id="a9c47-115">The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9c47-116"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="a9c47-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="a9c47-117">No</span><span class="sxs-lookup"><span data-stu-id="a9c47-117">No</span></span></p></td>
<td><p><span data-ttu-id="a9c47-118">Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos <strong>ParaCadaRegistro</strong> se lleva a cabo.</span><span class="sxs-lookup"><span data-stu-id="a9c47-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="a9c47-119">Por ejemplo, criterios con frecuencia es equivalente a la cláusula WHERE en una expresión SQL, sin la palabra donde.</span><span class="sxs-lookup"><span data-stu-id="a9c47-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="a9c47-120">Si se omite criterios, el bloque de datos <strong>ParaCadaRegistro</strong> funciona en todo el dominio especificado por el argumento <em>en</em> .</span><span class="sxs-lookup"><span data-stu-id="a9c47-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="a9c47-121">Cualquier campo que se incluya en criterios debe ser también un campo de <em>en</em>.</span><span class="sxs-lookup"><span data-stu-id="a9c47-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9c47-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="a9c47-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="a9c47-123">No</span><span class="sxs-lookup"><span data-stu-id="a9c47-123">No</span></span></p></td>
<td><p><span data-ttu-id="a9c47-124">Una cadena que proporciona un nombre alternativo para el dominio especificado por el argumento <em>en</em> .</span><span class="sxs-lookup"><span data-stu-id="a9c47-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="a9c47-125">A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas. Si no se especifica el <em>Alias</em> , se usará el nombre de la tabla o consulta como el alias.</span><span class="sxs-lookup"><span data-stu-id="a9c47-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a9c47-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9c47-126">Remarks</span></span>

<span data-ttu-id="a9c47-127">Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.</span><span class="sxs-lookup"><span data-stu-id="a9c47-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

