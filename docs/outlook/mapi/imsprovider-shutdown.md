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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317265"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="d41bb-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="d41bb-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="d41bb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d41bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d41bb-105">Cierra un proveedor de almacenamiento de mensajes de manera ordenada.</span><span class="sxs-lookup"><span data-stu-id="d41bb-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d41bb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d41bb-106">Parameters</span></span>

 <span data-ttu-id="d41bb-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d41bb-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="d41bb-108">a Reserve debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="d41bb-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d41bb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d41bb-109">Return value</span></span>

<span data-ttu-id="d41bb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d41bb-110">S_OK</span></span> 
  
> <span data-ttu-id="d41bb-111">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d41bb-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d41bb-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d41bb-112">Remarks</span></span>

<span data-ttu-id="d41bb-113">MAPI llama al método **IMSProvider:: Shutdown** justo antes de liberar el objeto de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d41bb-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="d41bb-114">MAPI libera todos los objetos de inicio de sesión de un proveedor antes de llamar a **Shutdown** para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="d41bb-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d41bb-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d41bb-115">See also</span></span>



[<span data-ttu-id="d41bb-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d41bb-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

