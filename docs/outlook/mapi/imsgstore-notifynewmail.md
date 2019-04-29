---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: a8ec06fd0401a129e08a06acdb1c18785f90d4a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431781"
---
# <a name="imsgstorenotifynewmail"></a><span data-ttu-id="e8e0b-103">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="e8e0b-103">IMsgStore::NotifyNewMail</span></span>

  
  
<span data-ttu-id="e8e0b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8e0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8e0b-105">Informa el almac�n de mensajes que ha llegado un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="e8e0b-105">Informs the message store that a new message has arrived.</span></span> <span data-ttu-id="e8e0b-106">Se llama a este m�todo s�lo por la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="e8e0b-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a><span data-ttu-id="e8e0b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e8e0b-107">Parameters</span></span>

 <span data-ttu-id="e8e0b-108">_lpNotification_</span><span class="sxs-lookup"><span data-stu-id="e8e0b-108">_lpNotification_</span></span>
  
> <span data-ttu-id="e8e0b-109">[entrada] Un puntero a una estructura de [notificaci�n](notification.md) que describa la notificaci�n de mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="e8e0b-109">[in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8e0b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8e0b-110">Return value</span></span>

<span data-ttu-id="e8e0b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8e0b-111">S_OK</span></span> 
  
> <span data-ttu-id="e8e0b-112">El almac�n de mensajes notific� correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8e0b-112">The message store was successfully notified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8e0b-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8e0b-113">Remarks</span></span>

<span data-ttu-id="e8e0b-114">Se llama al m�todo de **IMsgStore::NotifyNewMail** por la cola MAPI para notificar el almac�n de mensajes que est� listo para la entrega de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e8e0b-114">The **IMsgStore::NotifyNewMail** method is called by the MAPI spooler to inform the message store that a message is ready for delivery.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e8e0b-115">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="e8e0b-115">Notes to implementers</span></span>

<span data-ttu-id="e8e0b-p102">Cuando se llama a **NotifyNewMail**, env�e una notificaci�n de correo nuevo a todos los clientes registrados. Puede enviar la notificaci�n mediante una llamada a [IMAPISupport::Notify](imapisupport-notify.md), si opta por utilizar los m�todos del objeto de soporte t�cnico, o mediante su propia implementaci�n. Un cliente registrado es uno que se llama [IMsgStore::Advise](imsgstore-advise.md) y se establece el par�metro  _lpEntryID_ en NULL y el par�metro  _ulEventMask_ a  _fnevNewMail_.</span><span class="sxs-lookup"><span data-stu-id="e8e0b-p102">When **NotifyNewMail** is called, send a new mail notification to all registered clients. You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation. A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_.</span></span> 
  
<span data-ttu-id="e8e0b-p103">No puede modificar ni liberar la memoria para la estructura de [notificaci�n](notification.md) que describe la notificaci�n de correo nuevo. Copie la estructura de **NOTIFICATION** mediante una llamada a la funci�n de utilidad [ScCopyNotifications](sccopynotifications.md) para hacer uso de la informaci�n de sus miembros.</span><span class="sxs-lookup"><span data-stu-id="e8e0b-p103">Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification. Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8e0b-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="e8e0b-121">See also</span></span>



[<span data-ttu-id="e8e0b-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="e8e0b-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="e8e0b-123">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="e8e0b-123">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
  
[<span data-ttu-id="e8e0b-124">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="e8e0b-124">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="e8e0b-125">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="e8e0b-125">ScCopyNotifications</span></span>](sccopynotifications.md)
  
[<span data-ttu-id="e8e0b-126">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e8e0b-126">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

