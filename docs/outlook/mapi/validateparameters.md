---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329571"
---
# <a name="validateparameters"></a><span data-ttu-id="c9d09-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="c9d09-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="c9d09-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9d09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9d09-105">Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="c9d09-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9d09-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c9d09-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9d09-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c9d09-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c9d09-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c9d09-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9d09-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c9d09-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c9d09-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c9d09-110">Called by:</span></span>  <br/> |<span data-ttu-id="c9d09-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c9d09-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="c9d09-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9d09-112">Parameters</span></span>

 <span data-ttu-id="c9d09-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="c9d09-113">_eMethod_</span></span>
  
> <span data-ttu-id="c9d09-114">a Especifica, por enumeración, el método que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="c9d09-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="c9d09-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="c9d09-115">_First_</span></span>
  
> <span data-ttu-id="c9d09-116">a Puntero al primer argumento de la pila.</span><span class="sxs-lookup"><span data-stu-id="c9d09-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9d09-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9d09-117">Return value</span></span>

<span data-ttu-id="c9d09-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9d09-118">S_OK</span></span> 
  
> <span data-ttu-id="c9d09-119">Todos los parámetros son válidos.</span><span class="sxs-lookup"><span data-stu-id="c9d09-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="c9d09-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c9d09-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="c9d09-121">Uno o varios de los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="c9d09-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9d09-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9d09-122">Remarks</span></span>

<span data-ttu-id="c9d09-123">La macro **ValidateParameters** se ha reemplazado por la macro [ValidateParms](validateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d09-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="c9d09-124">**ValidateParameters** no funciona correctamente en plataformas RISC y ahora se impide su compilación en ellos.</span><span class="sxs-lookup"><span data-stu-id="c9d09-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="c9d09-125">Sigue compilando y funciona correctamente en plataformas Intel, pero **ValidateParms** se recomienda en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="c9d09-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

