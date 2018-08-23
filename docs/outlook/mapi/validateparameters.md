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
ms.openlocfilehash: 662330a7b8c665471e9bbe6af27dff84ee68c8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586070"
---
# <a name="validateparameters"></a><span data-ttu-id="331da-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="331da-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="331da-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="331da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="331da-105">Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="331da-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="331da-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="331da-106">Header file:</span></span>  <br/> |<span data-ttu-id="331da-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="331da-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="331da-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="331da-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="331da-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="331da-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="331da-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="331da-110">Called by:</span></span>  <br/> |<span data-ttu-id="331da-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="331da-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="331da-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="331da-112">Parameters</span></span>

 <span data-ttu-id="331da-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="331da-113">_eMethod_</span></span>
  
> <span data-ttu-id="331da-114">[entrada] Especifica el (enumeración), el método para validar.</span><span class="sxs-lookup"><span data-stu-id="331da-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="331da-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="331da-115">_First_</span></span>
  
> <span data-ttu-id="331da-116">[entrada] Puntero al primer argumento en la pila.</span><span class="sxs-lookup"><span data-stu-id="331da-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="331da-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="331da-117">Return value</span></span>

<span data-ttu-id="331da-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="331da-118">S_OK</span></span> 
  
> <span data-ttu-id="331da-119">Todos los parámetros son válidos.</span><span class="sxs-lookup"><span data-stu-id="331da-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="331da-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="331da-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="331da-121">Uno o varios de los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="331da-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="331da-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="331da-122">Remarks</span></span>

<span data-ttu-id="331da-123">La macro **ValidateParameters** se ha sustituido por la macro [ValidateParms](validateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="331da-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="331da-124">**ValidateParameters** no funciona correctamente en plataformas RISC y ahora no puede compilar en ellos.</span><span class="sxs-lookup"><span data-stu-id="331da-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="331da-125">Aún compila y funciona correctamente en plataformas Intel, pero se recomienda **ValidateParms** en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="331da-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

