---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329487"
---
# <a name="imapiformadvise"></a><span data-ttu-id="127ee-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="127ee-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="127ee-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="127ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="127ee-105">Registra un visor de formularios para notificaciones sobre eventos que afectan al formulario.</span><span class="sxs-lookup"><span data-stu-id="127ee-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="127ee-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="127ee-106">Parameters</span></span>

 <span data-ttu-id="127ee-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="127ee-107">_pAdvise_</span></span>
  
> <span data-ttu-id="127ee-108">a Un puntero a un objeto receptor de vista notificar para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="127ee-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="127ee-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="127ee-109">_pulConnection_</span></span>
  
> <span data-ttu-id="127ee-110">contempla Un puntero a un valor distinto de cero que representa un registro de notificación correcto.</span><span class="sxs-lookup"><span data-stu-id="127ee-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="127ee-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="127ee-111">Return value</span></span>

<span data-ttu-id="127ee-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="127ee-112">S_OK</span></span> 
  
> <span data-ttu-id="127ee-113">El registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="127ee-113">The registration was successful.</span></span>
    
<span data-ttu-id="127ee-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="127ee-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="127ee-115">El registro no se ha realizado correctamente debido a memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="127ee-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="127ee-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="127ee-116">Remarks</span></span>

<span data-ttu-id="127ee-117">Los visores de formularios llaman al método **IMAPIForm:: Advise** de un formulario para registrar la notificación cuando se producen cambios en el formulario.</span><span class="sxs-lookup"><span data-stu-id="127ee-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="127ee-118">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="127ee-118">Notes to implementers</span></span>

<span data-ttu-id="127ee-119">ConServe una copia del puntero View aconsejar Sink pasada en el parámetro _pAdvise_ para que pueda usarla para llamar al método [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) adecuado cuando se produzca un evento.</span><span class="sxs-lookup"><span data-stu-id="127ee-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="127ee-120">Llamar al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del receptor de vista para reconocer el puntero hasta que se cancele el registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="127ee-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="127ee-121">Establezca el contenido del parámetro _pulConnection_ en un número distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="127ee-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="127ee-122">Muchos formularios implementan un objeto auxiliar para controlar el registro y las notificaciones posteriores de eventos.</span><span class="sxs-lookup"><span data-stu-id="127ee-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="127ee-123">Para obtener más información sobre el proceso de notificación en general, vea [notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="127ee-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="127ee-124">Para obtener más información acerca de las notificaciones y los formularios, consulte [enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="127ee-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="127ee-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="127ee-125">See also</span></span>



[<span data-ttu-id="127ee-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="127ee-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="127ee-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="127ee-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="127ee-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="127ee-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="127ee-129">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="127ee-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="127ee-130">Enviar y recibir notificaciones de formulario</span><span class="sxs-lookup"><span data-stu-id="127ee-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

