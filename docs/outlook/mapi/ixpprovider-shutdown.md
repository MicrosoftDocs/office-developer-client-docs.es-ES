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
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592608"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="42c53-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="42c53-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="42c53-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42c53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42c53-105">Se cierra un proveedor de transporte de una forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="42c53-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="42c53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42c53-106">Parameters</span></span>

 <span data-ttu-id="42c53-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="42c53-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="42c53-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="42c53-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42c53-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42c53-109">Return value</span></span>

<span data-ttu-id="42c53-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="42c53-110">S_OK</span></span> 
  
> <span data-ttu-id="42c53-111">La llamada se ha realizado correctamente en Apagar el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="42c53-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42c53-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42c53-112">Remarks</span></span>

<span data-ttu-id="42c53-113">La cola MAPI llama al método de **IXPProvider::Shutdown** justo antes de la liberación de un objeto de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="42c53-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="42c53-114">Antes de llamar a **apagado**, MAPI libera todos los objetos de inicio de sesión para un proveedor.</span><span class="sxs-lookup"><span data-stu-id="42c53-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42c53-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="42c53-115">See also</span></span>



[<span data-ttu-id="42c53-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="42c53-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="42c53-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42c53-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

