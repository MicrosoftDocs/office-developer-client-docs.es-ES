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
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335707"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="6b1ca-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6b1ca-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="6b1ca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b1ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b1ca-105">Cancela el envío de notificaciones previamente configuradas con una llamada al método [IMAPISession::Advise.](imapisession-advise.md)</span><span class="sxs-lookup"><span data-stu-id="6b1ca-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6b1ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b1ca-106">Parameters</span></span>

 <span data-ttu-id="6b1ca-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="6b1ca-107">_ulConnection_</span></span>
  
> <span data-ttu-id="6b1ca-108">[entrada] Un número de conexión asociado a un registro de notificación activo.</span><span class="sxs-lookup"><span data-stu-id="6b1ca-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="6b1ca-109">El valor de  _ulConnection_ debe haber sido devuelto por una llamada anterior a **IMAPISession::Advise**.</span><span class="sxs-lookup"><span data-stu-id="6b1ca-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b1ca-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b1ca-110">Return value</span></span>

<span data-ttu-id="6b1ca-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b1ca-111">S_OK</span></span> 
  
> <span data-ttu-id="6b1ca-112">El registro se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b1ca-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b1ca-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b1ca-113">Remarks</span></span>

<span data-ttu-id="6b1ca-114">El **método IMAPISession::Unadvise** cancela un registro para la notificación.</span><span class="sxs-lookup"><span data-stu-id="6b1ca-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="6b1ca-115">**Unadvise** libera su puntero al receptor de avisos del autor de la llamada, que recibió en la llamada **advise** usada para el registro.</span><span class="sxs-lookup"><span data-stu-id="6b1ca-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="6b1ca-116">Por lo general, **Unadvise llama** al método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del receptor de avisos durante la **llamada Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="6b1ca-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="6b1ca-117">Sin embargo, si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de aviso, la llamada **Release** se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="6b1ca-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b1ca-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6b1ca-118">See also</span></span>



[<span data-ttu-id="6b1ca-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6b1ca-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6b1ca-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="6b1ca-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="6b1ca-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b1ca-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

