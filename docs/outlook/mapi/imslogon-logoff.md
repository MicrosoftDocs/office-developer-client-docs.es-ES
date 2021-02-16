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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348877"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="94d26-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="94d26-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="94d26-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94d26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94d26-105">Cierra la sesión de un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94d26-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="94d26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94d26-106">Parameters</span></span>

 <span data-ttu-id="94d26-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="94d26-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="94d26-108">[entrada] Reservado; debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="94d26-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94d26-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94d26-109">Return value</span></span>

<span data-ttu-id="94d26-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="94d26-110">S_OK</span></span> 
  
> <span data-ttu-id="94d26-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="94d26-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94d26-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94d26-112">Remarks</span></span>

<span data-ttu-id="94d26-113">Los proveedores de al almacenamiento de mensajes implementan el método **IMSLogon::Logoff** para cerrar por la fuerza un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94d26-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="94d26-114">**Se llama a IMSLogon::Logoff** en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="94d26-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="94d26-115">Mientras MAPI cierra la sesión de un cliente después de una llamada al método [IMAPISession::Logoff.](imapisession-logoff.md)</span><span class="sxs-lookup"><span data-stu-id="94d26-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="94d26-116">Mientras MAPI está registrando un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94d26-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="94d26-117">En este caso, se llama a **IMSLogon::Logoff** como parte del procesamiento de MAPI del método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del objeto de soporte técnico que crea el proveedor del almacén de mensajes mientras procesa una llamada al método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) o **IUnknown::Release** en un objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94d26-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="94d26-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94d26-118">See also</span></span>



[<span data-ttu-id="94d26-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="94d26-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="94d26-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94d26-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="94d26-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="94d26-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="94d26-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="94d26-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="94d26-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="94d26-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="94d26-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94d26-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

