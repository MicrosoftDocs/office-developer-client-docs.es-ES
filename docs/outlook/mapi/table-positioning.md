---
title: Posicionamiento de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 656f696c58e9b62e7e601d7f531870b8c385e862
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418592"
---
# <a name="table-positioning"></a><span data-ttu-id="8f954-103">Posicionamiento de tabla</span><span class="sxs-lookup"><span data-stu-id="8f954-103">Table Positioning</span></span>

  
  
<span data-ttu-id="8f954-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f954-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f954-105">La posición actual dentro de una tabla siempre se indica mediante un cursor.</span><span class="sxs-lookup"><span data-stu-id="8f954-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="8f954-106">Hay un cursor para cada vista de una tabla; el implementador de la tabla establece su valor.</span><span class="sxs-lookup"><span data-stu-id="8f954-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="8f954-107">Cuando un cliente o proveedor de servicios que usa la tabla realiza una llamada para cambiar la posición de la tabla, se restablece el valor del cursor.</span><span class="sxs-lookup"><span data-stu-id="8f954-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="8f954-108">La posición de una tabla se puede cambiar con:</span><span class="sxs-lookup"><span data-stu-id="8f954-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="8f954-109">Un marcador.</span><span class="sxs-lookup"><span data-stu-id="8f954-109">A bookmark.</span></span>
    
- <span data-ttu-id="8f954-110">Un valor fraccionario.</span><span class="sxs-lookup"><span data-stu-id="8f954-110">A fractional value.</span></span>
    
- <span data-ttu-id="8f954-111">Un filtro.</span><span class="sxs-lookup"><span data-stu-id="8f954-111">A filter.</span></span>
    

