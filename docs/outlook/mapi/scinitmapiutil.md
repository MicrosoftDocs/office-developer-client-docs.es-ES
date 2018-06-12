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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820578"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="870de-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="870de-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="870de-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="870de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="870de-105">Reemplaza [MAPIInitialize](mapiinitialize.md) cuando se usan sólo las funciones de utilidad select.</span><span class="sxs-lookup"><span data-stu-id="870de-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="870de-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="870de-106">Header file:</span></span>  <br/> |<span data-ttu-id="870de-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="870de-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="870de-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="870de-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="870de-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="870de-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="870de-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="870de-110">Called by:</span></span>  <br/> |<span data-ttu-id="870de-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="870de-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="870de-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="870de-112">Parameters</span></span>

 <span data-ttu-id="870de-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="870de-113">_ulFlags_</span></span>
  
> <span data-ttu-id="870de-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="870de-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="870de-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="870de-115">Return value</span></span>

<span data-ttu-id="870de-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="870de-116">S_OK</span></span> 
  
> <span data-ttu-id="870de-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="870de-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="870de-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="870de-118">Remarks</span></span>

<span data-ttu-id="870de-119">Las funciones **ScInitMapiUtil** y [DeinitMapiUtil](deinitmapiutil.md) cooperan para llamar a y seleccione utilidad funciones, en lugar de [MAPIInitialize](mapiinitialize.md), que llama a principal, así como la utilidad de funciones de la versión.</span><span class="sxs-lookup"><span data-stu-id="870de-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="870de-120">Cuando **ScInitMapiUtil** llama a las funciones de utilidad, también inicializa la memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="870de-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="870de-121">Una vez finalizada la utilización de las funciones que se ha llamado a **ScInitMapiUtil** , **DeinitMapiUtil** debe llamarse explícitamente para liberarlos.</span><span class="sxs-lookup"><span data-stu-id="870de-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="870de-122">Por el contrario, **MAPIInitialize** implícitamente llama a **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="870de-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="870de-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="870de-123">See also</span></span>



[<span data-ttu-id="870de-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="870de-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

