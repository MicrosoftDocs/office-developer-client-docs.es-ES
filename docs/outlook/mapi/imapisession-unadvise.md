---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3b582b48773b9f6f1a6f46f9c0e4c6dcb9782b86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592069"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="47851-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="47851-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="47851-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47851-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47851-105">Cancela el envío de notificaciones configuradas previamente con una llamada al método [IMAPISession::Advise](imapisession-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="47851-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="47851-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47851-106">Parameters</span></span>

 <span data-ttu-id="47851-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="47851-107">_ulConnection_</span></span>
  
> <span data-ttu-id="47851-108">[entrada] Un número de conexión asociado con un registro activo de notificación.</span><span class="sxs-lookup"><span data-stu-id="47851-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="47851-109">El valor de _ulConnection_ debe se han devuelto por una llamada anterior a **IMAPISession::Advise**.</span><span class="sxs-lookup"><span data-stu-id="47851-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47851-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47851-110">Return value</span></span>

<span data-ttu-id="47851-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="47851-111">S_OK</span></span> 
  
> <span data-ttu-id="47851-112">El registro se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="47851-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47851-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47851-113">Remarks</span></span>

<span data-ttu-id="47851-114">El método **IMAPISession::Unadvise** cancela un registro de notificación.</span><span class="sxs-lookup"><span data-stu-id="47851-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="47851-115">Versiones de **Unadvise** su puntero al autor de la llamada de aviso receptor, que recibe en la llamada **Advise** utilizan para el registro.</span><span class="sxs-lookup"><span data-stu-id="47851-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="47851-116">Por lo general, **Unadvise** llama a método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) del receptor de notificaciones durante la llamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="47851-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="47851-117">Sin embargo, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de notificaciones, la llamada de la **versión** se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="47851-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47851-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="47851-118">See also</span></span>



[<span data-ttu-id="47851-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="47851-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="47851-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="47851-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="47851-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="47851-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

