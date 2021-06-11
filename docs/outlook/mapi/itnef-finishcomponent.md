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
# <a name="itneffinishcomponent"></a><span data-ttu-id="dea76-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="dea76-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="dea76-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dea76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dea76-105">Procesa componentes individuales de un mensaje uno a uno en una secuencia Transport-Neutral de formato de encapsulación (TNEF).</span><span class="sxs-lookup"><span data-stu-id="dea76-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="dea76-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dea76-106">Parameters</span></span>

 <span data-ttu-id="dea76-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dea76-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dea76-108">[in] Máscara de bits de marcas que controla el componente que se va a finalizar.</span><span class="sxs-lookup"><span data-stu-id="dea76-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="dea76-109">Debe establecerse una u otra de las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="dea76-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="dea76-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="dea76-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="dea76-111">El procesamiento se finalizará para un objeto de datos adjuntos; el  _parámetro ulComponentID_ contiene la **propiedad PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dea76-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="dea76-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="dea76-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="dea76-113">El procesamiento se finalizará para un objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="dea76-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="dea76-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="dea76-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="dea76-115">[in] 0 para indicar el procesamiento de un mensaje o la **PR_ATTACH_NUM** propiedad de un archivo adjunto que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="dea76-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="dea76-116">Si la TNEF_COMPONENT_MESSAGE se establece en el  _parámetro ulFlags,_  _ulComponentID_ debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="dea76-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="dea76-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="dea76-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="dea76-118">[in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene etiquetas de propiedades que identifican las propiedades pasadas en el _parámetro lpCustomProps._</span><span class="sxs-lookup"><span data-stu-id="dea76-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="dea76-119">Debe haber una correspondencia uno a uno entre cada valor de propiedad en _lpCustomProps_ y una etiqueta de propiedad en el _parámetro lpCustomPropList._</span><span class="sxs-lookup"><span data-stu-id="dea76-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="dea76-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="dea76-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="dea76-121">[in] Puntero a una [estructura SPropValue](spropvalue.md) que contiene valores de propiedad para las propiedades que se codifican.</span><span class="sxs-lookup"><span data-stu-id="dea76-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="dea76-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="dea76-122">_lpPropList_</span></span>
  
> <span data-ttu-id="dea76-123">[in] Puntero a una **estructura SPropTagArray** que contiene etiquetas de propiedad para las propiedades que se codifican.</span><span class="sxs-lookup"><span data-stu-id="dea76-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="dea76-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="dea76-124">_lppProblems_</span></span>
  
> <span data-ttu-id="dea76-125">[salida] Puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="dea76-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="dea76-126">La **estructura STnefProblemArray** indica qué propiedades, si las hay, no se codificaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="dea76-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="dea76-127">Si se pasa NULL en el parámetro  _lppProblems,_ no se devuelve ninguna matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="dea76-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dea76-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dea76-128">Return value</span></span>

<span data-ttu-id="dea76-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="dea76-129">S_OK</span></span> 
  
> <span data-ttu-id="dea76-130">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="dea76-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dea76-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dea76-131">Remarks</span></span>

<span data-ttu-id="dea76-132">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::FinishComponent** para realizar el procesamiento de TNEF para un componente, ya sea un mensaje o un dato adjunto, como indica la marca establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="dea76-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="dea76-133">Para habilitar el procesamiento de componentes, el proveedor de llamadas o la puerta de enlace pasan la marca TNEF_COMPONENT_ENCODING en  _ulFlags_ para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) que abrió el objeto para recibir codificación.</span><span class="sxs-lookup"><span data-stu-id="dea76-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="dea76-134">El paso de valores en los parámetros _lpCustomPropList_ y _lpCustomProps_ realiza una codificación de componentes equivalente a la realizada por el [método ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="dea76-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="dea76-135">Pasar un valor en el parámetro  _lpPropList_ realiza una codificación de componentes equivalente a la realizada por el método [ITnef::AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE establecida en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="dea76-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="dea76-136">Pasar estos valores permite realizar codificaciones con una sola llamada en lugar de varias llamadas.</span><span class="sxs-lookup"><span data-stu-id="dea76-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="dea76-137">La implementación de TNEF informa de problemas de codificación de secuencias TNEF sin detener el **proceso FinishComponent.**</span><span class="sxs-lookup"><span data-stu-id="dea76-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="dea76-138">La **estructura STnefProblemArray** devuelta en  _lppProblems_ indica qué atributos TNEF o propiedades MAPI, si las hubiera, no se pudieron procesar.</span><span class="sxs-lookup"><span data-stu-id="dea76-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="dea76-139">El valor devuelto en el **miembro scode** de una de las estructuras **STnefProblem** contenidas en **STnefProblemArray** indica el problema específico.</span><span class="sxs-lookup"><span data-stu-id="dea76-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="dea76-140">El proveedor o la puerta de enlace pueden funcionar en la suposición de que todas las propiedades o atributos para los que **FinishComponent** no devuelve un informe de problemas se procesaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="dea76-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="dea76-141">Si un proveedor o puerta de enlace no funciona con matrices problemáticas, puede pasar NULL en  _lppProblems_; en este caso, no se devuelve ninguna matriz de problemas.</span><span class="sxs-lookup"><span data-stu-id="dea76-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="dea76-142">El valor devuelto en  _lppProblems_ solo es válido si la llamada devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="dea76-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="dea76-143">Cuando S_OK, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura [STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="dea76-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="dea76-144">Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor de llamadas o la puerta de enlace no debe usar ni liberar la estructura.</span><span class="sxs-lookup"><span data-stu-id="dea76-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="dea76-145">Si no se produce ningún error en la llamada, el proveedor de llamadas o la puerta de enlace debe liberar la memoria de **STnefProblemArray** llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="dea76-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dea76-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="dea76-146">See also</span></span>



[<span data-ttu-id="dea76-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="dea76-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="dea76-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="dea76-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="dea76-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dea76-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dea76-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="dea76-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="dea76-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="dea76-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="dea76-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="dea76-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="dea76-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="dea76-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="dea76-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dea76-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

