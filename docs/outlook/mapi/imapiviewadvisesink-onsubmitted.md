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
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433986"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="c56e3-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="c56e3-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="c56e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c56e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c56e3-105">Notifica al visor de formularios que el mensaje actual se ha enviado a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="c56e3-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="c56e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c56e3-106">Parameters</span></span>

<span data-ttu-id="c56e3-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c56e3-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c56e3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c56e3-108">Return value</span></span>

<span data-ttu-id="c56e3-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="c56e3-109">S_OK</span></span> 
  
> <span data-ttu-id="c56e3-110">La notificación se ha publicado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56e3-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c56e3-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c56e3-111">Remarks</span></span>

<span data-ttu-id="c56e3-112">Un objeto de formulario llama al método **IMAPIViewAdviseSink::OnSubmitted** después de que se haya devuelto correctamente una llamada a [IMAPIMessageSite::SubmitMessage.](imapimessagesite-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="c56e3-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c56e3-113">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="c56e3-113">Notes to implementers</span></span>

<span data-ttu-id="c56e3-114">Después **de llamar a OnSubmitted,** puede continuar sugiendo que el mensaje se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="c56e3-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="c56e3-115">Actualiza las ventanas para reflejar los cambios que se han producido.</span><span class="sxs-lookup"><span data-stu-id="c56e3-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="c56e3-116">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="c56e3-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c56e3-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c56e3-117">See also</span></span>



[<span data-ttu-id="c56e3-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c56e3-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="c56e3-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c56e3-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

