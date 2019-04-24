---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357200"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="6fe70-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="6fe70-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="6fe70-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fe70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fe70-105">Cierra un proveedor de transporte de manera ordenada.</span><span class="sxs-lookup"><span data-stu-id="6fe70-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6fe70-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6fe70-106">Parameters</span></span>

 <span data-ttu-id="6fe70-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="6fe70-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="6fe70-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6fe70-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fe70-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fe70-109">Return value</span></span>

<span data-ttu-id="6fe70-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fe70-110">S_OK</span></span> 
  
> <span data-ttu-id="6fe70-111">La llamada se ha realizado correctamente al apagar el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="6fe70-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fe70-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6fe70-112">Remarks</span></span>

<span data-ttu-id="6fe70-113">La cola MAPI llama al método **IXPProvider:: Shutdown** justo antes de liberar un objeto de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="6fe70-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="6fe70-114">Antes de llamar a **Shutdown**, MAPI libera todos los objetos de inicio de sesión de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="6fe70-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6fe70-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fe70-115">See also</span></span>



[<span data-ttu-id="6fe70-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="6fe70-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="6fe70-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fe70-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

