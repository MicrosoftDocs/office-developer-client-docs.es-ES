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
ms.openlocfilehash: 0242015680f11e5be6ae8ea9987e5778dc7cdf05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594365"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="49800-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="49800-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="49800-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49800-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49800-105">Procesa los componentes individuales de un mensaje de uno a la vez en una secuencia de formato de encapsulación neutro para el transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="49800-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="49800-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="49800-106">Parameters</span></span>

 <span data-ttu-id="49800-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="49800-107">_ulFlags_</span></span>
  
> <span data-ttu-id="49800-108">[entrada] Una máscara de bits de indicadores que controla qué componente va a ser terminado.</span><span class="sxs-lookup"><span data-stu-id="49800-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="49800-109">Se debe establecer uno u otro de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="49800-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="49800-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="49800-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="49800-111">Va a ser terminado el procesamiento para un objeto attachment; el parámetro _ulComponentID_ contiene la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="49800-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="49800-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="49800-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="49800-113">Va a ser terminado de procesamiento para un objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="49800-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="49800-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="49800-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="49800-115">[entrada] 0 para indicar el procesamiento para un mensaje o la propiedad **PR_ATTACH_NUM** de datos adjuntos que va a procesar.</span><span class="sxs-lookup"><span data-stu-id="49800-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="49800-116">Si se establece la marca TNEF_COMPONENT_MESSAGE en el parámetro _ulFlags_ , _ulComponentID_ debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="49800-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="49800-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="49800-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="49800-118">[entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad que identifican las propiedades que se pasa en el parámetro _lpCustomProps_ .</span><span class="sxs-lookup"><span data-stu-id="49800-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="49800-119">Debe haber una correspondencia uno a uno entre cada valor de la propiedad en _lpCustomProps_ y una etiqueta de propiedad en el parámetro _lpCustomPropList_ .</span><span class="sxs-lookup"><span data-stu-id="49800-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="49800-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="49800-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="49800-121">[entrada] Un puntero a una estructura [SPropValue](spropvalue.md) que contiene los valores de propiedad para las propiedades codificar.</span><span class="sxs-lookup"><span data-stu-id="49800-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="49800-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="49800-122">_lpPropList_</span></span>
  
> <span data-ttu-id="49800-123">[entrada] Un puntero a una estructura de **elemento SPropTagArray** que contiene las etiquetas de propiedad para las propiedades codificar.</span><span class="sxs-lookup"><span data-stu-id="49800-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="49800-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="49800-124">_lppProblems_</span></span>
  
> <span data-ttu-id="49800-125">[out] Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="49800-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="49800-126">La estructura **STnefProblemArray** indica qué propiedades, si hay alguna, no codificados correctamente.</span><span class="sxs-lookup"><span data-stu-id="49800-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="49800-127">Si se pasa NULL en el parámetro _lppProblems_ , no hay ninguna matriz de problema (propiedad) se devuelve.</span><span class="sxs-lookup"><span data-stu-id="49800-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="49800-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49800-128">Return value</span></span>

<span data-ttu-id="49800-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="49800-129">S_OK</span></span> 
  
> <span data-ttu-id="49800-130">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="49800-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49800-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49800-131">Remarks</span></span>

<span data-ttu-id="49800-132">Los proveedores, los proveedores de almacén de mensajes y las puertas de enlace llamada al método **ITnef::FinishComponent** para llevar a cabo TNEF de procesamiento para un componente, un mensaje o un archivo adjunto, indicada por el marcador establecido en el parámetro _ulFlags_ de transporte.</span><span class="sxs-lookup"><span data-stu-id="49800-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="49800-133">Para que el procesamiento de componente esté habilitada, el proveedor o la puerta de enlace que llama pase la marca TNEF_COMPONENT_ENCODING _ulFlags_ para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) que abre el objeto para recibir la codificación.</span><span class="sxs-lookup"><span data-stu-id="49800-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="49800-134">Pasar valores en los parámetros _lpCustomPropList_ y _lpCustomProps_ realiza componente codificación equivalente a la se realiza mediante el método [ITnef::SetProps](itnef-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="49800-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="49800-135">Pasar un valor en el parámetro _lpPropList_ realiza el equivalente de codificación de componente para el se realiza en el método [ITnef::AddProps](itnef-addprops.md) con el indicador TNEF_PROP_INCLUDE establecido en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="49800-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="49800-136">Pasar estos valores le permite realizar codificaciones con una única llamada en lugar de varias llamadas.</span><span class="sxs-lookup"><span data-stu-id="49800-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="49800-137">La implementación de TNEF informa de problemas de codificación de secuencia TNEF sin detener el proceso de **FinishComponent** .</span><span class="sxs-lookup"><span data-stu-id="49800-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="49800-138">La estructura de **STnefProblemArray** devuelta en _lppProblems_ indica qué atributos TNEF o las propiedades MAPI, si hay alguna, no se podrían procesar.</span><span class="sxs-lookup"><span data-stu-id="49800-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="49800-139">El valor devuelto en el miembro **scode** de una de las estructuras de **STnefProblem** contenidos en **STnefProblemArray** indica el problema específico.</span><span class="sxs-lookup"><span data-stu-id="49800-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="49800-140">El proveedor o la puerta de enlace puede trabajar en la suposición de que todas las propiedades o atributos para el que **FinishComponent** no devuelve un informe de problemas se procesaran correctamente.</span><span class="sxs-lookup"><span data-stu-id="49800-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="49800-141">Si un proveedor o una puerta de enlace no funciona con matrices de problema, puede pasar NULL en _lppProblems_; en este caso, no se devuelve la matriz de ningún problema.</span><span class="sxs-lookup"><span data-stu-id="49800-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="49800-142">El valor devuelto en _lppProblems_ es válido sólo si la llamada devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="49800-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="49800-143">Cuando se devuelve S_OK, el proveedor o la puerta de enlace debe comprobar los valores devueltos en la estructura [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="49800-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="49800-144">Si se produce un error en la llamada, no se rellena la estructura de **STnefProblemArray** , y el proveedor o la puerta de enlace realiza la llamada no debe utilizar o libre la estructura.</span><span class="sxs-lookup"><span data-stu-id="49800-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="49800-145">Si se produce ningún error en la llamada, el proveedor o la puerta de enlace realiza la llamada debe liberar la memoria para el **STnefProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="49800-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49800-146">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="49800-146">See also</span></span>



[<span data-ttu-id="49800-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="49800-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="49800-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="49800-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="49800-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="49800-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="49800-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="49800-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="49800-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="49800-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="49800-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="49800-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="49800-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="49800-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="49800-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49800-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

