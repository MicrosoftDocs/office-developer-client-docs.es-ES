---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 33287d8ac6b1faeba8b8746a95850f6fd1c37462
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579490"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="4d4e7-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4d4e7-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="4d4e7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d4e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d4e7-105">Cancela un registro para las notificaciones con un visor de formulario que se ha establecido previamente mediante una llamada a [IMAPIForm::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="4d4e7-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4d4e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d4e7-106">Parameters</span></span>

 <span data-ttu-id="4d4e7-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="4d4e7-107">_ulConnection_</span></span>
  
> <span data-ttu-id="4d4e7-108">[entrada] Un número de conexión que identifica el registro de notificación que se cancelen.</span><span class="sxs-lookup"><span data-stu-id="4d4e7-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d4e7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d4e7-109">Return value</span></span>

<span data-ttu-id="4d4e7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d4e7-110">S_OK</span></span> 
  
> <span data-ttu-id="4d4e7-111">Se canceló el registro.</span><span class="sxs-lookup"><span data-stu-id="4d4e7-111">The registration was canceled.</span></span>
    
<span data-ttu-id="4d4e7-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4d4e7-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="4d4e7-113">El número de conexión que se pasa en el parámetro _ulConnection_ no representan un registro válido.</span><span class="sxs-lookup"><span data-stu-id="4d4e7-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4d4e7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d4e7-114">Remarks</span></span>

<span data-ttu-id="4d4e7-115">Visores de formulario llamar al método **IMAPIForm::Unadvise** para cancelar un registro de notificación que estableció por primera vez llamando al método **IMAPIForm::Advise** .</span><span class="sxs-lookup"><span data-stu-id="4d4e7-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4d4e7-116">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="4d4e7-116">Notes to implementers</span></span>

<span data-ttu-id="4d4e7-117">Descartar el puntero que se mantiene a la vista del Visor de formulario de aviso receptor llamando a su método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4d4e7-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="4d4e7-118">Por lo general, se llama a **versión** durante la llamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="4d4e7-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="4d4e7-119">Sin embargo, si otro subproceso está en el proceso de una llamada a uno de los métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) para la vista de aviso receptor, retrasar la llamada **versión** hasta que el método **IMAPIViewAdviseSink** devuelve.</span><span class="sxs-lookup"><span data-stu-id="4d4e7-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d4e7-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4d4e7-120">See also</span></span>



[<span data-ttu-id="4d4e7-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="4d4e7-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="4d4e7-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d4e7-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="4d4e7-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d4e7-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

