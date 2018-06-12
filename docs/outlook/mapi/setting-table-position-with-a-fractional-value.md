---
title: Posición de la tabla de configuración con un valor fraccionario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 104de38a41408091a6fbb69995de4f41f6fea6a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820648"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="8fc5b-103">Posición de la tabla de configuración con un valor fraccionario</span><span class="sxs-lookup"><span data-stu-id="8fc5b-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="8fc5b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fc5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fc5b-105">Los usuarios de la tabla pueden mover a una posición que representa un porcentaje aproximado de filas en relación con el total.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="8fc5b-106">En lugar de mover a una fila exacto, este método de colocación divide la tabla en partes según las fracciones.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="8fc5b-107">Pueden mover los usuarios de la tabla, por ejemplo, en punto de intermedio de una tabla o en la fila que es 7 y 8 de la forma a través de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="8fc5b-108">**Para mover el cursor un número aproximado de filas**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="8fc5b-109">Llamar a [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="8fc5b-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="8fc5b-110">**SeekRowApprox** se mueve a la fila que representa un porcentaje determinado de filas en relación con el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="8fc5b-111">Este porcentaje se especifica en los parámetros _ulNumerator_ y _ulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="8fc5b-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="8fc5b-112">**SeekRowApprox** se usa con frecuencia para implementar las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="8fc5b-113">**Para determinar la posición aproximada de una tabla**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="8fc5b-114">Llame a [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="8fc5b-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="8fc5b-115">**QueryPosition** puede utilizarse para informar al usuario de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="8fc5b-116">Establece un valor fraccionario según el número de filas en la tabla y el número de la fila actual.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="8fc5b-117">Esperar que este valor representa una aproximación.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="8fc5b-118">Se recomienda no para calcular la posición exacta debido a que las implementaciones precisas pueden ser costosas invocar, especialmente en las tablas ordenadas por categorías los implementadores de tabla.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8fc5b-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="8fc5b-119">See also</span></span>



[<span data-ttu-id="8fc5b-120">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="8fc5b-120">MAPI Tables</span></span>](mapi-tables.md)

