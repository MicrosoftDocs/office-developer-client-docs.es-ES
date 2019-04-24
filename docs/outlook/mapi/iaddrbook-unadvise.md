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
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286986"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="3b16b-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3b16b-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="3b16b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b16b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b16b-105">Cancela un registro de notificaciones previamente establecido para una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3b16b-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3b16b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3b16b-106">Parameters</span></span>

 <span data-ttu-id="3b16b-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="3b16b-107">_ulConnection_</span></span>
  
> <span data-ttu-id="3b16b-108">a Un número de conexión que representa el registro que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="3b16b-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="3b16b-109">El parámetro _ulConnection_ debe contener un valor devuelto por una llamada anterior al método [IAddrBook:: Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="3b16b-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3b16b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b16b-110">Return value</span></span>

<span data-ttu-id="3b16b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b16b-111">S_OK</span></span> 
  
> <span data-ttu-id="3b16b-112">El registro se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="3b16b-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b16b-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b16b-113">Remarks</span></span>

<span data-ttu-id="3b16b-114">Los clientes llaman al método **Unadvise** para dejar de recibir notificaciones sobre los cambios realizados en una determinada entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3b16b-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="3b16b-115">Cuando se cancela un registro de notificación, el proveedor de la libreta de direcciones libera su puntero al receptor de notificaciones del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3b16b-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="3b16b-116">Sin embargo, la liberación se puede producir durante la llamada a **Unadvise** o en algún momento posterior si hay otro subproceso en el proceso de llamada al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b16b-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="3b16b-117">Cuando hay una notificación en curso, la liberación se retrasa hasta que se devuelva el método **BENOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="3b16b-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b16b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b16b-118">See also</span></span>



[<span data-ttu-id="3b16b-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="3b16b-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="3b16b-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3b16b-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="3b16b-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3b16b-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

