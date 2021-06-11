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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436156"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="6bda7-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6bda7-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="6bda7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bda7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bda7-105">Cancela un registro de notificación establecido anteriormente para una entrada de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6bda7-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6bda7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6bda7-106">Parameters</span></span>

 <span data-ttu-id="6bda7-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="6bda7-107">_ulConnection_</span></span>
  
> <span data-ttu-id="6bda7-108">[in] Número de conexión que representa el registro que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="6bda7-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="6bda7-109">El _parámetro ulConnection_ debe contener un valor devuelto por una llamada anterior al [método IAddrBook::Advise.](iaddrbook-advise.md)</span><span class="sxs-lookup"><span data-stu-id="6bda7-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6bda7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bda7-110">Return value</span></span>

<span data-ttu-id="6bda7-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6bda7-111">S_OK</span></span> 
  
> <span data-ttu-id="6bda7-112">El registro se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="6bda7-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6bda7-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6bda7-113">Remarks</span></span>

<span data-ttu-id="6bda7-114">Los clientes llaman **al método Unadvise** para dejar de recibir notificaciones sobre los cambios en una entrada de libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="6bda7-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="6bda7-115">Cuando se cancela un registro de notificación, el proveedor de libreta de direcciones libera su puntero al receptor de avisos del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6bda7-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="6bda7-116">Sin embargo, la versión puede producirse durante la llamada **Unadvise** o en algún momento posterior, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="6bda7-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="6bda7-117">Cuando una notificación está en curso, la versión se retrasa hasta que el **método OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="6bda7-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6bda7-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bda7-118">See also</span></span>



[<span data-ttu-id="6bda7-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="6bda7-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="6bda7-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6bda7-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6bda7-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6bda7-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

