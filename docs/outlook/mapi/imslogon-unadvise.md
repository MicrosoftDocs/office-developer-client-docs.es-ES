---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 34c15ca4f7d81eeeee71fb0cb7e31085c75e5492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817832"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="4dc43-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4dc43-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="4dc43-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4dc43-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4dc43-105">Quita el registro de un objeto de notificación de cambios del almacén de mensajes ha establecido previamente mediante una llamada al método [IMSLogon::Advise](imslogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="4dc43-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4dc43-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dc43-106">Parameters</span></span>

 <span data-ttu-id="4dc43-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="4dc43-107">_ulConnection_</span></span>
  
> <span data-ttu-id="4dc43-108">[entrada] El número de la conexión de registro devuelto por una llamada a **IMSLogon::Advise**.</span><span class="sxs-lookup"><span data-stu-id="4dc43-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4dc43-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dc43-109">Return value</span></span>

<span data-ttu-id="4dc43-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4dc43-110">S_OK</span></span> 
  
> <span data-ttu-id="4dc43-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4dc43-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4dc43-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4dc43-112">Remarks</span></span>

<span data-ttu-id="4dc43-113">Almacén de mensajes implementan los proveedores el método **IMSLogon::Unadvise** para liberar el puntero al objeto receptor advise pasado en el parámetro _lpAdviseSink_ en la llamada anterior a **IMSLogon::Advise**, con lo que se cancela una notificación en el registro.</span><span class="sxs-lookup"><span data-stu-id="4dc43-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="4dc43-114">Como parte de descartar el puntero al objeto receptor advise, se llama al método del objeto [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4dc43-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="4dc43-115">Por lo general, se llama a **versión** durante la llamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="4dc43-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="4dc43-116">Sin embargo, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise, la llamada de la **versión** se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="4dc43-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4dc43-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dc43-117">See also</span></span>



[<span data-ttu-id="4dc43-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4dc43-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4dc43-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="4dc43-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="4dc43-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4dc43-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)
