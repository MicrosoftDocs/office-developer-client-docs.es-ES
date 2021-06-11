---
title: Administrar memoria para ADRLIST y estructuras SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407868"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="d0025-103">Administración de memoria para estructuras ADRLIST y SRowSet"</span><span class="sxs-lookup"><span data-stu-id="d0025-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="d0025-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0025-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0025-105">El requisito de asignar toda la memoria de un búfer siempre que sea posible con una sola llamada **MAPIAllocateBuffer** no se aplica al usar la lista de direcciones, **o ADRLIST**, y el conjunto de filas, o **SRowSet**, estructuras.</span><span class="sxs-lookup"><span data-stu-id="d0025-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="d0025-106">Estas dos estructuras son excepciones a las reglas estándar para asignar y liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="d0025-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="d0025-107">Contienen varios niveles de estructuras y están diseñadas para permitir que los miembros individuales se puedan agregar o quitar.</span><span class="sxs-lookup"><span data-stu-id="d0025-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="d0025-108">Por lo tanto, cada propiedad debe ser una asignación independiente.</span><span class="sxs-lookup"><span data-stu-id="d0025-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="d0025-109">Donde la mayoría de las estructuras se liberan con una llamada a **MAPIFreeBuffer**, cada entrada individual de una estructura **ADRLIST** o **SRowSet** debe liberarse con su propia llamada a **MAPIFreeBuffer** o una sola llamada a **FreeProws** o **FreePadrlist**.</span><span class="sxs-lookup"><span data-stu-id="d0025-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="d0025-110">Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)y [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="d0025-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="d0025-111">**FreeProws** y **FreePadrlist** son funciones proporcionadas por MAPI para simplificar la libertad de estas estructuras de datos.</span><span class="sxs-lookup"><span data-stu-id="d0025-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="d0025-112">Para obtener más información, [vea FreeProws](freeprows.md) y [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="d0025-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="d0025-113">**FreePadrlist** libera la memoria de la estructura **ADRLIST** más toda la memoria asociada para los miembros de la estructura; **FreeProws hace** lo mismo para la **estructura SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="d0025-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="d0025-114">En el diagrama siguiente se muestra el diseño de una estructura de datos **ADRLIST,** que indica las asignaciones de memoria independientes necesarias.</span><span class="sxs-lookup"><span data-stu-id="d0025-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="d0025-115">Los cuadros grises muestran la memoria que se puede asignar y liberar con una llamada.</span><span class="sxs-lookup"><span data-stu-id="d0025-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="d0025-116">**Asignación de memoria de ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="d0025-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="d0025-117">![Asignación de memoria ADRLIST](media/amapi_52.gif "ADRLIST asignación de memoria ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="d0025-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0025-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0025-118">See also</span></span>

- [<span data-ttu-id="d0025-119">Administración de memoria en MAPI</span><span class="sxs-lookup"><span data-stu-id="d0025-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

