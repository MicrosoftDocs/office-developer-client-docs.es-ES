---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: adf9b28e941e9ead9b83660f58701f13f35cabc7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817628"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="74839-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="74839-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="74839-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74839-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74839-105">Se notifica al Visor de formulario que ha cargado un nuevo o un mensaje existente en un formulario.</span><span class="sxs-lookup"><span data-stu-id="74839-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="74839-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74839-106">Parameters</span></span>

<span data-ttu-id="74839-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="74839-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="74839-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74839-108">Return value</span></span>

<span data-ttu-id="74839-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="74839-109">S_OK</span></span> 
  
> <span data-ttu-id="74839-110">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="74839-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74839-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74839-111">Remarks</span></span>

<span data-ttu-id="74839-112">Objetos de formulario llaman al método de **IMAPIViewAdviseSink::OnNewMessage** siempre que se carga un mensaje en un formulario mediante los métodos [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="74839-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="74839-113">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="74839-113">Notes to implementers</span></span>

<span data-ttu-id="74839-114">Liberar su puntero al objeto form activo debido a que ya no apunta al mensaje que anteriormente estaba viendo el Visor.</span><span class="sxs-lookup"><span data-stu-id="74839-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="74839-115">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="74839-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74839-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="74839-116">See also</span></span>



[<span data-ttu-id="74839-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74839-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="74839-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="74839-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="74839-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="74839-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="74839-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74839-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

