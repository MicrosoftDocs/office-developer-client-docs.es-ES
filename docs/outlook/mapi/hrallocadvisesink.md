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
ms.openlocfilehash: 5a5e736e8be1120f5fb90048f01fdc8a44479060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817026"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="e96b8-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e96b8-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="e96b8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e96b8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e96b8-105">Crea un objeto de receptor advise, dado un contexto especificado por la implementación de llamada y una función de devolución de llamada que se desencadene mediante una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="e96b8-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e96b8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e96b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e96b8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e96b8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e96b8-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e96b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e96b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e96b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e96b8-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e96b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="e96b8-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e96b8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="e96b8-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e96b8-112">Parameters</span></span>

 <span data-ttu-id="e96b8-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="e96b8-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="e96b8-114">[entrada] Puntero a una función de devolución de llamada según el prototipo [NOTIFCALLBACK](notifcallback.md) es MAPI que se llama cuando se produce un evento de notificación para el recién creada de aviso receptor.</span><span class="sxs-lookup"><span data-stu-id="e96b8-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="e96b8-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="e96b8-115">_lpvContext_</span></span>
  
> <span data-ttu-id="e96b8-116">[entrada] Puntero a los datos del autor de la llamada se pasa a la función de devolución de llamada cuando llama a MAPI.</span><span class="sxs-lookup"><span data-stu-id="e96b8-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="e96b8-117">Los datos del autor de la llamada pueden representar una dirección de cifra significativa para el cliente o el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e96b8-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="e96b8-118">Normalmente, para el código de C++, el parámetro _lpvContext_ representa un puntero a la dirección de un objeto.</span><span class="sxs-lookup"><span data-stu-id="e96b8-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="e96b8-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="e96b8-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="e96b8-120">[out] Puntero a un puntero a un objeto de receptor advise.</span><span class="sxs-lookup"><span data-stu-id="e96b8-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e96b8-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e96b8-121">Return value</span></span>

<span data-ttu-id="e96b8-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e96b8-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e96b8-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e96b8-123">Remarks</span></span>

<span data-ttu-id="e96b8-124">Para usar la función **HrAllocAdviseSink** , una aplicación de cliente o un proveedor de servicios crea un objeto para recibir notificaciones, crea una función de devolución de llamada de notificación según el prototipo de función [NOTIFCALLBACK](notifcallback.md) que va asociado con ese objeto y pasa un puntero al objeto en la función **HrAllocAdviseSink** como el valor de _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="e96b8-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="e96b8-125">Al hacerlo, realiza una notificación; y como parte del proceso de notificación, llama a la función de devolución de llamada con el puntero de objeto como el contexto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e96b8-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="e96b8-126">MAPI implementa su motor de notificación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e96b8-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="e96b8-127">En C++, la devolución de llamada de notificación puede ser un método de objeto.</span><span class="sxs-lookup"><span data-stu-id="e96b8-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="e96b8-128">Si el objeto generación de la notificación no está presente, el cliente o proveedor que solicita notificación debe mantener un recuento de referencia independiente para ese objeto para el objeto de aviso receptor.</span><span class="sxs-lookup"><span data-stu-id="e96b8-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="e96b8-129">**HrAllocAdviseSink** debe usarse con moderación; es más seguro para los clientes crear sus propios receptores advise.</span><span class="sxs-lookup"><span data-stu-id="e96b8-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

