---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5d9a57cee371675493ba71b2df52b83941d34fc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817816"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="e6588-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="e6588-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="e6588-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6588-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6588-105">Proveedor de almacén de registros de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6588-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e6588-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6588-106">Parameters</span></span>

 <span data-ttu-id="e6588-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6588-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="e6588-108">[entrada] Reservado; debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="e6588-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6588-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6588-109">Return value</span></span>

<span data-ttu-id="e6588-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6588-110">S_OK</span></span> 
  
> <span data-ttu-id="e6588-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="e6588-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6588-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6588-112">Remarks</span></span>

<span data-ttu-id="e6588-113">Los proveedores de almacén de mensajes implementan el método **IMSLogon::Logoff** para forzar apagar un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e6588-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="e6588-114">Se denomina **IMSLogon::Logoff** en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6588-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="e6588-115">Mientras MAPI está cerrando un cliente después de una llamada al método [IMAPISession::Logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="e6588-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="e6588-116">Mientras MAPI está cerrando un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e6588-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="e6588-117">En este caso, se denomina **IMSLogon::Logoff** como parte de MAPI al procesar el método [IUnknown:: Release](http://msdn.microsoft.com/es-es/library/ms682317%28v=VS.85%29.aspx) del objeto de soporte técnico que el proveedor de almacenamiento de mensaje crea mientras está procesando un [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) o **IUnknown:: Versión** llamada al método en un objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e6588-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](http://msdn.microsoft.com/es-es/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e6588-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="e6588-118">See also</span></span>



[<span data-ttu-id="e6588-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="e6588-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="e6588-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6588-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="e6588-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="e6588-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="e6588-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="e6588-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="e6588-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e6588-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e6588-124">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6588-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

