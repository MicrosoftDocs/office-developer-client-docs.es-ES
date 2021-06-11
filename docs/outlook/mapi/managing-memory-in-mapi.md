---
title: Administración de memoria en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298099"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="0f63e-103">Administración de memoria en MAPI</span><span class="sxs-lookup"><span data-stu-id="0f63e-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="0f63e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f63e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f63e-105">Saber cómo y cuándo asignar y liberar memoria es una parte importante de la programación con MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f63e-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="0f63e-106">MAPI proporciona funciones y macros que el cliente o el proveedor de servicios pueden usar para administrar la memoria de forma coherente.</span><span class="sxs-lookup"><span data-stu-id="0f63e-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="0f63e-107">Las tres funciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="0f63e-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="0f63e-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0f63e-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="0f63e-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="0f63e-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="0f63e-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0f63e-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="0f63e-111">Cuando los clientes y los proveedores de servicios usan estas funciones, se elimina el problema de quién "posee" (es decir, sabe cómo liberar) un bloque determinado de memoria.</span><span class="sxs-lookup"><span data-stu-id="0f63e-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="0f63e-112">Un cliente que llama a un método de proveedor de servicios no necesita pasar un búfer lo suficientemente grande como para contener un valor devuelto de cualquier tamaño.</span><span class="sxs-lookup"><span data-stu-id="0f63e-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="0f63e-113">El proveedor de servicios simplemente puede asignar la cantidad adecuada de memoria mediante **MAPIAllocateBuffer** y, si es necesario, **MAPIAllocateMore**, y el cliente puede liberarla posteriormente a voluntad usando **MAPIFreeBuffer**, independientemente del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="0f63e-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="0f63e-114">Las macros de memoria se usan para asignar estructuras o matrices de estructuras de un tamaño específico.</span><span class="sxs-lookup"><span data-stu-id="0f63e-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="0f63e-115">Los clientes y proveedores de servicios deben usar estas macros en lugar de asignar la memoria manualmente.</span><span class="sxs-lookup"><span data-stu-id="0f63e-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="0f63e-116">Por ejemplo, si un cliente necesita realizar el procesamiento de resolución de nombres en una lista de destinatarios con tres entradas, la macro **SizedADRLIST** se puede usar para crear una estructura **ADRLIST** para pasar a **IAddrBook::ResolveName** con el número correcto de miembros **adrentry.**</span><span class="sxs-lookup"><span data-stu-id="0f63e-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="0f63e-117">Todas las macros de memoria se definen en MAPIDEFS. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="0f63e-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="0f63e-118">Estas macros son:</span><span class="sxs-lookup"><span data-stu-id="0f63e-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="0f63e-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="0f63e-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="0f63e-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="0f63e-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="0f63e-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="0f63e-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="0f63e-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="0f63e-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="0f63e-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="0f63e-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="0f63e-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0f63e-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="0f63e-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="0f63e-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="0f63e-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="0f63e-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="0f63e-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="0f63e-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="0f63e-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="0f63e-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="0f63e-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="0f63e-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="0f63e-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="0f63e-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="0f63e-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="0f63e-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="0f63e-132">MAPI también admite el uso de la interfaz COM [IMalloc para](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) la administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="0f63e-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="0f63e-133">MAPI proporciona a los proveedores de servicios un puntero de interfaz **IMalloc** en el momento de la inicialización y también puede recuperar uno a través de la [función MAPIGetDefaultMalloc.](mapigetdefaultmalloc.md)</span><span class="sxs-lookup"><span data-stu-id="0f63e-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="0f63e-134">La principal ventaja de usar los métodos **IMalloc** para administrar la memoria a través de las funciones MAPI es que con los métodos COM es posible reasignar un búfer existente.</span><span class="sxs-lookup"><span data-stu-id="0f63e-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="0f63e-135">Las funciones de memoria MAPI no admiten la reasignación.</span><span class="sxs-lookup"><span data-stu-id="0f63e-135">The MAPI memory functions do not support reallocation.</span></span> 
  

