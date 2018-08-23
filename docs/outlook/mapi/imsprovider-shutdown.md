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
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589094"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="efef6-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="efef6-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="efef6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efef6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efef6-105">Cierra un proveedor de almacén de mensajes de una forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="efef6-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="efef6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efef6-106">Parameters</span></span>

 <span data-ttu-id="efef6-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="efef6-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="efef6-108">[entrada] Reservado; debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="efef6-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efef6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efef6-109">Return value</span></span>

<span data-ttu-id="efef6-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="efef6-110">S_OK</span></span> 
  
> <span data-ttu-id="efef6-111">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="efef6-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efef6-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efef6-112">Remarks</span></span>

<span data-ttu-id="efef6-113">MAPI, llama al método **IMSProvider::Shutdown** justo antes de liberar el objeto de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="efef6-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="efef6-114">MAPI libera todos los objetos de inicio de sesión para un proveedor antes de llamar a **apagado** de ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="efef6-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efef6-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="efef6-115">See also</span></span>



[<span data-ttu-id="efef6-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="efef6-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

