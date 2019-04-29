---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Última modificación: 26 de junio de 2012'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426859"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="e2115-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="e2115-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="e2115-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2115-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e2115-105">Inicia una sincronización.</span><span class="sxs-lookup"><span data-stu-id="e2115-105">Initiates a synchronization.</span></span> <span data-ttu-id="e2115-106">Este método es llamado por Microsoft Outlook 2010 y Microsoft Outlook 2013 y lo implementan los proveedores de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2115-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="e2115-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e2115-107">Parameters</span></span>

 <span data-ttu-id="e2115-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="e2115-108">_psibpb_</span></span>
  
> <span data-ttu-id="e2115-109">Informa al proveedor de lo que se va a sincronizar y proporciona acceso a las interfaces que se pueden usar durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="e2115-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="e2115-110">Es una estructura [MAPISIB](mapisib.md) .</span><span class="sxs-lookup"><span data-stu-id="e2115-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2115-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2115-111">Return value</span></span>

<span data-ttu-id="e2115-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2115-112">S_OK</span></span> 
  
> <span data-ttu-id="e2115-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="e2115-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2115-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="e2115-114">See also</span></span>



[<span data-ttu-id="e2115-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2115-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="e2115-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="e2115-116">MAPISIB</span></span>](mapisib.md)

