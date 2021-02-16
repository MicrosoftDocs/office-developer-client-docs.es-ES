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
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317279"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="096b4-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="096b4-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="096b4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="096b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="096b4-105">Quita el registro de un objeto para la notificación de los cambios del almacén de mensajes establecidos anteriormente mediante una llamada al método [IMSLogon::Advise.](imslogon-advise.md)</span><span class="sxs-lookup"><span data-stu-id="096b4-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="096b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="096b4-106">Parameters</span></span>

 <span data-ttu-id="096b4-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="096b4-107">_ulConnection_</span></span>
  
> <span data-ttu-id="096b4-108">[entrada] El número de la conexión de registro devuelta por una llamada a **IMSLogon::Advise**.</span><span class="sxs-lookup"><span data-stu-id="096b4-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="096b4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="096b4-109">Return value</span></span>

<span data-ttu-id="096b4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="096b4-110">S_OK</span></span> 
  
> <span data-ttu-id="096b4-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="096b4-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="096b4-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="096b4-112">Remarks</span></span>

<span data-ttu-id="096b4-113">Los proveedores de almacén de mensajes implementan el método **IMSLogon::Unadvise** para liberar el puntero al objeto receptor de aviso pasado en el parámetro  _lpAdviseSink_ en la llamada anterior a **IMSLogon::Advise,** cancelando así un registro de notificación.</span><span class="sxs-lookup"><span data-stu-id="096b4-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="096b4-114">Como parte de descartar el puntero al objeto receptor de aviso, se llama al método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del objeto.</span><span class="sxs-lookup"><span data-stu-id="096b4-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="096b4-115">Por lo general, se llama a **Release** durante la **llamada Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="096b4-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="096b4-116">Sin embargo, si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor de aviso, la llamada **release** se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="096b4-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="096b4-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="096b4-117">See also</span></span>



[<span data-ttu-id="096b4-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="096b4-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="096b4-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="096b4-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="096b4-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="096b4-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

