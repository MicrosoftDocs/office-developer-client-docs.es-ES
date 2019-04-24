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
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329473"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="8f2b0-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8f2b0-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="8f2b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f2b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f2b0-105">Cancela un registro de notificaciones con un visor de formularios establecido previamente mediante una llamada a [IMAPIForm:: Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="8f2b0-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8f2b0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8f2b0-106">Parameters</span></span>

 <span data-ttu-id="8f2b0-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="8f2b0-107">_ulConnection_</span></span>
  
> <span data-ttu-id="8f2b0-108">a Un número de conexión que identifica el registro de notificaciones que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="8f2b0-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f2b0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f2b0-109">Return value</span></span>

<span data-ttu-id="8f2b0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f2b0-110">S_OK</span></span> 
  
> <span data-ttu-id="8f2b0-111">Se canceló el registro.</span><span class="sxs-lookup"><span data-stu-id="8f2b0-111">The registration was canceled.</span></span>
    
<span data-ttu-id="8f2b0-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8f2b0-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="8f2b0-113">El número de conexión pasado en el parámetro _ulConnection_ no representa un registro válido.</span><span class="sxs-lookup"><span data-stu-id="8f2b0-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8f2b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f2b0-114">Remarks</span></span>

<span data-ttu-id="8f2b0-115">Los visores de formularios llaman al método **IMAPIForm:: Unadvise** para cancelar un registro para la notificación que se estableció por primera vez mediante una llamada al método **IMAPIForm:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="8f2b0-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8f2b0-116">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="8f2b0-116">Notes to implementers</span></span>

<span data-ttu-id="8f2b0-117">DesCartar el puntero que está reteniendo al receptor de la vista de notificar del formulario del visor llamando a su método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8f2b0-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="8f2b0-118">Por lo general, se llama a **Release** durante la llamada a **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="8f2b0-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="8f2b0-119">Sin embargo, si hay otro subproceso que llama a uno de los métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) para el receptor View Advise, retrase la llamada a **Release** hasta que se devuelva el método **IMAPIViewAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="8f2b0-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f2b0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f2b0-120">See also</span></span>



[<span data-ttu-id="8f2b0-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="8f2b0-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="8f2b0-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f2b0-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="8f2b0-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f2b0-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

