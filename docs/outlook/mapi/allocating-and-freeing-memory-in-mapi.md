---
title: Asignar y liberar memoria en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dc97abcb4b316b696032f2788f4e653717e1396b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816418"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a><span data-ttu-id="375ba-103">Asignar y liberar memoria en MAPI</span><span class="sxs-lookup"><span data-stu-id="375ba-103">Allocating and Freeing Memory in MAPI</span></span>

  
  
<span data-ttu-id="375ba-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="375ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="375ba-105">Además de especificar cómo asignar y liberar memoria, MAPI define un modelo para saber cuándo memoria se pasa entre el método de interfaz pública y función de la API deben liberarse a las llamadas.</span><span class="sxs-lookup"><span data-stu-id="375ba-105">In addition to specifying how to allocate and free memory, MAPI defines a model for knowing when memory passed between public interface method and API function calls should be freed.</span></span> <span data-ttu-id="375ba-106">El modelo se aplica sólo a la memoria asignada para los parámetros que no sean punteros a las interfaces, como cadenas y punteros a estructuras.</span><span class="sxs-lookup"><span data-stu-id="375ba-106">The model applies only to memory allocated for parameters that are not pointers to interfaces, such as strings and pointers to structures.</span></span> <span data-ttu-id="375ba-107">Punteros de interfaz usar el mecanismo de implementada a través de **IUnknown**de recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="375ba-107">Interface pointers use the reference counting mechanism implemented through **IUnknown**.</span></span> <span data-ttu-id="375ba-108">Al asignar y liberar MAPI no relacionadas con la memoria internamente dentro de una aplicación de cliente o un proveedor de servicios, use cualquier mecanismo sentido.</span><span class="sxs-lookup"><span data-stu-id="375ba-108">When allocating and freeing non-MAPI related memory internally within a client application or service provider, use whatever mechanism makes sense.</span></span> 
  
<span data-ttu-id="375ba-109">El modelo define parámetros como uno de los tres tipos.</span><span class="sxs-lookup"><span data-stu-id="375ba-109">The model defines parameters as one of three types.</span></span> <span data-ttu-id="375ba-110">Puede introducir parámetros, establecidos por el autor de la llamada con información que va a usar la función o método llamado, parámetros de salida, establecido por el método o la función llamada y devuelto para el autor de la llamada, o los parámetros de entrada y salida, una combinación de los dos tipos.</span><span class="sxs-lookup"><span data-stu-id="375ba-110">They can be input parameters, set by the caller with information to be used by the called function or method, output parameters, set by the called function or method and returned to the caller, or input-output parameters, a combination of the two types.</span></span> <span data-ttu-id="375ba-111">Los parámetros de salida con frecuencia son punteros a los datos o punteros a punteros a los datos.</span><span class="sxs-lookup"><span data-stu-id="375ba-111">Output parameters are frequently pointers to data or pointers to pointers to data.</span></span> <span data-ttu-id="375ba-112">Aunque la función llamada es responsable de asignar los datos para los parámetros de salida, el autor de la llamada asigna la memoria para el puntero.</span><span class="sxs-lookup"><span data-stu-id="375ba-112">Although the called function is responsible for allocating the data for output parameters, the caller allocates the memory for the pointer.</span></span> 
  
<span data-ttu-id="375ba-113">Las reglas para asignar y liberar memoria para estos tipos de los parámetros se explican en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="375ba-113">The rules for allocating and releasing memory for these types of parameters are explained in the following table.</span></span>
  
|<span data-ttu-id="375ba-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="375ba-114">**Type**</span></span>|<span data-ttu-id="375ba-115">**Asignación de memoria**</span><span class="sxs-lookup"><span data-stu-id="375ba-115">**Memory allocation**</span></span>|<span data-ttu-id="375ba-116">**Versión de memoria**</span><span class="sxs-lookup"><span data-stu-id="375ba-116">**Memory release**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="375ba-117">Input</span><span class="sxs-lookup"><span data-stu-id="375ba-117">Input</span></span>  <br/> |<span data-ttu-id="375ba-118">Autor de la llamada es responsable y puede usar cualquier mecanismo.</span><span class="sxs-lookup"><span data-stu-id="375ba-118">Caller is responsible and can use any mechanism.</span></span>  <br/> |<span data-ttu-id="375ba-119">Autor de la llamada es responsable y puede usar cualquier mecanismo.</span><span class="sxs-lookup"><span data-stu-id="375ba-119">Caller is responsible and can use any mechanism.</span></span>  <br/> |
|<span data-ttu-id="375ba-120">Output</span><span class="sxs-lookup"><span data-stu-id="375ba-120">Output</span></span>  <br/> |<span data-ttu-id="375ba-121">Función llamada es responsable y debe usar **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="375ba-121">Called function is responsible and must use **MAPIAllocateBuffer**.</span></span> <span data-ttu-id="375ba-122">Para obtener más información, vea [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="375ba-122">For more information, see [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>  <br/> |<span data-ttu-id="375ba-123">Autor de la llamada es responsable y debe usar **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="375ba-123">Caller is responsible and must use **MAPIFreeBuffer**.</span></span> <span data-ttu-id="375ba-124">Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="375ba-124">For more information, see [MAPIFreeBuffer](mapifreebuffer.md).</span></span>  <br/> |
|<span data-ttu-id="375ba-125">De entrada y salida</span><span class="sxs-lookup"><span data-stu-id="375ba-125">Input-output</span></span>  <br/> |<span data-ttu-id="375ba-126">Autor de la llamada es responsable de la asignación inicial y la función llamada pueden reasignar si es necesario mediante **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="375ba-126">Caller is responsible for the initial allocation and called function can reallocate if necessary using **MAPIAllocateBuffer**.</span></span>  <br/> |<span data-ttu-id="375ba-127">Función llamada es responsable de liberar inicial si es necesaria reasignación.</span><span class="sxs-lookup"><span data-stu-id="375ba-127">Called function is responsible for initial freeing if reallocation is necessary.</span></span> <span data-ttu-id="375ba-128">Autor de la llamada debe liberar el valor devuelto final.</span><span class="sxs-lookup"><span data-stu-id="375ba-128">Caller must free the final return value.</span></span>  <br/> |
   
<span data-ttu-id="375ba-129">Durante las condiciones de error, los implementadores de los métodos de interfaz que necesite preste atención a los parámetros de salida y de entrada y salida debido a que el autor de la llamada normalmente no tiene ninguna forma de limpieza de ellos.</span><span class="sxs-lookup"><span data-stu-id="375ba-129">During failure conditions, implementers of interface methods need to pay attention to output and input-output parameters because the caller generally has no way to clean them up.</span></span> <span data-ttu-id="375ba-130">Si se devuelve un error, a continuación, cada resultado o el parámetro de entrada y salida debe ser de izquierda en el valor inicializado el autor de la llamada o establecer en un valor que se puede limpiar sin ninguna acción por parte del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="375ba-130">If an error is returned, then each output or input-output parameter must either be left at the value initialized by the caller or set to a value that can be cleaned up without any action on the part of the caller.</span></span> <span data-ttu-id="375ba-131">Por ejemplo, un puntero-parámetro de salida de `void ** ppv` debe mantenerse tal como estaba en la entrada, o se puede establecer en NULL ( `*ppv = NULL`).</span><span class="sxs-lookup"><span data-stu-id="375ba-131">For example, an output pointer-parameter of  `void ** ppv` must be left as it was on input or can be set to NULL (  `*ppv = NULL`).</span></span>
  
