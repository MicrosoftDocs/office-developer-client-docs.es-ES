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
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817252"
---
# <a name="imapiformadvise"></a><span data-ttu-id="0b4e6-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="0b4e6-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="0b4e6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b4e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b4e6-105">Registra un visor de formulario para las notificaciones sobre los eventos que afectan a la forma.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0b4e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b4e6-106">Parameters</span></span>

 <span data-ttu-id="0b4e6-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="0b4e6-107">_pAdvise_</span></span>
  
> <span data-ttu-id="0b4e6-108">[entrada] Un puntero a una vista de aviso objeto receptor para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="0b4e6-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="0b4e6-109">_pulConnection_</span></span>
  
> <span data-ttu-id="0b4e6-110">[out] Un puntero a un valor distinto de cero que representa un registro de la notificación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0b4e6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b4e6-111">Return value</span></span>

<span data-ttu-id="0b4e6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b4e6-112">S_OK</span></span> 
  
> <span data-ttu-id="0b4e6-113">El registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-113">The registration was successful.</span></span>
    
<span data-ttu-id="0b4e6-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="0b4e6-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="0b4e6-115">El registro no tuvo éxito debido a memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b4e6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b4e6-116">Remarks</span></span>

<span data-ttu-id="0b4e6-117">Visores de formulario llame al método de **IMAPIForm::Advise** de un formulario para registrarse para la notificación cuando se producen cambios al formulario.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0b4e6-118">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="0b4e6-118">Notes to implementers</span></span>

<span data-ttu-id="0b4e6-119">Mantener una copia de la vista de aviso puntero receptor pasa en el parámetro _pAdvise_ de forma que puede usar para llamar al método apropiado de [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) cuando se produce un evento.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="0b4e6-120">Método de [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) del receptor para conservar el puntero hasta que se cancele el registro de la notificación de aviso de llamada de la vista.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-120">Call the view advise sink's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="0b4e6-121">Establecer el contenido del parámetro _pulConnection_ a un número distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="0b4e6-122">Muchas formas implementan un objeto auxiliar para controlar el registro y la notificación posterior de eventos.</span><span class="sxs-lookup"><span data-stu-id="0b4e6-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="0b4e6-123">Para obtener más información sobre el proceso de notificación en general, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0b4e6-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="0b4e6-124">Para obtener más información acerca de la notificación y formularios, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0b4e6-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b4e6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b4e6-125">See also</span></span>



[<span data-ttu-id="0b4e6-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0b4e6-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="0b4e6-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b4e6-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="0b4e6-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b4e6-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="0b4e6-129">Notificación de eventos de MAPI</span><span class="sxs-lookup"><span data-stu-id="0b4e6-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="0b4e6-130">Enviar y recibir notificaciones de formulario</span><span class="sxs-lookup"><span data-stu-id="0b4e6-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

