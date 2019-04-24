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
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328794"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="01e79-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="01e79-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="01e79-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01e79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01e79-105">Notifica al visor de formularios que se ha cargado un mensaje nuevo o existente en un formulario.</span><span class="sxs-lookup"><span data-stu-id="01e79-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="01e79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01e79-106">Parameters</span></span>

<span data-ttu-id="01e79-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01e79-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="01e79-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01e79-108">Return value</span></span>

<span data-ttu-id="01e79-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="01e79-109">S_OK</span></span> 
  
> <span data-ttu-id="01e79-110">La notificación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="01e79-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01e79-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01e79-111">Remarks</span></span>

<span data-ttu-id="01e79-112">Los objetos de formulario llaman al método **IMAPIViewAdviseSink:: OnNewMessage** cada vez que se carga un mensaje en un formulario con el método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) o [IPersistMessage:: Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="01e79-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="01e79-113">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="01e79-113">Notes to implementers</span></span>

<span data-ttu-id="01e79-114">Libere el puntero activo al objeto de formulario porque ya no señala al mensaje que el visor había visto anteriormente.</span><span class="sxs-lookup"><span data-stu-id="01e79-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="01e79-115">Para obtener más información acerca de las notificaciones de formulario, vea [enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="01e79-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01e79-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="01e79-116">See also</span></span>



[<span data-ttu-id="01e79-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01e79-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="01e79-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="01e79-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="01e79-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="01e79-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="01e79-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01e79-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

