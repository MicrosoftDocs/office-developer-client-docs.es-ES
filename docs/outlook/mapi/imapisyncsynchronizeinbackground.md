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
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817573"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="58511-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="58511-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="58511-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58511-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="58511-105">Inicia una sincronización.</span><span class="sxs-lookup"><span data-stu-id="58511-105">Initiates a synchronization.</span></span> <span data-ttu-id="58511-106">Este método es llamado por Microsoft Outlook 2010 y Microsoft Outlook 2013 y se implementan los proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="58511-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="58511-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58511-107">Parameters</span></span>

 <span data-ttu-id="58511-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="58511-108">_psibpb_</span></span>
  
> <span data-ttu-id="58511-109">Informa al proveedor de qué se va a sincronizar y le proporciona acceso a las interfaces que pueden usarse durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="58511-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="58511-110">Es una estructura [MAPISIB](mapisib.md) .</span><span class="sxs-lookup"><span data-stu-id="58511-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="58511-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58511-111">Return value</span></span>

<span data-ttu-id="58511-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="58511-112">S_OK</span></span> 
  
> <span data-ttu-id="58511-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="58511-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58511-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="58511-114">See also</span></span>



[<span data-ttu-id="58511-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58511-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="58511-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="58511-116">MAPISIB</span></span>](mapisib.md)

