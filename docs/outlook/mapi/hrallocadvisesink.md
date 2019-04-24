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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348219"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="89a52-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="89a52-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="89a52-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89a52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89a52-105">Crea un objeto de receptor de notificaciones, dado un contexto especificado por la implementación de llamada y una función de devolución de llamada que se desencadenará mediante una notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="89a52-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89a52-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="89a52-106">Header file:</span></span>  <br/> |<span data-ttu-id="89a52-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="89a52-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="89a52-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="89a52-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="89a52-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="89a52-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="89a52-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="89a52-110">Called by:</span></span>  <br/> |<span data-ttu-id="89a52-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="89a52-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="89a52-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="89a52-112">Parameters</span></span>

 <span data-ttu-id="89a52-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="89a52-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="89a52-114">a Puntero a una función de devolución de llamada basada en el prototipo [NOTIFCALLBACK](notifcallback.md) al que MAPI debe llamar cuando se produce un evento de notificación para el receptor de notificaciones recién creado.</span><span class="sxs-lookup"><span data-stu-id="89a52-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="89a52-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="89a52-115">_lpvContext_</span></span>
  
> <span data-ttu-id="89a52-116">a Puntero a los datos del autor de la llamada pasados a la función de devolución de llamada cuando MAPI los llama.</span><span class="sxs-lookup"><span data-stu-id="89a52-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="89a52-117">Los datos del autor de la llamada pueden representar una dirección de importancia para el cliente o el proveedor.</span><span class="sxs-lookup"><span data-stu-id="89a52-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="89a52-118">Normalmente, para código de C++, el parámetro _lpvContext_ representa un puntero a la dirección de un objeto.</span><span class="sxs-lookup"><span data-stu-id="89a52-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="89a52-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="89a52-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="89a52-120">contempla Puntero a un puntero a un objeto de receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="89a52-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="89a52-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89a52-121">Return value</span></span>

<span data-ttu-id="89a52-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="89a52-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89a52-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89a52-123">Remarks</span></span>

<span data-ttu-id="89a52-124">Para usar la función **HrAllocAdviseSink** , una aplicación cliente o un proveedor de servicios crea un objeto para recibir notificaciones, crea una función de devolución de llamada de notificación basada en el prototipo de función [NOTIFCALLBACK](notifcallback.md) que va con ese objeto, y pasa un puntero al objeto en la función **HrAllocAdviseSink** como el valor _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="89a52-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="89a52-125">Al hacerlo, se realiza una notificación; como parte del proceso de notificación, MAPI llama a la función de devolución de llamada con el puntero del objeto como contexto.</span><span class="sxs-lookup"><span data-stu-id="89a52-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="89a52-126">MAPI implementa su motor de notificación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="89a52-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="89a52-127">En C++, la devolución de llamada de la notificación puede ser un método de objeto.</span><span class="sxs-lookup"><span data-stu-id="89a52-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="89a52-128">Si el objeto que genera la notificación no está presente, el cliente o proveedor que solicita la notificación debe mantener un recuento de referencia independiente para ese objeto para el receptor de notificaciones del objeto.</span><span class="sxs-lookup"><span data-stu-id="89a52-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="89a52-129">**HrAllocAdviseSink** debe usarse con moderación; es más seguro para los clientes crear sus propios receptores de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="89a52-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

