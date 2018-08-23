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
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589325"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="63d74-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="63d74-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="63d74-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63d74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63d74-105">Crea un objeto de receptor advise, dado un contexto especificado por la implementación de llamada y una función de devolución de llamada que se desencadene mediante una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="63d74-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63d74-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="63d74-106">Header file:</span></span>  <br/> |<span data-ttu-id="63d74-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="63d74-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="63d74-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="63d74-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="63d74-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="63d74-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="63d74-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="63d74-110">Called by:</span></span>  <br/> |<span data-ttu-id="63d74-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="63d74-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="63d74-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63d74-112">Parameters</span></span>

 <span data-ttu-id="63d74-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="63d74-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="63d74-114">[entrada] Puntero a una función de devolución de llamada según el prototipo [NOTIFCALLBACK](notifcallback.md) es MAPI que se llama cuando se produce un evento de notificación para el recién creada de aviso receptor.</span><span class="sxs-lookup"><span data-stu-id="63d74-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="63d74-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="63d74-115">_lpvContext_</span></span>
  
> <span data-ttu-id="63d74-116">[entrada] Puntero a los datos del autor de la llamada se pasa a la función de devolución de llamada cuando llama a MAPI.</span><span class="sxs-lookup"><span data-stu-id="63d74-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="63d74-117">Los datos del autor de la llamada pueden representar una dirección de cifra significativa para el cliente o el proveedor.</span><span class="sxs-lookup"><span data-stu-id="63d74-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="63d74-118">Normalmente, para el código de C++, el parámetro _lpvContext_ representa un puntero a la dirección de un objeto.</span><span class="sxs-lookup"><span data-stu-id="63d74-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="63d74-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="63d74-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="63d74-120">[out] Puntero a un puntero a un objeto de receptor advise.</span><span class="sxs-lookup"><span data-stu-id="63d74-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63d74-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63d74-121">Return value</span></span>

<span data-ttu-id="63d74-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="63d74-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63d74-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63d74-123">Remarks</span></span>

<span data-ttu-id="63d74-124">Para usar la función **HrAllocAdviseSink** , una aplicación de cliente o un proveedor de servicios crea un objeto para recibir notificaciones, crea una función de devolución de llamada de notificación según el prototipo de función [NOTIFCALLBACK](notifcallback.md) que va asociado con ese objeto y pasa un puntero al objeto en la función **HrAllocAdviseSink** como el valor de _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="63d74-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="63d74-125">Al hacerlo, realiza una notificación; y como parte del proceso de notificación, llama a la función de devolución de llamada con el puntero de objeto como el contexto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="63d74-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="63d74-126">MAPI implementa su motor de notificación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="63d74-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="63d74-127">En C++, la devolución de llamada de notificación puede ser un método de objeto.</span><span class="sxs-lookup"><span data-stu-id="63d74-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="63d74-128">Si el objeto generación de la notificación no está presente, el cliente o proveedor que solicita notificación debe mantener un recuento de referencia independiente para ese objeto para el objeto de aviso receptor.</span><span class="sxs-lookup"><span data-stu-id="63d74-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="63d74-129">**HrAllocAdviseSink** debe usarse con moderación; es más seguro para los clientes crear sus propios receptores advise.</span><span class="sxs-lookup"><span data-stu-id="63d74-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

