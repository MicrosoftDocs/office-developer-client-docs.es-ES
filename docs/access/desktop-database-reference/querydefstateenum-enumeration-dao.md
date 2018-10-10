---
title: QueryDefStateEnum Enumeration (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68f6f1e96ae57508d94ea341b36e3a6b32cac660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485399"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="af19f-102">QueryDefStateEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="af19f-102">QueryDefStateEnum Enumeration (DAO)</span></span>


<span data-ttu-id="af19f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="af19f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="af19f-104">Se utiliza con la propiedad **Prepare** para determinar el método utilizado para especificar cómo se debe preparar una consulta.</span><span class="sxs-lookup"><span data-stu-id="af19f-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af19f-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="af19f-105">Name</span></span></p></th>
<th><p><span data-ttu-id="af19f-106">Valor</span><span class="sxs-lookup"><span data-stu-id="af19f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="af19f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="af19f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af19f-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="af19f-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="af19f-109">1</span><span class="sxs-lookup"><span data-stu-id="af19f-109">1</span></span></p></td>
<td><p><span data-ttu-id="af19f-110">(Valor predeterminado) La instrucción es preparada (es decir, se llama a la API de ODBC de SQLPrepare).</span><span class="sxs-lookup"><span data-stu-id="af19f-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af19f-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="af19f-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="af19f-112">2</span><span class="sxs-lookup"><span data-stu-id="af19f-112">2</span></span></p></td>
<td><p><span data-ttu-id="af19f-113">La instrucción no es preparada (es decir, se llama a la API de ODBC de SQLExecDirect).</span><span class="sxs-lookup"><span data-stu-id="af19f-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

