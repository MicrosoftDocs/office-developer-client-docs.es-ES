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
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584957"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="20368-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="20368-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="20368-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20368-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20368-105">Proporciona control de la CPU a la cola de MAPI para que pueda realizar las tareas que considere necesarias.</span><span class="sxs-lookup"><span data-stu-id="20368-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="20368-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="20368-106">Parameters</span></span>

 <span data-ttu-id="20368-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20368-107">_ulFlags_</span></span>
  
> <span data-ttu-id="20368-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="20368-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20368-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20368-109">Return value</span></span>

<span data-ttu-id="20368-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="20368-110">S_OK</span></span> 
  
> <span data-ttu-id="20368-111">El proveedor de transporte había publicado correctamente la CPU.</span><span class="sxs-lookup"><span data-stu-id="20368-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="20368-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="20368-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="20368-113">Indica el proveedor de transporte para detener la entrega del mensaje a los destinatarios que aún no la ha recibido.</span><span class="sxs-lookup"><span data-stu-id="20368-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20368-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20368-114">Remarks</span></span>

<span data-ttu-id="20368-115">El método **IMAPISupport::SpoolerYield** se implementa para los objetos de soporte técnico del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="20368-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="20368-116">Los proveedores de transporte llame a **SpoolerYield** para permitir que la cola MAPI realizar cualquier procesamiento necesario.</span><span class="sxs-lookup"><span data-stu-id="20368-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="20368-117">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="20368-117">Notes to callers</span></span>

<span data-ttu-id="20368-118">Llame a **SpoolerYield** al realizar las operaciones largas que pueden poner en pausa.</span><span class="sxs-lookup"><span data-stu-id="20368-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="20368-119">Esto permite a las aplicaciones de primer plano para que se ejecute durante una operación larga, como la entrega a una lista de destinatarios grandes en una red ocupada.</span><span class="sxs-lookup"><span data-stu-id="20368-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="20368-120">Si **SpoolerYield** devuelve con MAPI_W_CANCEL_MESSAGE, la cola MAPI ha determinado que ya no se debe enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="20368-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="20368-121">Devolver MAPI_E_USER_CANCEL a su proceso de llamada y exit, si es posible.</span><span class="sxs-lookup"><span data-stu-id="20368-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="20368-122">Para obtener más información acerca de la obtención de la cola MAPI, consulte [interactuar con la cola de MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="20368-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20368-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="20368-123">See also</span></span>



[<span data-ttu-id="20368-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="20368-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

