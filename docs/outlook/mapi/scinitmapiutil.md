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
ms.openlocfilehash: 3176280de33bda01bfd09ebaafc31d326d455a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575038"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="743a2-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="743a2-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="743a2-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="743a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="743a2-105">Reemplaza [MAPIInitialize](mapiinitialize.md) cuando se usan sólo las funciones de utilidad select.</span><span class="sxs-lookup"><span data-stu-id="743a2-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="743a2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="743a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="743a2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="743a2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="743a2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="743a2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="743a2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="743a2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="743a2-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="743a2-110">Called by:</span></span>  <br/> |<span data-ttu-id="743a2-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="743a2-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="743a2-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="743a2-112">Parameters</span></span>

 <span data-ttu-id="743a2-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="743a2-113">_ulFlags_</span></span>
  
> <span data-ttu-id="743a2-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="743a2-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="743a2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="743a2-115">Return value</span></span>

<span data-ttu-id="743a2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="743a2-116">S_OK</span></span> 
  
> <span data-ttu-id="743a2-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="743a2-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="743a2-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="743a2-118">Remarks</span></span>

<span data-ttu-id="743a2-119">Las funciones **ScInitMapiUtil** y [DeinitMapiUtil](deinitmapiutil.md) cooperan para llamar a y seleccione utilidad funciones, en lugar de [MAPIInitialize](mapiinitialize.md), que llama a principal, así como la utilidad de funciones de la versión.</span><span class="sxs-lookup"><span data-stu-id="743a2-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="743a2-120">Cuando **ScInitMapiUtil** llama a las funciones de utilidad, también inicializa la memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="743a2-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="743a2-121">Una vez finalizada la utilización de las funciones que se ha llamado a **ScInitMapiUtil** , **DeinitMapiUtil** debe llamarse explícitamente para liberarlos.</span><span class="sxs-lookup"><span data-stu-id="743a2-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="743a2-122">Por el contrario, **MAPIInitialize** implícitamente llama a **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="743a2-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="743a2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="743a2-123">See also</span></span>



[<span data-ttu-id="743a2-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="743a2-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

