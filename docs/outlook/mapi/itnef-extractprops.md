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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407504"
---
# <a name="itnefextractprops"></a><span data-ttu-id="c66fe-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="c66fe-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="c66fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c66fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c66fe-105">Extrae las propiedades de una encapsulación TNEF.</span><span class="sxs-lookup"><span data-stu-id="c66fe-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="c66fe-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c66fe-106">Parameters</span></span>

 <span data-ttu-id="c66fe-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c66fe-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c66fe-108">[in] Máscara de bits de marcas que controla cómo se descodifican las propiedades.</span><span class="sxs-lookup"><span data-stu-id="c66fe-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="c66fe-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="c66fe-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c66fe-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="c66fe-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="c66fe-111">Descodifica todas las propiedades no especificadas en el _parámetro lpPropList._</span><span class="sxs-lookup"><span data-stu-id="c66fe-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="c66fe-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="c66fe-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="c66fe-113">Descodifica todas las propiedades especificadas en  _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="c66fe-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="c66fe-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="c66fe-114">_lpPropList_</span></span>
  
> <span data-ttu-id="c66fe-115">[in] Puntero a la lista de propiedades que se incluirán o excluirán de la operación de decodificación.</span><span class="sxs-lookup"><span data-stu-id="c66fe-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="c66fe-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="c66fe-116">_lpProblems_</span></span>
  
> <span data-ttu-id="c66fe-117">[salida] Puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="c66fe-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="c66fe-118">La **estructura STnefProblemArray** indica qué propiedades, si las hay, no se codificaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="c66fe-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="c66fe-119">Si se pasa NULL en el  _parámetro lpProblems,_ no se devuelve ninguna matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c66fe-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c66fe-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c66fe-120">Return value</span></span>

<span data-ttu-id="c66fe-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c66fe-121">S_OK</span></span> 
  
> <span data-ttu-id="c66fe-122">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c66fe-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="c66fe-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="c66fe-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="c66fe-124">Los datos que se descodifican en una secuencia están dañados.</span><span class="sxs-lookup"><span data-stu-id="c66fe-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c66fe-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c66fe-125">Remarks</span></span>

<span data-ttu-id="c66fe-126">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::ExtractProps** para extraer (es decir, descodificar) las propiedades de la encapsulación de un mensaje o de los datos adjuntos que se pasaron a la función [OpenTnefStream.](opentnefstream.md)</span><span class="sxs-lookup"><span data-stu-id="c66fe-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="c66fe-127">El proveedor de llamadas o la puerta de enlace puede especificar una lista de propiedades para descodificar.</span><span class="sxs-lookup"><span data-stu-id="c66fe-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="c66fe-128">Los proveedores y puertas de enlace también pueden usar **ExtractProps** para proporcionar información sobre cualquier tratamiento especial para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c66fe-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="c66fe-129">**ExtractProps** rellena el mensaje original pasado **a OpenTnefStream** con las propiedades descodificadas.</span><span class="sxs-lookup"><span data-stu-id="c66fe-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="c66fe-130">Las **llamadas ExtractProps posteriores** regresan al mensaje y extraen la nueva lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c66fe-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="c66fe-131">A diferencia del método [ITnef::AddProps,](itnef-addprops.md) que pone en cola las acciones solicitadas hasta que se llama al método **ITnef::Finish,** el método **ExtractProps** descodifica las propiedades encapsuladas inmediatamente cuando se llama a él.</span><span class="sxs-lookup"><span data-stu-id="c66fe-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="c66fe-132">Por ese motivo, el mensaje de destino para la decodificación de encapsulación debe estar relativamente vacío.</span><span class="sxs-lookup"><span data-stu-id="c66fe-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="c66fe-133">Las propiedades existentes en el mensaje de destino se sobrescriben mediante propiedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="c66fe-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="c66fe-134">**ExtractProps** solo se admite para los objetos que se abren con la marca TNEF_DECODE para la función **OpenTnefStream** o [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="c66fe-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="c66fe-135">La implementación de TNEF informa de problemas de codificación de secuencias TNEF sin detener el **proceso ExtractProps.**</span><span class="sxs-lookup"><span data-stu-id="c66fe-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="c66fe-136">La [estructura STnefProblemArray](stnefproblemarray.md) devuelta en  _lpProblems_ indica qué atributos TNEF o propiedades MAPI, si las hubiera, no se pudieron procesar.</span><span class="sxs-lookup"><span data-stu-id="c66fe-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="c66fe-137">El valor devuelto en el **miembro scode** de una de las estructuras **STnefProblem** contenidas en **STnefProblemArray** indica el problema específico.</span><span class="sxs-lookup"><span data-stu-id="c66fe-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="c66fe-138">El proveedor o la puerta de enlace pueden funcionar con la suposición de que todas las propiedades o atributos para los que **ExtractProps** no devuelve un informe de problemas se procesaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="c66fe-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c66fe-139">Si una propiedad del bloque de encapsulación MAPI no se puede procesar y deja la secuencia poco confiable durante la decodificación de una secuencia TNEF, se detiene la decodificación del bloque de encapsulación y se notifica un problema.</span><span class="sxs-lookup"><span data-stu-id="c66fe-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="c66fe-140">La matriz de problemas para este tipo de problema contiene 0L para el miembro **ulPropTag,** o para el miembro ulAttribute, y MAPI_E_UNABLE_TO_COMPLETE para `attMAPIProps` `attAttachment` el miembro **scode.** </span><span class="sxs-lookup"><span data-stu-id="c66fe-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="c66fe-141">Tenga en cuenta que la decodificación de la secuencia no está detenida, solo la decodificación del bloque de encapsulación MAPI.</span><span class="sxs-lookup"><span data-stu-id="c66fe-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="c66fe-142">La decodificación de secuencias continúa con el siguiente bloque de atributos.</span><span class="sxs-lookup"><span data-stu-id="c66fe-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="c66fe-143">Si un proveedor o puerta de enlace no funciona con matrices problemáticas, puede pasar NULL en  _lppProblems_; en este caso, no se devuelve ninguna matriz de problemas.</span><span class="sxs-lookup"><span data-stu-id="c66fe-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="c66fe-144">El valor devuelto en  _lpProblems_ solo es válido si la llamada devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="c66fe-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="c66fe-145">Cuando S_OK, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura **STnefProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="c66fe-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="c66fe-146">Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor de llamadas o la puerta de enlace no debe usar ni liberar la estructura.</span><span class="sxs-lookup"><span data-stu-id="c66fe-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="c66fe-147">Si no se produce ningún error en la llamada, el proveedor de llamadas o la puerta de enlace debe liberar la memoria de la estructura **STnefProblemArray** llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c66fe-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c66fe-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="c66fe-148">See also</span></span>



[<span data-ttu-id="c66fe-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="c66fe-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="c66fe-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="c66fe-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="c66fe-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="c66fe-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="c66fe-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c66fe-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c66fe-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="c66fe-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="c66fe-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="c66fe-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="c66fe-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="c66fe-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="c66fe-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c66fe-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

