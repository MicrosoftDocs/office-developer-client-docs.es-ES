---
title: Agregados secundarios
TOCTitle: Grandchild Aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c5ab45412b0524bcef14a952f5c5bbe0953278c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873533"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="ac863-102">Agregados secundarios</span><span class="sxs-lookup"><span data-stu-id="ac863-102">Grandchild Aggregates</span></span>


<span data-ttu-id="ac863-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac863-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac863-104">La columna de capítulo creada en una cláusula de un comando shape se podrá dar un *nombre de alias de capítulo* (normalmente con la palabra clave AS).</span><span class="sxs-lookup"><span data-stu-id="ac863-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="ac863-105">Se puede identificar cualquier columna de cualquier capítulo del **Recordset** con forma con un nombre completo que identifica al elemento secundario que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="ac863-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="ac863-106">Por ejemplo, si el capítulo principal, Cap1, contiene un capítulo secundario, Cap2, tiene una columna de cantidad, importe, a continuación, el nombre completo sería Cap1.Cap2.Cant. A continuación, se puede usar el nombre completo como un argumento a una de las funciones de agregado (SUM, AVG, MAX, MIN, COUNT, STDEV o cualquiera).</span><span class="sxs-lookup"><span data-stu-id="ac863-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

