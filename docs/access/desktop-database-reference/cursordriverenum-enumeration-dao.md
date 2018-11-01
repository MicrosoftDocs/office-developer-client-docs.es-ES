---
title: CursorDriverEnum Enumeration (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d264c1e91982231e025f17c00db79e47a1d5c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880743"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="6df59-102">CursorDriverEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="6df59-102">CursorDriverEnum Enumeration (DAO)</span></span>


<span data-ttu-id="6df59-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6df59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6df59-104">Especifica el tipo de controlador de cursor.</span><span class="sxs-lookup"><span data-stu-id="6df59-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6df59-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="6df59-105">Name</span></span></p></th>
<th><p><span data-ttu-id="6df59-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6df59-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6df59-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6df59-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6df59-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="6df59-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="6df59-109">3</span><span class="sxs-lookup"><span data-stu-id="6df59-109">3</span></span></p></td>
<td><p><span data-ttu-id="6df59-p101">Utiliza siempre la biblioteca de cursores de FoxPro. Esta opción es necesaria para realizar actualizaciones por lotes.</span><span class="sxs-lookup"><span data-stu-id="6df59-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df59-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="6df59-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="6df59-113">-1</span><span class="sxs-lookup"><span data-stu-id="6df59-113">-1</span></span></p></td>
<td><p><span data-ttu-id="6df59-114">(Valor predeterminado) Utiliza cursores de servidor si este los admite; en caso contrario, utiliza la biblioteca de cursores de ODBC.</span><span class="sxs-lookup"><span data-stu-id="6df59-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df59-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="6df59-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="6df59-116">4</span><span class="sxs-lookup"><span data-stu-id="6df59-116">4</span></span></p></td>
<td><p><span data-ttu-id="6df59-117">Abre todos los cursores (es decir, objetos <strong>Recordset</strong> ) como tipo de sólo avance, sólo lectura, con un tamaño de conjunto de filas de la 1.</span><span class="sxs-lookup"><span data-stu-id="6df59-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="6df59-118">También conocido como &quot;consultas sin cursor.&quot;</span><span class="sxs-lookup"><span data-stu-id="6df59-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df59-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="6df59-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="6df59-120">1</span><span class="sxs-lookup"><span data-stu-id="6df59-120">1</span></span></p></td>
<td><p><span data-ttu-id="6df59-p103">Utiliza siempre la biblioteca de cursores de ODBC. Esta opción proporciona mejor rendimiento para conjuntos de resultados pequeños, pero el rendimiento disminuye rápidamente en el caso de conjuntos de resultados más grandes.</span><span class="sxs-lookup"><span data-stu-id="6df59-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df59-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="6df59-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="6df59-124">2</span><span class="sxs-lookup"><span data-stu-id="6df59-124">2</span></span></p></td>
<td><p><span data-ttu-id="6df59-p104">Utiliza siempre cursores de servidor. En la mayoría de las operaciones grandes, esta opción proporciona mejor rendimiento, pero puede dar lugar a un tráfico de red más intenso.</span><span class="sxs-lookup"><span data-stu-id="6df59-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

