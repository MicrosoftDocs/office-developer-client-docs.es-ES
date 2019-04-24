---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351264"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="7a25d-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="7a25d-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="7a25d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a25d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a25d-105">Reemplaza [MAPIInitialize](mapiinitialize.md) cuando solo se usan funciones de la utilidad Select.</span><span class="sxs-lookup"><span data-stu-id="7a25d-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a25d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7a25d-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a25d-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="7a25d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7a25d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7a25d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7a25d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7a25d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7a25d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7a25d-110">Called by:</span></span>  <br/> |<span data-ttu-id="7a25d-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="7a25d-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7a25d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="7a25d-112">Parameters</span></span>

 <span data-ttu-id="7a25d-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a25d-113">_ulFlags_</span></span>
  
> <span data-ttu-id="7a25d-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7a25d-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a25d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a25d-115">Return value</span></span>

<span data-ttu-id="7a25d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a25d-116">S_OK</span></span> 
  
> <span data-ttu-id="7a25d-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="7a25d-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a25d-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a25d-118">Remarks</span></span>

<span data-ttu-id="7a25d-119">Las funciones **ScInitMapiUtil** y [DeinitMapiUtil](deinitmapiutil.md) cooperan para llamar y liberar funciones de la utilidad Select, en oposición a [MAPIInitialize](mapiinitialize.md), que llama a las funciones principales y de utilidades.</span><span class="sxs-lookup"><span data-stu-id="7a25d-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="7a25d-120">Cuando **ScInitMapiUtil** llama a las funciones de utilidad, también inicializa la memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="7a25d-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="7a25d-121">Cuando se completa el uso de las funciones que **ScInitMapiUtil** ha llamado, se debe llamar explícitamente a **DeinitMapiUtil** para liberarlos.</span><span class="sxs-lookup"><span data-stu-id="7a25d-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="7a25d-122">Por el contrario, **MAPIInitialize** llama implícitamente a **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="7a25d-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a25d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a25d-123">See also</span></span>



[<span data-ttu-id="7a25d-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="7a25d-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

