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
ms.openlocfilehash: 297b5a516f8275b236092f9f385afcb673c95de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585244"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="bb935-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="bb935-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="bb935-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb935-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb935-105">Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios y MAPI.</span><span class="sxs-lookup"><span data-stu-id="bb935-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb935-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bb935-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb935-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bb935-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bb935-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="bb935-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bb935-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bb935-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bb935-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bb935-110">Called by:</span></span>  <br/> |<span data-ttu-id="bb935-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bb935-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="bb935-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb935-112">Parameters</span></span>

 <span data-ttu-id="bb935-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="bb935-113">_eMethod_</span></span>
  
> <span data-ttu-id="bb935-114">[entrada] Especifica el (enumeración), el método para validar.</span><span class="sxs-lookup"><span data-stu-id="bb935-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="bb935-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="bb935-115">_First_</span></span>
  
> <span data-ttu-id="bb935-116">[entrada] Puntero al primer argumento en la pila.</span><span class="sxs-lookup"><span data-stu-id="bb935-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb935-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb935-117">Return value</span></span>

<span data-ttu-id="bb935-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb935-118">S_OK</span></span> 
  
> <span data-ttu-id="bb935-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="bb935-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="bb935-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="bb935-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="bb935-121">Un error de origen desconocido o inesperado no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="bb935-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb935-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb935-122">Remarks</span></span>

<span data-ttu-id="bb935-123">La macro **UlValidateParameters** se ha sustituido por la macro [UlValidateParms](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="bb935-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="bb935-124">**UlValidateParameters** no funciona correctamente en plataformas RISC y ahora no puede compilar en ellos.</span><span class="sxs-lookup"><span data-stu-id="bb935-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="bb935-125">Aún compila y funciona correctamente en plataformas Intel, pero se recomienda **UlValidateParms** en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="bb935-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

