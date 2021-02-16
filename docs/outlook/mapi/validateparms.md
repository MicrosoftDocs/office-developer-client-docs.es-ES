---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436811"
---
# <a name="validateparms"></a><span data-ttu-id="bf08c-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="bf08c-103">ValidateParms</span></span>

  
  
<span data-ttu-id="bf08c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf08c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf08c-105">Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="bf08c-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf08c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bf08c-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf08c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bf08c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bf08c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bf08c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bf08c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bf08c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bf08c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bf08c-110">Called by:</span></span>  <br/> |<span data-ttu-id="bf08c-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bf08c-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="bf08c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf08c-112">Parameters</span></span>

 <span data-ttu-id="bf08c-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="bf08c-113">_eMethod_</span></span>
  
> <span data-ttu-id="bf08c-114">[entrada] Especifica, por enumeración, el método que se debe validar.</span><span class="sxs-lookup"><span data-stu-id="bf08c-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="bf08c-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="bf08c-115">_First_</span></span>
  
> <span data-ttu-id="bf08c-116">[entrada] Puntero al primer argumento de la pila.</span><span class="sxs-lookup"><span data-stu-id="bf08c-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf08c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf08c-117">Return value</span></span>

<span data-ttu-id="bf08c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf08c-118">S_OK</span></span> 
  
> <span data-ttu-id="bf08c-119">Todos los parámetros son válidos.</span><span class="sxs-lookup"><span data-stu-id="bf08c-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="bf08c-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="bf08c-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="bf08c-121">Uno o varios de los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="bf08c-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf08c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf08c-122">Remarks</span></span>

<span data-ttu-id="bf08c-123">Se supone que los parámetros pasados entre MAPI y los proveedores de servicios son correctos y solo se someten a la validación de depuración con la macro [CheckParms.](checkparms.md)</span><span class="sxs-lookup"><span data-stu-id="bf08c-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="bf08c-124">Los proveedores deben comprobar todos los parámetros pasados por las aplicaciones cliente, pero los clientes deben suponer que los parámetros MAPI y del proveedor son correctos.</span><span class="sxs-lookup"><span data-stu-id="bf08c-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="bf08c-125">Use la **macro HR_FAILED** para probar los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="bf08c-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="bf08c-126">**ValidateParms** se llama de forma diferente en función de si el código de llamada es C o C++.</span><span class="sxs-lookup"><span data-stu-id="bf08c-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="bf08c-127">C++ pasa un parámetro  implícito conocido como esto a cada llamada de método, que se convierte en explícita en C y es la dirección del objeto.</span><span class="sxs-lookup"><span data-stu-id="bf08c-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="bf08c-128">El primer parámetro,  _eMethod_, es un enumerador creado a partir de la interfaz y el método que se va a validar e indica qué parámetros esperar encontrar en la pila.</span><span class="sxs-lookup"><span data-stu-id="bf08c-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="bf08c-129">El segundo parámetro es diferente para C y C++.</span><span class="sxs-lookup"><span data-stu-id="bf08c-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="bf08c-130">En C++ se denomina  _First_ y es el primer parámetro del método que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="bf08c-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="bf08c-131">El segundo parámetro para el lenguaje C,  _ppThis_, es la dirección del primer parámetro para el método que siempre es un puntero de objeto.</span><span class="sxs-lookup"><span data-stu-id="bf08c-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="bf08c-132">En ambos casos, el segundo parámetro proporciona la dirección del principio de la lista de parámetros del método y, en función de  _eMethod,_ baja la pila y valida los parámetros.</span><span class="sxs-lookup"><span data-stu-id="bf08c-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="bf08c-133">Los proveedores que implementan interfaces comunes como **IMAPITable** e **IMAPIProp** siempre deben comprobar los parámetros mediante la función **ValidateParms** para garantizar la coherencia en todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="bf08c-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="bf08c-134">Se han definido funciones de validación de parámetros adicionales para algunos tipos de parámetros complejos que se usarán según corresponda.</span><span class="sxs-lookup"><span data-stu-id="bf08c-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="bf08c-135">Consulte los temas de referencia para las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="bf08c-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="bf08c-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="bf08c-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="bf08c-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="bf08c-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="bf08c-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="bf08c-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="bf08c-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="bf08c-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="bf08c-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="bf08c-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="bf08c-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="bf08c-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="bf08c-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="bf08c-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="bf08c-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="bf08c-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="bf08c-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="bf08c-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="bf08c-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="bf08c-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="bf08c-146">Los métodos heredados usan la misma validación de parámetros que la interfaz de la que heredan.</span><span class="sxs-lookup"><span data-stu-id="bf08c-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="bf08c-147">Por ejemplo, la comprobación de parámetros **para IMessage** e **IMAPIProp** debe ser la misma.</span><span class="sxs-lookup"><span data-stu-id="bf08c-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf08c-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf08c-148">See also</span></span>



[<span data-ttu-id="bf08c-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="bf08c-149">UlValidateParms</span></span>](ulvalidateparms.md)

