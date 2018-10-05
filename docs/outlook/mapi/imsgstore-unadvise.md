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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398020"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="8cffa-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8cffa-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="8cffa-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cffa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cffa-105">Cancela el envío de notificaciones configuradas previamente con una llamada al método [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="8cffa-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8cffa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cffa-106">Parameters</span></span>

 <span data-ttu-id="8cffa-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="8cffa-107">_ulConnection_</span></span>
  
> <span data-ttu-id="8cffa-108">[entrada] El número de conexión asociado con un registro activo de notificación.</span><span class="sxs-lookup"><span data-stu-id="8cffa-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="8cffa-109">El valor de _ulConnection_ debe se han devuelto por una llamada anterior al método **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="8cffa-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8cffa-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cffa-110">Return value</span></span>

<span data-ttu-id="8cffa-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cffa-111">S_OK</span></span> 
  
> <span data-ttu-id="8cffa-112">El registro se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="8cffa-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8cffa-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cffa-113">Remarks</span></span>

<span data-ttu-id="8cffa-114">El método **IMsgStore::Unadvise** cancela un registro de notificación.</span><span class="sxs-lookup"><span data-stu-id="8cffa-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="8cffa-115">Versiones de **Unadvise** su puntero al autor de la llamada de aviso receptor, que recibe en la llamada **Advise** utilizan para el registro.</span><span class="sxs-lookup"><span data-stu-id="8cffa-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="8cffa-116">Por lo general, **Unadvise** llama a método de [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del receptor de notificaciones durante la llamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="8cffa-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="8cffa-117">Sin embargo, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de notificaciones, la llamada de la **versión** se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="8cffa-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8cffa-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cffa-118">See also</span></span>



[<span data-ttu-id="8cffa-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8cffa-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="8cffa-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="8cffa-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="8cffa-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8cffa-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

