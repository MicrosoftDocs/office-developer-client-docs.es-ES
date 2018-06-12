---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 26949f10e22c4d2ea49594ee3365ae7d3bb3662d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818001"
---
# <a name="itnefextractprops"></a><span data-ttu-id="fc9fc-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="fc9fc-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="fc9fc-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc9fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc9fc-105">Extrae las propiedades de una encapsulación TNEF.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="fc9fc-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="fc9fc-106">Parameters</span></span>

 <span data-ttu-id="fc9fc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc9fc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fc9fc-108">[entrada] Una máscara de bits de indicadores que controla cómo descodificación de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="fc9fc-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="fc9fc-109">The following flags can be set:</span></span>
    
<span data-ttu-id="fc9fc-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="fc9fc-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="fc9fc-111">Descodifica todas las propiedades que no se especifica en el parámetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="fc9fc-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="fc9fc-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="fc9fc-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="fc9fc-113">Descodifica todas las propiedades especificadas en _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="fc9fc-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="fc9fc-114">_lpPropList_</span></span>
  
> <span data-ttu-id="fc9fc-115">[entrada] Un puntero a la lista de propiedades para incluir o excluir de la operación de descodificación.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="fc9fc-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="fc9fc-116">_lpProblems_</span></span>
  
> <span data-ttu-id="fc9fc-117">[out] Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="fc9fc-118">La estructura **STnefProblemArray** indica qué propiedades, si hay alguna, no codificados correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="fc9fc-119">Si se pasa NULL en el parámetro _lpProblems_ , no hay ninguna matriz de problema (propiedad) se devuelve.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fc9fc-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc9fc-120">Return value</span></span>

<span data-ttu-id="fc9fc-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc9fc-121">S_OK</span></span> 
  
> <span data-ttu-id="fc9fc-122">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="fc9fc-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="fc9fc-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="fc9fc-124">Datos que se va a descodificar en un objeto stream está dañados.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc9fc-125">Notas</span><span class="sxs-lookup"><span data-stu-id="fc9fc-125">Remarks</span></span>

<span data-ttu-id="fc9fc-126">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace, llame al método **ITnef::ExtractProps** para extraer (que es, descodificar) las propiedades de la encapsulación de un mensaje o datos adjuntos que se pasan a la función [OpenTnefStream](opentnefstream.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9fc-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="fc9fc-127">El proveedor o la puerta de enlace realiza la llamada puede especificar una lista de propiedades para descodificar.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="fc9fc-128">Los proveedores y las puertas de enlace también pueden usar **ExtractProps** para proporcionar información sobre cualquier tratamiento especial de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="fc9fc-129">**ExtractProps** rellena el mensaje original que se pasó a **OpenTnefStream** con las propiedades descodificadas.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="fc9fc-130">Las llamadas posteriores **ExtractProps** vuelva al mensaje y extracción la nueva lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="fc9fc-131">A diferencia del método [ITnef::AddProps](itnef-addprops.md) , que las colas solicitan acciones hasta que se llama al método **ITnef::Finish** , el método **ExtractProps** descodifica las propiedades encapsuladas inmediatamente cuando se llama.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="fc9fc-132">Por ese motivo, el mensaje de destino para encapsulación descodificación debe estar relativamente vacío.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="fc9fc-133">Las propiedades existentes en el mensaje de destino se sobrescriben con las propiedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="fc9fc-134">**ExtractProps** sólo se admite para objetos que se abren con la marca TNEF_DECODE para la función **OpenTnefStream** o [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9fc-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="fc9fc-135">La implementación de TNEF informa de problemas de codificación de secuencia TNEF sin detener el proceso de **ExtractProps** .</span><span class="sxs-lookup"><span data-stu-id="fc9fc-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="fc9fc-136">La estructura de [STnefProblemArray](stnefproblemarray.md) devuelta en _lpProblems_ indica qué atributos TNEF o las propiedades MAPI, si hay alguna, no se podrían procesar.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="fc9fc-137">El valor devuelto en el miembro **scode** de una de las estructuras de **STnefProblem** contenidos en **STnefProblemArray** indica el problema específico.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="fc9fc-138">El proveedor o la puerta de enlace puede trabajar en la suposición de que todas las propiedades o atributos para el que **ExtractProps** no devuelve un informe de problemas se procesaran correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fc9fc-139">Si una propiedad en el bloque de encapsulación de MAPI no se puede procesar y sale de la secuencia de poco fiable durante la descodificación de una secuencia TNEF, se detiene la descodificación del bloque de encapsulación y se notifica un problema.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="fc9fc-140">La matriz de problema para este tipo de problema contiene 0L para el miembro **ulPropTag** , `attMAPIProps` o `attAttachment` para el miembro **ulAttribute** y MAPI_E_UNABLE_TO_COMPLETE para el miembro **scode** .</span><span class="sxs-lookup"><span data-stu-id="fc9fc-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="fc9fc-141">Tenga en cuenta que la descodificación de la secuencia no es detenido, sólo la descodificación del bloque de encapsulación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="fc9fc-142">La secuencia de descodificación continúa con el siguiente bloque de atributos.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="fc9fc-143">Si un proveedor o una puerta de enlace no funciona con matrices de problema, puede pasar NULL en _lppProblems_; en este caso, no se devuelve la matriz de ningún problema.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="fc9fc-144">El valor devuelto en _lpProblems_ es válido sólo si la llamada devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="fc9fc-145">Cuando se devuelve S_OK, el proveedor o la puerta de enlace debe comprobar los valores devueltos en la estructura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="fc9fc-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="fc9fc-146">Si se produce un error en la llamada, no se rellena la estructura **STnefProblemArray** y el proveedor o la puerta de enlace realiza la llamada no debe utilizar o libre la estructura.</span><span class="sxs-lookup"><span data-stu-id="fc9fc-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="fc9fc-147">Si se produce ningún error en la llamada, el proveedor o la puerta de enlace realiza la llamada debe liberar la memoria para la estructura de **STnefProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9fc-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc9fc-148">Ver también</span><span class="sxs-lookup"><span data-stu-id="fc9fc-148">See also</span></span>



[<span data-ttu-id="fc9fc-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="fc9fc-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="fc9fc-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="fc9fc-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="fc9fc-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="fc9fc-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="fc9fc-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fc9fc-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fc9fc-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="fc9fc-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="fc9fc-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="fc9fc-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="fc9fc-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="fc9fc-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="fc9fc-156">ITnef: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc9fc-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

