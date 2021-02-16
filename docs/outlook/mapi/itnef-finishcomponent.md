---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416443"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="ac309-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="ac309-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="ac309-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac309-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac309-105">Procesa componentes individuales de un mensaje de uno en uno en una secuencia Transport-Neutral de formato de encapsulamiento (TNEF).</span><span class="sxs-lookup"><span data-stu-id="ac309-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ac309-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac309-106">Parameters</span></span>

 <span data-ttu-id="ac309-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac309-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ac309-108">[entrada] Máscara de bits de marcas que controla qué componente se finalizará.</span><span class="sxs-lookup"><span data-stu-id="ac309-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="ac309-109">Debe establecerse una u otra de las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="ac309-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="ac309-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="ac309-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="ac309-111">El procesamiento finalizará para un objeto de datos adjuntos; El  _parámetro ulComponentID_ contiene **la PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac309-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="ac309-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="ac309-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="ac309-113">El procesamiento finalizará para un objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac309-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="ac309-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="ac309-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="ac309-115">[entrada] 0 para indicar el procesamiento de un mensaje o la PR_ATTACH_NUM **propiedad** de un archivo adjunto que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="ac309-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="ac309-116">Si la TNEF_COMPONENT_MESSAGE se establece en el  _parámetro ulFlags,_  _ulComponentID_ debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="ac309-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="ac309-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="ac309-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="ac309-118">[entrada] Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene etiquetas de propiedad que identifican las propiedades pasadas en el parámetro _lpCustomProps._</span><span class="sxs-lookup"><span data-stu-id="ac309-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="ac309-119">Debe haber una correspondencia uno a uno entre cada valor de propiedad en _lpCustomProps_ y una etiqueta de propiedad en el _parámetro lpCustomPropList._</span><span class="sxs-lookup"><span data-stu-id="ac309-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="ac309-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="ac309-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="ac309-121">[entrada] Puntero a una [estructura SPropValue](spropvalue.md) que contiene valores de propiedad para las propiedades que se codifican.</span><span class="sxs-lookup"><span data-stu-id="ac309-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="ac309-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="ac309-122">_lpPropList_</span></span>
  
> <span data-ttu-id="ac309-123">[entrada] Puntero a una estructura **SPropTagArray** que contiene etiquetas de propiedad para las propiedades que se codifican.</span><span class="sxs-lookup"><span data-stu-id="ac309-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="ac309-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="ac309-124">_lppProblems_</span></span>
  
> <span data-ttu-id="ac309-125">[salida] Puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="ac309-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="ac309-126">La **estructura STnefProblemArray** indica qué propiedades, si las hay, no se codificaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac309-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="ac309-127">Si se pasa NULL en el  _parámetro lppProblems,_ no se devuelve ninguna matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ac309-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac309-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac309-128">Return value</span></span>

<span data-ttu-id="ac309-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac309-129">S_OK</span></span> 
  
> <span data-ttu-id="ac309-130">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ac309-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac309-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac309-131">Remarks</span></span>

<span data-ttu-id="ac309-132">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::FinishComponent** para realizar el procesamiento de TNEF para un componente, ya sea un mensaje o datos adjuntos, como se indica en la marca establecida en el parámetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ac309-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="ac309-133">Para habilitar el procesamiento de componentes, el proveedor de llamadas o la puerta de enlace pasan la marca TNEF_COMPONENT_ENCODING en  _ulFlags_ para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) que abrió el objeto para recibir codificación.</span><span class="sxs-lookup"><span data-stu-id="ac309-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="ac309-134">Pasar valores en los parámetros _lpCustomPropList_ y _lpCustomProps_ realiza una codificación de componentes equivalente a la realizada por el método [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="ac309-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="ac309-135">Pasar un valor en el parámetro  _lpPropList_ realiza una codificación de componentes equivalente a la realizada por el método [ITnef::AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE establecida en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ac309-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="ac309-136">Pasar estos valores permite realizar codificaciones con una sola llamada en lugar de varias llamadas.</span><span class="sxs-lookup"><span data-stu-id="ac309-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="ac309-137">La implementación de TNEF informa de problemas de codificación de secuencias TNEF sin detener el **proceso finishcomponent.**</span><span class="sxs-lookup"><span data-stu-id="ac309-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="ac309-138">La **estructura STnefProblemArray** devuelta en  _lppProblems_ indica qué atributos TNEF o propiedades MAPI, si las hay, no se pudieron procesar.</span><span class="sxs-lookup"><span data-stu-id="ac309-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="ac309-139">El valor devuelto en el **miembro scode** de una de las estructuras **STnefProblem** contenidas en **STnefProblemArray** indica el problema específico.</span><span class="sxs-lookup"><span data-stu-id="ac309-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="ac309-140">El proveedor o la puerta de enlace pueden trabajar en la suposición de que todas las propiedades o atributos para los que **FinishComponent** no devuelve un informe de problemas se procesaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac309-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="ac309-141">Si un proveedor o puerta de enlace no funciona con matrices de problemas, puede pasar NULL en  _lppProblems_; En este caso, no se devuelve ninguna matriz problemática.</span><span class="sxs-lookup"><span data-stu-id="ac309-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="ac309-142">El valor devuelto en  _lppProblems_ solo es válido si la llamada devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="ac309-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="ac309-143">Cuando S_OK se devuelve, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura [STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="ac309-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="ac309-144">Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor de llamadas o la puerta de enlace no deben usar ni liberar la estructura.</span><span class="sxs-lookup"><span data-stu-id="ac309-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="ac309-145">Si no se produce ningún error en la llamada, el proveedor de llamadas o la puerta de enlace debe liberar la memoria de **STnefProblemArray** llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="ac309-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac309-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ac309-146">See also</span></span>



[<span data-ttu-id="ac309-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="ac309-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="ac309-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="ac309-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="ac309-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ac309-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ac309-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="ac309-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="ac309-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="ac309-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="ac309-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ac309-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="ac309-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="ac309-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="ac309-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac309-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

