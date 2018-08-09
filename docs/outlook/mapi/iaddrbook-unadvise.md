---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817153"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="b4ebd-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b4ebd-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="b4ebd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4ebd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4ebd-105">Cancela un registro de notificación establecido anteriormente para una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b4ebd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4ebd-106">Parameters</span></span>

 <span data-ttu-id="b4ebd-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="b4ebd-107">_ulConnection_</span></span>
  
> <span data-ttu-id="b4ebd-108">[entrada] Un número de conexión que representa el registro que se cancelen.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="b4ebd-109">El parámetro _ulConnection_ debe contener un valor devuelto por una llamada anterior al método [IAddrBook::Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ebd-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b4ebd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4ebd-110">Return value</span></span>

<span data-ttu-id="b4ebd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4ebd-111">S_OK</span></span> 
  
> <span data-ttu-id="b4ebd-112">El registro se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4ebd-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4ebd-113">Remarks</span></span>

<span data-ttu-id="b4ebd-114">Los clientes de llaman al método **Unadvise** para dejar de recibir notificaciones sobre los cambios realizados en una entrada de la libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="b4ebd-115">Cuando se cancela un registro de la notificación, las versiones de proveedor de la libreta de direcciones su puntero al autor de la llamada del aviso receptor.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="b4ebd-116">Sin embargo, la versión puede producirse durante la llamada **Unadvise** o en algún momento posterior, si es otro subproceso en el proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ebd-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="b4ebd-117">Cuando una notificación está en progreso, la versión se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4ebd-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4ebd-118">See also</span></span>



[<span data-ttu-id="b4ebd-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="b4ebd-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="b4ebd-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b4ebd-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b4ebd-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b4ebd-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

