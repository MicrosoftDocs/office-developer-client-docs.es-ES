---
title: CursorDriverEnum (enumeración) (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295250"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="52c29-102">CursorDriverEnum (enumeración) (DAO)</span><span class="sxs-lookup"><span data-stu-id="52c29-102">CursorDriverEnum enumeration (DAO)</span></span>

<span data-ttu-id="52c29-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52c29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52c29-104">Especifica el tipo de controlador de cursor.</span><span class="sxs-lookup"><span data-stu-id="52c29-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52c29-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="52c29-105">Name</span></span></p></th>
<th><p><span data-ttu-id="52c29-106">Valor</span><span class="sxs-lookup"><span data-stu-id="52c29-106">Value</span></span></p></th>
<th><p><span data-ttu-id="52c29-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="52c29-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52c29-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="52c29-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="52c29-109">3 </span><span class="sxs-lookup"><span data-stu-id="52c29-109">3</span></span></p></td>
<td><p><span data-ttu-id="52c29-p101">Utiliza siempre la biblioteca de cursores de FoxPro. Esta opción es necesaria para realizar actualizaciones por lotes.</span><span class="sxs-lookup"><span data-stu-id="52c29-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c29-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="52c29-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="52c29-113">-1</span><span class="sxs-lookup"><span data-stu-id="52c29-113">-1</span></span></p></td>
<td><p><span data-ttu-id="52c29-114">(Valor predeterminado) Utiliza cursores de servidor si este los admite; en caso contrario, utiliza la biblioteca de cursores de ODBC.</span><span class="sxs-lookup"><span data-stu-id="52c29-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c29-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="52c29-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="52c29-116">4 </span><span class="sxs-lookup"><span data-stu-id="52c29-116">4</span></span></p></td>
<td><p><span data-ttu-id="52c29-117">Abre todos los cursores (es decir, objetos <strong>Recordset</strong>) como cursores de sólo avance, solo lectura, siendo el tamaño del conjunto de filas igual a 1.</span><span class="sxs-lookup"><span data-stu-id="52c29-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="52c29-118">También se conoce como &quot; consultas sin cursor.&quot;</span><span class="sxs-lookup"><span data-stu-id="52c29-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c29-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="52c29-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="52c29-120">1 </span><span class="sxs-lookup"><span data-stu-id="52c29-120">1</span></span></p></td>
<td><p><span data-ttu-id="52c29-p103">Utiliza siempre la biblioteca de cursores de ODBC. Esta opción proporciona mejor rendimiento para conjuntos de resultados pequeños, pero el rendimiento disminuye rápidamente en el caso de conjuntos de resultados más grandes.</span><span class="sxs-lookup"><span data-stu-id="52c29-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c29-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="52c29-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="52c29-124">2 </span><span class="sxs-lookup"><span data-stu-id="52c29-124">2</span></span></p></td>
<td><p><span data-ttu-id="52c29-p104">Utiliza siempre cursores de servidor. En la mayoría de las operaciones grandes, esta opción proporciona mejor rendimiento, pero puede dar lugar a un tráfico de red más intenso.</span><span class="sxs-lookup"><span data-stu-id="52c29-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

