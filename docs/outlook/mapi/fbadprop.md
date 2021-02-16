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
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426719"
---
# <a name="fbadprop"></a><span data-ttu-id="c023a-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="c023a-103">FBadProp</span></span>

  
  
<span data-ttu-id="c023a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c023a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c023a-105">Valida una propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="c023a-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c023a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c023a-106">Header file:</span></span>  <br/> |<span data-ttu-id="c023a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c023a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c023a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c023a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c023a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c023a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c023a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c023a-110">Called by:</span></span>  <br/> |<span data-ttu-id="c023a-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c023a-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="c023a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c023a-112">Parameters</span></span>

 <span data-ttu-id="c023a-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="c023a-113">_lpprop_</span></span>
  
> <span data-ttu-id="c023a-114">[entrada] Una estructura [SPropValue](spropvalue.md) que define la propiedad que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="c023a-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c023a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c023a-115">Return value</span></span>

<span data-ttu-id="c023a-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c023a-116">TRUE</span></span> 
  
> <span data-ttu-id="c023a-117">La propiedad especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="c023a-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="c023a-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c023a-118">FALSE</span></span> 
  
> <span data-ttu-id="c023a-119">La propiedad especificada es válida.</span><span class="sxs-lookup"><span data-stu-id="c023a-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c023a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c023a-120">Remarks</span></span>

<span data-ttu-id="c023a-121">Un proveedor de servicios puede llamar a la función **FBadProp** por diversos motivos, por ejemplo, para prepararse para una llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) que establece una propiedad.</span><span class="sxs-lookup"><span data-stu-id="c023a-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="c023a-122">**FBadProp** valida la propiedad especificada según el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c023a-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="c023a-123">Por ejemplo, si la propiedad es booleana, **FBadProp** se asegura de que el valor es TRUE o FALSE.</span><span class="sxs-lookup"><span data-stu-id="c023a-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="c023a-124">Si la propiedad es binaria, **FBadProp** comprueba el puntero y el tamaño y se asegura de que se asigna correctamente.</span><span class="sxs-lookup"><span data-stu-id="c023a-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c023a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c023a-125">See also</span></span>



[<span data-ttu-id="c023a-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="c023a-126">FBadPropTag</span></span>](fbadproptag.md)

