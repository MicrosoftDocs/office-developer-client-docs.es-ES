---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409786"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="8626b-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="8626b-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="8626b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8626b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8626b-105">Cancela una conexión a una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="8626b-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8626b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8626b-106">Parameters</span></span>

 <span data-ttu-id="8626b-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8626b-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8626b-108">[In] Reservado; debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="8626b-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8626b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8626b-109">Return value</span></span>

<span data-ttu-id="8626b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8626b-110">S_OK</span></span> 
  
> <span data-ttu-id="8626b-111">La conexión se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="8626b-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="8626b-112">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="8626b-112">Notes to implementers</span></span>

<span data-ttu-id="8626b-113">En la implementación del método **Shutdown,** realice las tareas que considere necesarias.</span><span class="sxs-lookup"><span data-stu-id="8626b-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="8626b-114">MAPI llama al **método Shutdown** solo después de liberar todos los objetos de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8626b-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8626b-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="8626b-115">See also</span></span>



[<span data-ttu-id="8626b-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8626b-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

