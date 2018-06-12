---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820905"
---
# <a name="ulpropsize"></a><span data-ttu-id="3455f-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="3455f-103">UlPropSize</span></span>

  
  
<span data-ttu-id="3455f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3455f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3455f-105">Devuelve el tamaño de un valor de propiedad único.</span><span class="sxs-lookup"><span data-stu-id="3455f-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3455f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3455f-106">Header file:</span></span>  <br/> |<span data-ttu-id="3455f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3455f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3455f-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="3455f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3455f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3455f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3455f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3455f-110">Called by:</span></span>  <br/> |<span data-ttu-id="3455f-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="3455f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="3455f-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3455f-112">Parameters</span></span>

 <span data-ttu-id="3455f-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="3455f-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="3455f-114">[entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definición de la propiedad que se va a medir.</span><span class="sxs-lookup"><span data-stu-id="3455f-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3455f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3455f-115">Return value</span></span>

<span data-ttu-id="3455f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3455f-116">S_OK</span></span> 
  
> <span data-ttu-id="3455f-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3455f-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3455f-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="3455f-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="3455f-119">Un error de origen desconocido o inesperado no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="3455f-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3455f-120">Notas</span><span class="sxs-lookup"><span data-stu-id="3455f-120">Remarks</span></span>

<span data-ttu-id="3455f-121">La función **UlPropSize** devuelve el tamaño, en bytes, del valor de propiedad para la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="3455f-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="3455f-122">No tiene en cuenta el tamaño del resto de la estructura **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="3455f-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

