---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419614"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="b3e55-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="b3e55-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="b3e55-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3e55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3e55-105">Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios y MAPI.</span><span class="sxs-lookup"><span data-stu-id="b3e55-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3e55-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b3e55-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3e55-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b3e55-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b3e55-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b3e55-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b3e55-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b3e55-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b3e55-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b3e55-110">Called by:</span></span>  <br/> |<span data-ttu-id="b3e55-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b3e55-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="b3e55-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3e55-112">Parameters</span></span>

 <span data-ttu-id="b3e55-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="b3e55-113">_eMethod_</span></span>
  
> <span data-ttu-id="b3e55-114">a Especifica, por enumeración, el método que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="b3e55-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="b3e55-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="b3e55-115">_First_</span></span>
  
> <span data-ttu-id="b3e55-116">a Puntero al primer argumento de la pila.</span><span class="sxs-lookup"><span data-stu-id="b3e55-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b3e55-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3e55-117">Return value</span></span>

<span data-ttu-id="b3e55-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3e55-118">S_OK</span></span> 
  
> <span data-ttu-id="b3e55-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b3e55-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b3e55-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b3e55-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b3e55-121">Un error impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="b3e55-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3e55-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3e55-122">Remarks</span></span>

<span data-ttu-id="b3e55-123">Se supone que los parámetros que se han pasado entre MAPI y los proveedores de servicios son correctos y solo se someten a la validación de depuración con la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="b3e55-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="b3e55-124">Los proveedores deben comprobar todos los parámetros pasados por las aplicaciones cliente, pero los clientes deben suponer que los parámetros MAPI y del proveedor son correctos.</span><span class="sxs-lookup"><span data-stu-id="b3e55-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="b3e55-125">Use la macro **HR_FAILED** para probar los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="b3e55-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="b3e55-126">Se llama a la macro **UlValidateParms** de forma diferente en función de si el código de llamada es C o C++.</span><span class="sxs-lookup"><span data-stu-id="b3e55-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="b3e55-127">Esta macro se usa para validar los parámetros de los métodos **IUnknown** y MAPI que devuelven valores ulong en lugar de HRESULT; la macro [ValidateParms](validateparms.md) funciona para todos los demás.</span><span class="sxs-lookup"><span data-stu-id="b3e55-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

