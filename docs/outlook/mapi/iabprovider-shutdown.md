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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817121"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="a3bc5-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="a3bc5-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="a3bc5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3bc5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3bc5-105">Cancela una conexión a una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="a3bc5-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a3bc5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3bc5-106">Parameters</span></span>

 <span data-ttu-id="a3bc5-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3bc5-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a3bc5-108">[Entrada] Reservado; debe ser un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="a3bc5-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3bc5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3bc5-109">Return value</span></span>

<span data-ttu-id="a3bc5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3bc5-110">S_OK</span></span> 
  
> <span data-ttu-id="a3bc5-111">La conexión se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3bc5-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="a3bc5-112">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="a3bc5-112">Notes to implementers</span></span>

<span data-ttu-id="a3bc5-113">En la implementación del método **apagado** , lleve a cabo cualquier tarea de tener en cuenta es necesario.</span><span class="sxs-lookup"><span data-stu-id="a3bc5-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="a3bc5-114">MAPI llama a su método **Shutdown** sólo después de que se han lanzado todos los objetos de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a3bc5-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3bc5-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="a3bc5-115">See also</span></span>



[<span data-ttu-id="a3bc5-116">IABProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3bc5-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

