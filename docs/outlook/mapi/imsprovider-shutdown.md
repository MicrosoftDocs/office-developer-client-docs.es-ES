---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438627"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="5b3a3-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="5b3a3-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="5b3a3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b3a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b3a3-105">Cierra un proveedor de almacén de mensajes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="5b3a3-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5b3a3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5b3a3-106">Parameters</span></span>

 <span data-ttu-id="5b3a3-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b3a3-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="5b3a3-108">[in] Reservado; debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="5b3a3-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b3a3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b3a3-109">Return value</span></span>

<span data-ttu-id="5b3a3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b3a3-110">S_OK</span></span> 
  
> <span data-ttu-id="5b3a3-111">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="5b3a3-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b3a3-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b3a3-112">Remarks</span></span>

<span data-ttu-id="5b3a3-113">MAPI llama al **método IMSProvider::Shutdown** justo antes de liberar el objeto de proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5b3a3-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="5b3a3-114">MAPI libera todos los objetos de inicio de sesión de un proveedor antes de llamar a **Shutdown** para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="5b3a3-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b3a3-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b3a3-115">See also</span></span>



[<span data-ttu-id="5b3a3-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b3a3-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

