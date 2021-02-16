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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409695"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="7ddf0-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="7ddf0-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="7ddf0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ddf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ddf0-105">Cierra un proveedor de transporte de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7ddf0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ddf0-106">Parameters</span></span>

 <span data-ttu-id="7ddf0-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ddf0-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="7ddf0-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ddf0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ddf0-109">Return value</span></span>

<span data-ttu-id="7ddf0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ddf0-110">S_OK</span></span> 
  
> <span data-ttu-id="7ddf0-111">La llamada ha logrado apagar el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ddf0-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ddf0-112">Remarks</span></span>

<span data-ttu-id="7ddf0-113">La cola MAPI llama al método **IXPProvider::Shutdown** justo antes de liberar un objeto de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="7ddf0-114">Antes de **llamar a Shutdown**, MAPI libera todos los objetos de inicio de sesión para un proveedor.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ddf0-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ddf0-115">See also</span></span>



[<span data-ttu-id="7ddf0-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="7ddf0-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="7ddf0-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ddf0-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

