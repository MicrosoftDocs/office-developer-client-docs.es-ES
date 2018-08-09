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
ms.openlocfilehash: 5859d94f85ca3fe7a0c738ed596d3c1a11fb2e8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818047"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="327b7-103">Administración de memoria en MAPI</span><span class="sxs-lookup"><span data-stu-id="327b7-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="327b7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="327b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="327b7-105">Sepa cómo y cuándo asignar y liberar memoria es una parte importante de la programación con MAPI.</span><span class="sxs-lookup"><span data-stu-id="327b7-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="327b7-106">MAPI proporciona funciones tanto las macros que su proveedor de servicio o cliente puede usar para administrar la memoria de una manera coherente.</span><span class="sxs-lookup"><span data-stu-id="327b7-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="327b7-107">Las tres funciones son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="327b7-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="327b7-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="327b7-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="327b7-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="327b7-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="327b7-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="327b7-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="327b7-111">Cuando los clientes y proveedores de servicios de usan estas funciones, el problema de "propietario", es decir, sabe cómo liberar: se ha eliminado un bloque de memoria en particular.</span><span class="sxs-lookup"><span data-stu-id="327b7-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="327b7-112">Un cliente llama a un método de proveedor de servicio no necesita pasar un búfer suficientemente grande para contener un valor devuelto de cualquier tamaño.</span><span class="sxs-lookup"><span data-stu-id="327b7-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="327b7-113">El proveedor de servicios simplemente puede asignar la cantidad adecuada de memoria mediante **MAPIAllocateBuffer** y, si es necesario, **MAPIAllocateMore**y el cliente pueden más adelante liberarlo a voluntad mediante **MAPIFreeBuffer**, independiente del servicio proveedor.</span><span class="sxs-lookup"><span data-stu-id="327b7-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="327b7-114">Las macros de memoria se utilizan para asignar las estructuras o matrices de las estructuras de un tamaño específico.</span><span class="sxs-lookup"><span data-stu-id="327b7-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="327b7-115">Los clientes y proveedores de servicios deben usar estas macros en lugar de asignar la memoria de forma manual.</span><span class="sxs-lookup"><span data-stu-id="327b7-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="327b7-116">Por ejemplo, si un cliente necesita para llevar a cabo la resolución de nombres en una lista de destinatarios con tres entradas de procesamiento, se puede utilizar la macro **SizedADRLIST** para crear una estructura **ADRLIST** que se pase a **IAddrBook::ResolveName** con el número correcto de Miembros **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="327b7-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="327b7-117">Todas las macros de memoria se definen en el MAPIDEFS. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="327b7-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="327b7-118">Estas macros son:</span><span class="sxs-lookup"><span data-stu-id="327b7-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="327b7-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="327b7-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="327b7-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="327b7-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="327b7-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="327b7-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="327b7-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="327b7-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="327b7-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="327b7-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="327b7-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="327b7-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="327b7-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="327b7-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="327b7-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="327b7-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="327b7-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="327b7-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="327b7-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="327b7-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="327b7-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="327b7-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="327b7-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="327b7-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="327b7-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="327b7-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="327b7-132">MAPI también admite el uso de la interfaz [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) de COM para la administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="327b7-132">MAPI also supports the use of the COM interface [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="327b7-133">Proveedores de servicios se conceden un puntero de interfaz **IMalloc** por MAPI en la inicialización y también pueden recuperar uno a través de la función [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) .</span><span class="sxs-lookup"><span data-stu-id="327b7-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="327b7-134">La principal ventaja de utilizar los métodos **IMalloc** para la administración de memoria a través de las funciones MAPI es que con los métodos COM es posible reasignar un búfer existente.</span><span class="sxs-lookup"><span data-stu-id="327b7-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="327b7-135">Las funciones de memoria MAPI no admiten la reasignación.</span><span class="sxs-lookup"><span data-stu-id="327b7-135">The MAPI memory functions do not support reallocation.</span></span> 
  

