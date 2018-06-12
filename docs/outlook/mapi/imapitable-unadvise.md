---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e9d8565cfaa17764e92bddafb29e744d23872515
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817622"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="170ed-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="170ed-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="170ed-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="170ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="170ed-105">Cancela el envío de notificaciones configuradas previamente con una llamada al método [IMAPITable::Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="170ed-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="170ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="170ed-106">Parameters</span></span>

 <span data-ttu-id="170ed-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="170ed-107">_ulConnection_</span></span>
  
> <span data-ttu-id="170ed-108">[entrada] El número de la conexión de registro devuelto por una llamada a [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="170ed-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="170ed-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="170ed-109">Return value</span></span>

<span data-ttu-id="170ed-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="170ed-110">S_OK</span></span> 
  
> <span data-ttu-id="170ed-111">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="170ed-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="170ed-112">Notas</span><span class="sxs-lookup"><span data-stu-id="170ed-112">Remarks</span></span>

<span data-ttu-id="170ed-113">Use el método **IMAPITable::Unadvise** para liberar el puntero al objeto receptor advise pasado en el parámetro _lpAdviseSink_ en la llamada anterior a **IMAPITable::Advise**, con lo que se cancela un registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="170ed-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="170ed-114">Como parte de descartar el puntero al objeto receptor advise, se llama al método del objeto **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="170ed-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="170ed-115">Por lo general, se llama a **versión** durante la llamada **Unadvise** , pero si es otro subproceso en el proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el receptor de notificaciones, la llamada de la **versión** se retrasa hasta el **OnNotify** Devuelve el método.</span><span class="sxs-lookup"><span data-stu-id="170ed-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="170ed-116">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="170ed-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="170ed-117">Para obtener información específica acerca de la notificación de la tabla, vea [Acerca de las notificaciones de tabla](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="170ed-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="170ed-118">Para obtener información acerca del uso de los métodos **IMAPISupport** para admitir la notificación, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="170ed-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="170ed-119">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="170ed-119">MFCMAPI reference</span></span>

<span data-ttu-id="170ed-120">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="170ed-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="170ed-121">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="170ed-121">**File**</span></span>|<span data-ttu-id="170ed-122">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="170ed-122">**Function**</span></span>|<span data-ttu-id="170ed-123">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="170ed-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="170ed-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="170ed-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="170ed-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="170ed-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="170ed-126">MFCMAPI utiliza el método **IMAPITable::Unadvise** para cancelar las notificaciones para la tabla.</span><span class="sxs-lookup"><span data-stu-id="170ed-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="170ed-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="170ed-127">See also</span></span>



[<span data-ttu-id="170ed-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="170ed-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="170ed-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="170ed-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="170ed-130">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="170ed-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="170ed-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="170ed-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

