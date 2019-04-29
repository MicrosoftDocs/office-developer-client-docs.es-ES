---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431277"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="dc764-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="dc764-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="dc764-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc764-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc764-105">Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios y MAPI.</span><span class="sxs-lookup"><span data-stu-id="dc764-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc764-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dc764-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc764-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="dc764-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="dc764-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dc764-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc764-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc764-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc764-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dc764-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc764-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="dc764-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="dc764-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc764-112">Parameters</span></span>

 <span data-ttu-id="dc764-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="dc764-113">_eMethod_</span></span>
  
> <span data-ttu-id="dc764-114">a Especifica, por enumeración, el método que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="dc764-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="dc764-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="dc764-115">_First_</span></span>
  
> <span data-ttu-id="dc764-116">a Puntero al primer argumento de la pila.</span><span class="sxs-lookup"><span data-stu-id="dc764-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc764-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc764-117">Return value</span></span>

<span data-ttu-id="dc764-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc764-118">S_OK</span></span> 
  
> <span data-ttu-id="dc764-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="dc764-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="dc764-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="dc764-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="dc764-121">Un error de origen inesperado o desconocido impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="dc764-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc764-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc764-122">Remarks</span></span>

<span data-ttu-id="dc764-123">La macro **UlValidateParameters** se ha reemplazado por la macro [UlValidateParms](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="dc764-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="dc764-124">**UlValidateParameters** no funciona correctamente en plataformas RISC y ahora se impide su compilación en ellos.</span><span class="sxs-lookup"><span data-stu-id="dc764-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="dc764-125">Sigue compilando y funciona correctamente en plataformas Intel, pero **UlValidateParms** se recomienda en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="dc764-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

