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
ms.openlocfilehash: cec0b3584c6c19abb5f7421f1db0b06c877bb9ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820839"
---
# <a name="table-positioning"></a><span data-ttu-id="c4065-103">Posición de tabla</span><span class="sxs-lookup"><span data-stu-id="c4065-103">Table Positioning</span></span>

  
  
<span data-ttu-id="c4065-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4065-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4065-105">La posición actual dentro de una tabla siempre se indica mediante un cursor.</span><span class="sxs-lookup"><span data-stu-id="c4065-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="c4065-106">Hay un cursor para cada vista de una tabla; su valor se establece por implementador de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c4065-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="c4065-107">Cuando un proveedor de servicio o de cliente con la tabla, realiza una llamada para cambiar la posición de la tabla, se restablece el valor del cursor.</span><span class="sxs-lookup"><span data-stu-id="c4065-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="c4065-108">Puede cambiar la posición de una tabla con:</span><span class="sxs-lookup"><span data-stu-id="c4065-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="c4065-109">Un marcador.</span><span class="sxs-lookup"><span data-stu-id="c4065-109">A bookmark.</span></span>
    
- <span data-ttu-id="c4065-110">Un valor fraccionario.</span><span class="sxs-lookup"><span data-stu-id="c4065-110">A fractional value.</span></span>
    
- <span data-ttu-id="c4065-111">Un filtro.</span><span class="sxs-lookup"><span data-stu-id="c4065-111">A filter.</span></span>
    

