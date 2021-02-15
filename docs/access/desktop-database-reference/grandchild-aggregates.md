---
title: Agregados descendientes del secundario
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292149"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="61273-102">Agregados descendientes del secundario</span><span class="sxs-lookup"><span data-stu-id="61273-102">Grandchild aggregates</span></span>


<span data-ttu-id="61273-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61273-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61273-p101">A la columna de capítulo creada en una cláusula de un comando Shape se le puede asignar un *nombre de alias de capítulo* (normalmente con la palabra clave AS). Se puede identificar cualquier columna de cualquier capítulo del objeto **Recordset** con forma mediante un nombre completo que identifica al elemento secundario que contiene la columna. Por ejemplo, si el capítulo principal, cap1, contiene un capítulo secundario, cap2, que tiene una columna de cantidad, cant, el nombre completo sería cap1.cap2.cant. El nombre completo se puede usar como argumento de una de las funciones de agregado (SUMA, MEDIA, MÁX, MÍN, CONTAR, DESVEST o ANY).</span><span class="sxs-lookup"><span data-stu-id="61273-p101">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword). You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

