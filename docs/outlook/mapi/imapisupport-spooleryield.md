---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409912"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="d5b12-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="d5b12-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="d5b12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5b12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5b12-105">Proporciona el control de la CPU a la cola MAPI para que pueda llevar a cabo las tareas que estime necesarias.</span><span class="sxs-lookup"><span data-stu-id="d5b12-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d5b12-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5b12-106">Parameters</span></span>

 <span data-ttu-id="d5b12-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5b12-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d5b12-108">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d5b12-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5b12-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5b12-109">Return value</span></span>

<span data-ttu-id="d5b12-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5b12-110">S_OK</span></span> 
  
> <span data-ttu-id="d5b12-111">El proveedor de transporte liberó correctamente la CPU.</span><span class="sxs-lookup"><span data-stu-id="d5b12-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="d5b12-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d5b12-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="d5b12-113">Indica al proveedor de transporte que detenga la entrega del mensaje a todos los destinatarios que todavía no lo hayan recibido.</span><span class="sxs-lookup"><span data-stu-id="d5b12-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5b12-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5b12-114">Remarks</span></span>

<span data-ttu-id="d5b12-115">El método **IMAPISupport:: SpoolerYield** se implementa para los objetos de soporte del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="d5b12-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="d5b12-116">Los proveedores de transporte llaman a **SpoolerYield** para permitir que la cola MAPI realice cualquier procesamiento necesario.</span><span class="sxs-lookup"><span data-stu-id="d5b12-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5b12-117">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d5b12-117">Notes to callers</span></span>

<span data-ttu-id="d5b12-118">Llame a **SpoolerYield** cuando esté realizando operaciones de larga duración que se pueden pausar.</span><span class="sxs-lookup"><span data-stu-id="d5b12-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="d5b12-119">Esto permite que las aplicaciones de primer plano se ejecuten durante una operación larga, como la entrega a una lista de destinatarios de gran tamaño a través de una red ocupada.</span><span class="sxs-lookup"><span data-stu-id="d5b12-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="d5b12-120">Si **SpoolerYield** devuelve con MAPI_W_CANCEL_MESSAGE, la cola de MAPI determinó que el mensaje ya no debería enviarse.</span><span class="sxs-lookup"><span data-stu-id="d5b12-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="d5b12-121">Devolver MAPI_E_USER_CANCEL al proceso de llamada y salir, si es posible.</span><span class="sxs-lookup"><span data-stu-id="d5b12-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="d5b12-122">Para obtener más información acerca de la obtención de la cola MAPI, vea [interactuar con la cola MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="d5b12-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5b12-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="d5b12-123">See also</span></span>



[<span data-ttu-id="d5b12-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5b12-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

