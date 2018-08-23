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
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579721"
---
# <a name="validateparms"></a><span data-ttu-id="ce6ff-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="ce6ff-103">ValidateParms</span></span>

  
  
<span data-ttu-id="ce6ff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce6ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce6ff-105">Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce6ff-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ce6ff-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce6ff-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ce6ff-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ce6ff-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ce6ff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce6ff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ce6ff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ce6ff-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ce6ff-110">Called by:</span></span>  <br/> |<span data-ttu-id="ce6ff-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ce6ff-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="ce6ff-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce6ff-112">Parameters</span></span>

 <span data-ttu-id="ce6ff-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="ce6ff-113">_eMethod_</span></span>
  
> <span data-ttu-id="ce6ff-114">[entrada] Especifica el (enumeración), el método para validar.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="ce6ff-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="ce6ff-115">_First_</span></span>
  
> <span data-ttu-id="ce6ff-116">[entrada] Puntero al primer argumento en la pila.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce6ff-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce6ff-117">Return value</span></span>

<span data-ttu-id="ce6ff-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce6ff-118">S_OK</span></span> 
  
> <span data-ttu-id="ce6ff-119">Todos los parámetros son válidos.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="ce6ff-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="ce6ff-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="ce6ff-121">Uno o varios de los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce6ff-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce6ff-122">Remarks</span></span>

<span data-ttu-id="ce6ff-123">Parámetros pasados entre MAPI y servicio proveedores se supone que sea correcta y se sincronizan sólo depuración validación con la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="ce6ff-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="ce6ff-124">Proveedores deben comprobar todos los parámetros que se pasó por las aplicaciones cliente, pero los clientes deben se presupone que MAPI y proveedor de parámetros correctos.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="ce6ff-125">Use la macro **HR_FAILED** para comprobar los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="ce6ff-126">**ValidateParms** se llama de manera diferente dependiendo de si el código de llamada es C o C++.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="ce6ff-127">C++ pasa un parámetro implícito conocido como _este_ para cada llamada al método, que se convierte en explícitas en C y es la dirección del objeto.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="ce6ff-128">El primer parámetro, _eMethod_, es un enumerador realizado desde la interfaz y el método que se está validando e indica los parámetros que se espera encontrar en la pila.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="ce6ff-129">El segundo parámetro es diferente para C y C++.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="ce6ff-130">En C++ se denomina _primer_, y es el primer parámetro para el método que se está validando.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="ce6ff-131">El segundo parámetro para el lenguaje C, _ppThis_, es la dirección del primer parámetro para el método que es siempre un puntero de objeto.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="ce6ff-132">En ambos casos, el segundo parámetro proporciona la dirección del principio de la lista de parámetros del método y en función de _eMethod_, mueve hacia abajo de la pila y valida los parámetros.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="ce6ff-133">Los proveedores que implementan las interfaces comunes, como **IMAPITable** y **IMAPIProp** siempre deben comprobar los parámetros mediante la función **ValidateParms** con el fin de realizar seguro de coherencia entre todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="ce6ff-134">Se han definido las funciones de validación del parámetro adicional para que algunos tipos de parámetro complejo que se usará en su lugar, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="ce6ff-135">Vea los temas de referencia para las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ce6ff-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="ce6ff-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="ce6ff-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="ce6ff-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="ce6ff-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="ce6ff-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="ce6ff-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="ce6ff-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="ce6ff-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="ce6ff-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="ce6ff-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="ce6ff-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="ce6ff-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="ce6ff-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="ce6ff-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="ce6ff-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="ce6ff-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="ce6ff-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="ce6ff-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="ce6ff-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ce6ff-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="ce6ff-146">Métodos heredados usan la misma validación de parámetros como la interfaz de la que heredan.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="ce6ff-147">Por ejemplo, la comprobación de parámetros de **IMessage** y **IMAPIProp** deben ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce6ff-148">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ce6ff-148">See also</span></span>



[<span data-ttu-id="ce6ff-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="ce6ff-149">UlValidateParms</span></span>](ulvalidateparms.md)

