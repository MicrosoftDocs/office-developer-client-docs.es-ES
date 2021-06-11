---
title: Llamar a QueryRows para tablas pequeñas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404179"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="c0e65-103">Llamar a QueryRows para tablas pequeñas</span><span class="sxs-lookup"><span data-stu-id="c0e65-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="c0e65-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0e65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0e65-105">Al recuperar filas de una tabla pequeña, llama a [IMAPITable::QueryRows](imapitable-queryrows.md) en lugar de crear primero una restricción.</span><span class="sxs-lookup"><span data-stu-id="c0e65-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="c0e65-106">Crear una restricción afecta al rendimiento porque el proveedor primero debe crear una tabla, buscar las filas coincidentes en la tabla original y, a continuación, copiar las filas en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="c0e65-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="c0e65-107">Si el número total de filas de la tabla es menor que 100, probablemente sea más eficaz leer todas las filas y, a continuación, llamar a [IMAPITable::FindRow](imapitable-findrow.md) para buscar la fila adecuada.</span><span class="sxs-lookup"><span data-stu-id="c0e65-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="c0e65-108">Esta es una estrategia especialmente buena si esta información solo se necesita ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="c0e65-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="c0e65-109">El tiempo adecuado para usar una restricción es cuando la información restringida o filtrada se usará durante un período de tiempo más largo o se usará con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="c0e65-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="c0e65-110">Por ejemplo, si siempre necesita una vista con mensajes no leídos, entonces una restricción es la llamada adecuada para usar.</span><span class="sxs-lookup"><span data-stu-id="c0e65-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

