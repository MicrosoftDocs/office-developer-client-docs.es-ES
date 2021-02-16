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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430234"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="89f30-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="89f30-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="89f30-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89f30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89f30-105">Cancela el envío de notificaciones previamente configuradas con una llamada al método [IMAPITable::Advise.](imapitable-advise.md)</span><span class="sxs-lookup"><span data-stu-id="89f30-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="89f30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89f30-106">Parameters</span></span>

 <span data-ttu-id="89f30-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="89f30-107">_ulConnection_</span></span>
  
> <span data-ttu-id="89f30-108">[entrada] El número de la conexión de registro devuelta por una llamada a [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="89f30-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="89f30-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89f30-109">Return value</span></span>

<span data-ttu-id="89f30-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="89f30-110">S_OK</span></span> 
  
> <span data-ttu-id="89f30-111">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="89f30-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89f30-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89f30-112">Remarks</span></span>

<span data-ttu-id="89f30-113">Utilice el método **IMAPITable::Unadvise** para liberar el puntero al objeto receptor de aviso pasado en el parámetro  _lpAdviseSink_ en la llamada anterior a **IMAPITable::Advise**, cancelando así un registro de notificación.</span><span class="sxs-lookup"><span data-stu-id="89f30-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="89f30-114">Como parte de descartar el puntero al objeto receptor de aviso, se llama al método **IUnknown::Release** del objeto.</span><span class="sxs-lookup"><span data-stu-id="89f30-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="89f30-115">Por lo general, se llama a **Release** durante la llamada **Unadvise,** pero si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el receptor de avisos, la llamada **release** se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="89f30-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="89f30-116">Para obtener más información sobre el proceso de notificación, vea [Notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="89f30-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="89f30-117">Para obtener información específica acerca de la notificación de tabla, vea [Acerca de las notificaciones de tabla](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="89f30-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="89f30-118">Para obtener información acerca del uso **de los métodos IMAPISupport** para admitir notificaciones, vea [Notificación de eventos auxiliares.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="89f30-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="89f30-119">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="89f30-119">MFCMAPI reference</span></span>

<span data-ttu-id="89f30-120">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="89f30-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="89f30-121">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="89f30-121">**File**</span></span>|<span data-ttu-id="89f30-122">**Función**</span><span class="sxs-lookup"><span data-stu-id="89f30-122">**Function**</span></span>|<span data-ttu-id="89f30-123">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="89f30-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89f30-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="89f30-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="89f30-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="89f30-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="89f30-126">MFCMAPI usa el **método IMAPITable::Unadvise** para cancelar las notificaciones de la tabla.</span><span class="sxs-lookup"><span data-stu-id="89f30-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89f30-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="89f30-127">See also</span></span>



[<span data-ttu-id="89f30-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="89f30-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="89f30-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="89f30-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="89f30-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89f30-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="89f30-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="89f30-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

