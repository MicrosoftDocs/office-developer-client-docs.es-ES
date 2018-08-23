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
ms.openlocfilehash: bb373e4b666f44c432ac1b04c0449eb7f0408a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592937"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="3f69d-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="3f69d-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="3f69d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f69d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f69d-105">Se notifica al Visor de formulario que ha cargado un nuevo o un mensaje existente en un formulario.</span><span class="sxs-lookup"><span data-stu-id="3f69d-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="3f69d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f69d-106">Parameters</span></span>

<span data-ttu-id="3f69d-107">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3f69d-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3f69d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f69d-108">Return value</span></span>

<span data-ttu-id="3f69d-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f69d-109">S_OK</span></span> 
  
> <span data-ttu-id="3f69d-110">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3f69d-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f69d-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f69d-111">Remarks</span></span>

<span data-ttu-id="3f69d-112">Objetos de formulario llaman al método de **IMAPIViewAdviseSink::OnNewMessage** siempre que se carga un mensaje en un formulario mediante los métodos [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="3f69d-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3f69d-113">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="3f69d-113">Notes to implementers</span></span>

<span data-ttu-id="3f69d-114">Liberar su puntero al objeto form activo debido a que ya no apunta al mensaje que anteriormente estaba viendo el Visor.</span><span class="sxs-lookup"><span data-stu-id="3f69d-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="3f69d-115">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3f69d-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f69d-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3f69d-116">See also</span></span>



[<span data-ttu-id="3f69d-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f69d-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="3f69d-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="3f69d-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="3f69d-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="3f69d-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="3f69d-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f69d-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

