---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428903"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="cc824-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="cc824-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="cc824-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc824-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc824-105">Crea un objeto receptor de aviso, dado un contexto especificado por la implementación de llamada y una función de devolución de llamada que se desencadenará mediante una notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="cc824-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc824-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cc824-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc824-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cc824-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cc824-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="cc824-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cc824-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc824-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc824-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="cc824-110">Called by:</span></span>  <br/> |<span data-ttu-id="cc824-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="cc824-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="cc824-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="cc824-112">Parameters</span></span>

 <span data-ttu-id="cc824-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="cc824-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="cc824-114">[in] Puntero a una función de devolución de llamada basada en el prototipo [NOTIFCALLBACK](notifcallback.md) al que MAPI llamará cuando se produzca un evento de notificación para el receptor de notificaciones recién creado.</span><span class="sxs-lookup"><span data-stu-id="cc824-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="cc824-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="cc824-115">_lpvContext_</span></span>
  
> <span data-ttu-id="cc824-116">[in] Puntero a los datos de autor de la llamada pasados a la función de devolución de llamada cuando MAPI lo llama.</span><span class="sxs-lookup"><span data-stu-id="cc824-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="cc824-117">Los datos del autor de la llamada pueden representar una dirección de importancia para el cliente o el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cc824-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="cc824-118">Normalmente, para el código C++, el parámetro  _lpvContext_ representa un puntero a la dirección de un objeto.</span><span class="sxs-lookup"><span data-stu-id="cc824-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="cc824-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="cc824-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="cc824-120">[salida] Puntero a un puntero a un objeto receptor de aviso.</span><span class="sxs-lookup"><span data-stu-id="cc824-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc824-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc824-121">Return value</span></span>

<span data-ttu-id="cc824-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc824-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc824-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc824-123">Remarks</span></span>

<span data-ttu-id="cc824-124">Para usar la función **HrAllocAdviseSink,** una aplicación cliente o un proveedor de servicios crea un objeto para recibir notificaciones, crea una función de devolución de llamada de notificación basada en el prototipo de función [NOTIFCALLBACK](notifcallback.md) que va con ese objeto y pasa un puntero al objeto en la **función HrAllocAdviseSink** como valor _lpvContext._</span><span class="sxs-lookup"><span data-stu-id="cc824-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="cc824-125">Al hacerlo, se realiza una notificación; y como parte del proceso de notificación, MAPI llama a la función de devolución de llamada con el puntero de objeto como contexto.</span><span class="sxs-lookup"><span data-stu-id="cc824-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="cc824-126">MAPI implementa su motor de notificaciones de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cc824-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="cc824-127">En C++, la devolución de llamada de notificación puede ser un método de objeto.</span><span class="sxs-lookup"><span data-stu-id="cc824-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="cc824-128">Si el objeto que genera la notificación no está presente, el cliente o el proveedor que solicita la notificación debe mantener un recuento de referencias independiente para ese objeto para el receptor de avisos del objeto.</span><span class="sxs-lookup"><span data-stu-id="cc824-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="cc824-129">**HrAllocAdviseSink** debe usarse con moderación; es más seguro para los clientes crear sus propios receptores de asesoramiento.</span><span class="sxs-lookup"><span data-stu-id="cc824-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

