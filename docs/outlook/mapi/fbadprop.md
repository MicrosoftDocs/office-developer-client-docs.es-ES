---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816781"
---
# <a name="fbadprop"></a><span data-ttu-id="bf3bc-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="bf3bc-103">FBadProp</span></span>

  
  
<span data-ttu-id="bf3bc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf3bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf3bc-105">Valida una propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf3bc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bf3bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf3bc-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bf3bc-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bf3bc-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="bf3bc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bf3bc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bf3bc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bf3bc-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bf3bc-110">Called by:</span></span>  <br/> |<span data-ttu-id="bf3bc-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bf3bc-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="bf3bc-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf3bc-112">Parameters</span></span>

 <span data-ttu-id="bf3bc-113">_lpProp_</span><span class="sxs-lookup"><span data-stu-id="bf3bc-113">_lpprop_</span></span>
  
> <span data-ttu-id="bf3bc-114">[entrada] Una estructura [SPropValue](spropvalue.md) definición de la propiedad que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bf3bc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf3bc-115">Return value</span></span>

<span data-ttu-id="bf3bc-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="bf3bc-116">TRUE</span></span> 
  
> <span data-ttu-id="bf3bc-117">La propiedad especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="bf3bc-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="bf3bc-118">FALSE</span></span> 
  
> <span data-ttu-id="bf3bc-119">La propiedad especificada es válida.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf3bc-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf3bc-120">Remarks</span></span>

<span data-ttu-id="bf3bc-121">Un proveedor de servicios puede llamar a la función **FBadProp** por varias razones, por ejemplo, para preparar una llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) al establecer una propiedad.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="bf3bc-122">**FBadProp** valida la propiedad especificada según el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="bf3bc-123">Por ejemplo, si la propiedad es Boolean, **FBadProp** hacer sures que su valor es TRUE o FALSE.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="bf3bc-124">Si la propiedad es binario, **FBadProp** comprueba su puntero y su tamaño y se asegura de que está asignado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bf3bc-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf3bc-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf3bc-125">See also</span></span>



[<span data-ttu-id="bf3bc-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="bf3bc-126">FBadPropTag</span></span>](fbadproptag.md)

