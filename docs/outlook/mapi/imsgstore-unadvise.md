---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309726"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="cdbfc-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="cdbfc-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="cdbfc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdbfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdbfc-105">Cancela el envío de notificaciones previamente configurado con una llamada al método [IMsgStore:: Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="cdbfc-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="cdbfc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cdbfc-106">Parameters</span></span>

 <span data-ttu-id="cdbfc-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="cdbfc-107">_ulConnection_</span></span>
  
> <span data-ttu-id="cdbfc-108">a El número de conexión asociado con un registro de notificación activo.</span><span class="sxs-lookup"><span data-stu-id="cdbfc-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="cdbfc-109">El valor de _ulConnection_ debe haber sido devuelto por una llamada anterior al método **IMsgStore:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="cdbfc-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cdbfc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdbfc-110">Return value</span></span>

<span data-ttu-id="cdbfc-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cdbfc-111">S_OK</span></span> 
  
> <span data-ttu-id="cdbfc-112">El registro se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="cdbfc-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cdbfc-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cdbfc-113">Remarks</span></span>

<span data-ttu-id="cdbfc-114">El método **IMsgStore:: Unadvise** cancela un registro para la notificación.</span><span class="sxs-lookup"><span data-stu-id="cdbfc-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="cdbfc-115">No **aconseja** liberar su puntero al receptor de notificaciones del autor de la llamada, que recibió en la llamada de **aviso** utilizada para el registro.</span><span class="sxs-lookup"><span data-stu-id="cdbfc-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="cdbfc-116">Generalmente, **Unadvise** llama al método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del receptor de notificaciones durante \*\*\*\* la llamada a Unadvise.</span><span class="sxs-lookup"><span data-stu-id="cdbfc-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="cdbfc-117">Sin embargo, si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) del receptor de notificación, la llamada de **liberación** se retrasa hasta que se devuelva el método **BENOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="cdbfc-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cdbfc-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdbfc-118">See also</span></span>



[<span data-ttu-id="cdbfc-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="cdbfc-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="cdbfc-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="cdbfc-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="cdbfc-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cdbfc-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

