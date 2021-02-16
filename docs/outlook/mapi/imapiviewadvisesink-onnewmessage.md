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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419607"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="c7dea-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="c7dea-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="c7dea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7dea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7dea-105">Notifica al visor de formularios que se ha cargado un mensaje nuevo o existente en un formulario.</span><span class="sxs-lookup"><span data-stu-id="c7dea-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="c7dea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7dea-106">Parameters</span></span>

<span data-ttu-id="c7dea-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c7dea-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c7dea-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7dea-108">Return value</span></span>

<span data-ttu-id="c7dea-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7dea-109">S_OK</span></span> 
  
> <span data-ttu-id="c7dea-110">La notificación se ha publicado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c7dea-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7dea-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7dea-111">Remarks</span></span>

<span data-ttu-id="c7dea-112">Los objetos de formulario llaman al método **IMAPIViewAdviseSink::OnNewMessage** siempre que se carga un mensaje en un formulario mediante el método [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load.](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="c7dea-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c7dea-113">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="c7dea-113">Notes to implementers</span></span>

<span data-ttu-id="c7dea-114">Libere el puntero activo al objeto de formulario porque ya no apunta al mensaje que el visor estaba viendo anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c7dea-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="c7dea-115">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="c7dea-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7dea-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c7dea-116">See also</span></span>



[<span data-ttu-id="c7dea-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7dea-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="c7dea-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="c7dea-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="c7dea-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="c7dea-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="c7dea-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7dea-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

