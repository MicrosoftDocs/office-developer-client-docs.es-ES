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
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818018"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="0ba55-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="0ba55-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="0ba55-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ba55-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ba55-105">Se cierra un proveedor de transporte de una forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="0ba55-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0ba55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ba55-106">Parameters</span></span>

 <span data-ttu-id="0ba55-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ba55-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="0ba55-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0ba55-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ba55-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ba55-109">Return value</span></span>

<span data-ttu-id="0ba55-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ba55-110">S_OK</span></span> 
  
> <span data-ttu-id="0ba55-111">La llamada se ha realizado correctamente en Apagar el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0ba55-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ba55-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ba55-112">Remarks</span></span>

<span data-ttu-id="0ba55-113">La cola MAPI llama al método de **IXPProvider::Shutdown** justo antes de la liberación de un objeto de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0ba55-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="0ba55-114">Antes de llamar a **apagado**, MAPI libera todos los objetos de inicio de sesión para un proveedor.</span><span class="sxs-lookup"><span data-stu-id="0ba55-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ba55-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ba55-115">See also</span></span>



[<span data-ttu-id="0ba55-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="0ba55-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="0ba55-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ba55-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

