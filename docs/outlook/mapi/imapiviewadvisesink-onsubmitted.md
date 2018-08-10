---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 40a72bed0b3e763ea482b228174b85d9f42185c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817613"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="c716d-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="c716d-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="c716d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c716d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c716d-105">Se notifica al Visor de formulario que se ha enviado el mensaje actual a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="c716d-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="c716d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c716d-106">Parameters</span></span>

<span data-ttu-id="c716d-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c716d-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c716d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c716d-108">Return value</span></span>

<span data-ttu-id="c716d-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="c716d-109">S_OK</span></span> 
  
> <span data-ttu-id="c716d-110">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c716d-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c716d-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c716d-111">Remarks</span></span>

<span data-ttu-id="c716d-112">Un objeto de formulario llama al método de **IMAPIViewAdviseSink::OnSubmitted** después de que una llamada a [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) devuelva correctamente.</span><span class="sxs-lookup"><span data-stu-id="c716d-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c716d-113">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="c716d-113">Notes to implementers</span></span>

<span data-ttu-id="c716d-114">Después de llamar a **OnSubmitted** , puede continuar en la suposición de que se ha actualizado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c716d-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="c716d-115">Actualice sus windows para reflejar los cambios que se han producido.</span><span class="sxs-lookup"><span data-stu-id="c716d-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="c716d-116">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c716d-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c716d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c716d-117">See also</span></span>



[<span data-ttu-id="c716d-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c716d-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="c716d-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c716d-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

