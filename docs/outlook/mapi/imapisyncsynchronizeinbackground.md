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
ms.openlocfilehash: ee6fe07df894213331ab51f9abaa4008247dac07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568780"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="31f17-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="31f17-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="31f17-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31f17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="31f17-105">Inicia una sincronización.</span><span class="sxs-lookup"><span data-stu-id="31f17-105">Initiates a synchronization.</span></span> <span data-ttu-id="31f17-106">Este método es llamado por Microsoft Outlook 2010 y Microsoft Outlook 2013 y se implementan los proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="31f17-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="31f17-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31f17-107">Parameters</span></span>

 <span data-ttu-id="31f17-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="31f17-108">_psibpb_</span></span>
  
> <span data-ttu-id="31f17-109">Informa al proveedor de qué se va a sincronizar y le proporciona acceso a las interfaces que pueden usarse durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="31f17-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="31f17-110">Es una estructura [MAPISIB](mapisib.md) .</span><span class="sxs-lookup"><span data-stu-id="31f17-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="31f17-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31f17-111">Return value</span></span>

<span data-ttu-id="31f17-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="31f17-112">S_OK</span></span> 
  
> <span data-ttu-id="31f17-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="31f17-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31f17-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="31f17-114">See also</span></span>



[<span data-ttu-id="31f17-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31f17-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="31f17-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="31f17-116">MAPISIB</span></span>](mapisib.md)

