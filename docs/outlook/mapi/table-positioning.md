---
title: Posición de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f7b2baa8cd78fbb8ace72fd0edb7c77f4c02a4c8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583865"
---
# <a name="table-positioning"></a><span data-ttu-id="bfb7e-103">Posición de tabla</span><span class="sxs-lookup"><span data-stu-id="bfb7e-103">Table Positioning</span></span>

  
  
<span data-ttu-id="bfb7e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfb7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfb7e-105">La posición actual dentro de una tabla siempre se indica mediante un cursor.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="bfb7e-106">Hay un cursor para cada vista de una tabla; su valor se establece por implementador de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="bfb7e-107">Cuando un proveedor de servicio o de cliente con la tabla, realiza una llamada para cambiar la posición de la tabla, se restablece el valor del cursor.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="bfb7e-108">Puede cambiar la posición de una tabla con:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="bfb7e-109">Un marcador.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-109">A bookmark.</span></span>
    
- <span data-ttu-id="bfb7e-110">Un valor fraccionario.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-110">A fractional value.</span></span>
    
- <span data-ttu-id="bfb7e-111">Un filtro.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-111">A filter.</span></span>
    

