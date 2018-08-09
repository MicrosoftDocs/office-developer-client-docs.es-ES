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
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817806"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="d0a37-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="d0a37-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="d0a37-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0a37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0a37-105">Cierra un proveedor de almacén de mensajes de una forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="d0a37-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d0a37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0a37-106">Parameters</span></span>

 <span data-ttu-id="d0a37-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0a37-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="d0a37-108">[entrada] Reservado; debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="d0a37-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0a37-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0a37-109">Return value</span></span>

<span data-ttu-id="d0a37-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0a37-110">S_OK</span></span> 
  
> <span data-ttu-id="d0a37-111">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d0a37-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0a37-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0a37-112">Remarks</span></span>

<span data-ttu-id="d0a37-113">MAPI, llama al método **IMSProvider::Shutdown** justo antes de liberar el objeto de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d0a37-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="d0a37-114">MAPI libera todos los objetos de inicio de sesión para un proveedor antes de llamar a **apagado** de ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="d0a37-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0a37-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0a37-115">See also</span></span>



[<span data-ttu-id="d0a37-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0a37-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

