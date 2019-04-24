---
title: Establecer la posición de la tabla con un valor fraccionario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339266"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="cf274-103">Establecer la posición de la tabla con un valor fraccionario</span><span class="sxs-lookup"><span data-stu-id="cf274-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="cf274-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf274-105">Table los usuarios pueden desplazarse a una posición que representa un porcentaje aproximado de filas en relación con el total.</span><span class="sxs-lookup"><span data-stu-id="cf274-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="cf274-106">En lugar de desplazarse a una fila exacta, este método de colocación divide la tabla en partes basadas en fracciones.</span><span class="sxs-lookup"><span data-stu-id="cf274-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="cf274-107">Tabla los usuarios pueden mover, por ejemplo, al punto de medio camino de una tabla o a la fila que se encuentra en el 7/8 del recorrido de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cf274-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="cf274-108">**Para mover el cursor un número aproximado de filas**</span><span class="sxs-lookup"><span data-stu-id="cf274-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="cf274-109">Llame al [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="cf274-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="cf274-110">**SeekRowApprox** se desplaza a la fila que representa un porcentaje en particular de las filas en relación con el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cf274-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="cf274-111">Este porcentaje se especifica en los parámetros _ulNumerator_ y _ulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="cf274-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="cf274-112">**SeekRowApprox** se usa con frecuencia para implementar barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="cf274-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="cf274-113">**Para determinar la posición aproximada de una tabla**</span><span class="sxs-lookup"><span data-stu-id="cf274-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="cf274-114">Llame al [IMAPITable:: QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="cf274-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="cf274-115">**QueryPosition** puede usarse para informar al usuario de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="cf274-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="cf274-116">Establece un valor fraccionario basado en el número de filas de la tabla y en el número de la fila actual.</span><span class="sxs-lookup"><span data-stu-id="cf274-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="cf274-117">Se espera que este valor represente una aproximación.</span><span class="sxs-lookup"><span data-stu-id="cf274-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="cf274-118">Se recomienda a los implementadores de tablas no calcular la posición exacta porque las implementaciones precisas pueden ser costosas de invocar, especialmente en tablas clasificadas.</span><span class="sxs-lookup"><span data-stu-id="cf274-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="cf274-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf274-119">See also</span></span>



[<span data-ttu-id="cf274-120">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="cf274-120">MAPI Tables</span></span>](mapi-tables.md)

