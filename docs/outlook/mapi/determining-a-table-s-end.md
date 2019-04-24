---
title: Determinar el final de una tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316719"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="a274d-103">Determinar el final de una tabla</span><span class="sxs-lookup"><span data-stu-id="a274d-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="a274d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a274d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a274d-105">Un error común es suponer que se ha alcanzado el final de la tabla cuando:</span><span class="sxs-lookup"><span data-stu-id="a274d-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="a274d-106">Se ha llamado al método [IMAPITable:: QueryRows](imapitable-queryrows.md) en un bucle, con el final del bucle determinado por el recuento de filas devuelto por [IMAPITable:: GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="a274d-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="a274d-107">El recuento que devuelve **GetRowCount** no siempre representa el número exacto de filas en la tabla; es un recuento aproximado.</span><span class="sxs-lookup"><span data-stu-id="a274d-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="a274d-108">Se ha llamado a **QueryRows** con un número fijo de filas y se devuelven menos filas.</span><span class="sxs-lookup"><span data-stu-id="a274d-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="a274d-109">No es hasta que **QueryRows** devuelve un conjunto de filas con un recuento de filas igual a cero que no hay más filas que recuperar.</span><span class="sxs-lookup"><span data-stu-id="a274d-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="a274d-110">La única vez que una persona que llama puede suponer que el cursor está situado al final de la tabla para un recuento de filas positivo o al principio de la tabla para un recuento de filas negativo cuando se devuelven las filas de valor S_OK y cero.</span><span class="sxs-lookup"><span data-stu-id="a274d-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="a274d-111">El valor MAPI_E_NOT_FOUND no se devuelve nunca.</span><span class="sxs-lookup"><span data-stu-id="a274d-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a274d-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="a274d-112">See also</span></span>



[<span data-ttu-id="a274d-113">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="a274d-113">MAPI Tables</span></span>](mapi-tables.md)

