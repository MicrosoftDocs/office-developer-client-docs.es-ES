---
title: Administración de la memoria para las estructuras ADRLIST y SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589731"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="5a909-103">Administración de la memoria para las estructuras ADRLIST y SRowSet"</span><span class="sxs-lookup"><span data-stu-id="5a909-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="5a909-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a909-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a909-105">El requisito de asignar toda la memoria para un búfer siempre que sea posible con una sola llamada **MAPIAllocateBuffer** no se aplica cuando se usa la lista de direcciones, o las estructuras de **ADRLIST**y el conjunto de filas o **SRowSet**.</span><span class="sxs-lookup"><span data-stu-id="5a909-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="5a909-106">Estos dos estructuras son excepciones a las reglas estándares para asignar y liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="5a909-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="5a909-107">Contienen varios niveles de estructuras y están diseñados para permitir que se agreguen o eliminen miembros individuales.</span><span class="sxs-lookup"><span data-stu-id="5a909-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="5a909-108">Por lo tanto, cada propiedad debe ser una asignación independiente.</span><span class="sxs-lookup"><span data-stu-id="5a909-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="5a909-109">Donde se libera la mayoría de las estructuras con una llamada a **MAPIFreeBuffer**, cada entrada individual de una estructura de **ADRLIST** o **SRowSet** se debe liberar con su propia llamada a **MAPIFreeBuffer** o una sola llamada a **FreeProws** o ** FreePadrlist**.</span><span class="sxs-lookup"><span data-stu-id="5a909-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="5a909-110">Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)y [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="5a909-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="5a909-111">**FreeProws** y **FreePadrlist** son funciones proporcionadas por MAPI para simplificar la liberación de estas estructuras de datos.</span><span class="sxs-lookup"><span data-stu-id="5a909-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="5a909-112">Para obtener más información, vea [FreeProws](freeprows.md) y [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="5a909-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="5a909-113">**FreePadrlist** libera la memoria para la estructura **ADRLIST** más la memoria de todos los asociados para los miembros de la estructura; **FreeProws** hace lo mismo para la estructura **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="5a909-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="5a909-114">En el siguiente diagrama muestra el diseño de una estructura de datos **ADRLIST** , que indica las asignaciones de memoria independientes necesarias.</span><span class="sxs-lookup"><span data-stu-id="5a909-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="5a909-115">Los cuadros gris muestran de memoria que puede se asignan y liberan con una llamada.</span><span class="sxs-lookup"><span data-stu-id="5a909-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="5a909-116">**Asignación de memoria de ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="5a909-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="5a909-117">![Memoria de adrlist] (media/amapi_52.gif "Memoria de adrlist")</span><span class="sxs-lookup"><span data-stu-id="5a909-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a909-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5a909-118">See also</span></span>

- [<span data-ttu-id="5a909-119">Administración de memoria en MAPI</span><span class="sxs-lookup"><span data-stu-id="5a909-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

