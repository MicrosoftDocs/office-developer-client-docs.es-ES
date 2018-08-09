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
ms.openlocfilehash: 40533470681182719f5009b048e3b173b92ef290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816498"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="43b9e-103">Llamar a QueryRows para tablas pequeñas</span><span class="sxs-lookup"><span data-stu-id="43b9e-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="43b9e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43b9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43b9e-105">Al recuperar filas de una tabla pequeña, llame a [IMAPITable:: QueryRows](imapitable-queryrows.md) en lugar de crear primero una restricción.</span><span class="sxs-lookup"><span data-stu-id="43b9e-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="43b9e-106">Creación de una restricción afecta al rendimiento debido a que el proveedor debe crear primero una tabla, busque las filas coincidentes en la tabla original y, a continuación, copie las filas a la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="43b9e-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="43b9e-107">Si el número total de filas de la tabla es menor que 100, es probablemente más eficaces leer todas las filas y, a continuación, llame al [elemento IMAPITable:: FindRow](imapitable-findrow.md) para buscar la fila apropiada.</span><span class="sxs-lookup"><span data-stu-id="43b9e-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="43b9e-108">Ésta es una estrategia especialmente buena si esta información es necesaria sólo ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="43b9e-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="43b9e-109">El momento apropiado para usar una restricción es cuando la información restringida o filtrada se utiliza durante un período de tiempo más largo o se usa con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="43b9e-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="43b9e-110">Por ejemplo, si necesita siempre una vista con mensajes no leídos, la llamada correcta a usar es una restricción.</span><span class="sxs-lookup"><span data-stu-id="43b9e-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

