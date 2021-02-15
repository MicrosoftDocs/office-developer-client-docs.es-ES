---
title: Enumeración QueryDefStateEnum (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303321"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="16435-102">Enumeración QueryDefStateEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="16435-102">QueryDefStateEnum enumeration (DAO)</span></span>


<span data-ttu-id="16435-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16435-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16435-104">Se utiliza con la propiedad **Prepare** para determinar el método utilizado para especificar cómo se debe preparar una consulta.</span><span class="sxs-lookup"><span data-stu-id="16435-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16435-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="16435-105">Name</span></span></p></th>
<th><p><span data-ttu-id="16435-106">Valor</span><span class="sxs-lookup"><span data-stu-id="16435-106">Value</span></span></p></th>
<th><p><span data-ttu-id="16435-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="16435-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16435-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="16435-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="16435-109">1 </span><span class="sxs-lookup"><span data-stu-id="16435-109">1</span></span></p></td>
<td><p><span data-ttu-id="16435-110">(Valor predeterminado) La instrucción es preparada (es decir, se llama a la API de ODBC de SQLPrepare).</span><span class="sxs-lookup"><span data-stu-id="16435-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16435-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="16435-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="16435-112">2 </span><span class="sxs-lookup"><span data-stu-id="16435-112">2</span></span></p></td>
<td><p><span data-ttu-id="16435-113">La instrucción no es preparada (es decir, se llama a la API de ODBC de SQLExecDirect).</span><span class="sxs-lookup"><span data-stu-id="16435-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

