---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435680"
---
# <a name="itneffinish"></a><span data-ttu-id="b627d-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="b627d-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="b627d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b627d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b627d-105">Finaliza el procesamiento de todas las Transport-Neutral de formato de encapsulamiento automático (TNEF) que están en cola y en espera.</span><span class="sxs-lookup"><span data-stu-id="b627d-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="b627d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b627d-106">Parameters</span></span>

 <span data-ttu-id="b627d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b627d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b627d-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b627d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b627d-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="b627d-109">_lpKey_</span></span>
  
> <span data-ttu-id="b627d-110">[salida] Puntero a la propiedad **PR_ATTACH_NUM** clave ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="b627d-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="b627d-111">El objeto de encapsulación TNEF usa esta clave para hacer coincidir datos adjuntos con su etiqueta de ubicación de datos adjuntos en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b627d-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="b627d-112">Esta clave debe ser única para cada dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="b627d-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="b627d-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="b627d-113">_lpProblem_</span></span>
  
> <span data-ttu-id="b627d-114">[salida] Puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="b627d-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="b627d-115">La **estructura STnefProblemArray** indica qué propiedades, si las hay, no se codificaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="b627d-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="b627d-116">Si se pasa NULL en el  _parámetro lpProblem,_ no se devuelve ninguna matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b627d-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b627d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b627d-117">Return value</span></span>

<span data-ttu-id="b627d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b627d-118">S_OK</span></span> 
  
> <span data-ttu-id="b627d-119">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="b627d-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b627d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b627d-120">Remarks</span></span>

<span data-ttu-id="b627d-121">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::Finish** para realizar la codificación de todas las propiedades para las que se solicitó codificación en llamadas a los [métodos ITnef::AddProps](itnef-addprops.md) e [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="b627d-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="b627d-122">Si el objeto TNEF se abrió con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx,](opentnefstreamex.md) el método **Finish** codifica las propiedades solicitadas en la secuencia de encapsulación pasada a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="b627d-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="b627d-123">Si el objeto TNEF se abrió con la marca TNEF_DECODE, el método **Finish** descodifica las propiedades de la secuencia TNEF y las vuelve a escribir en el mensaje al que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="b627d-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="b627d-124">Después de **la llamada Finish,** el puntero a la secuencia de encapsulación apunta al final de los datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="b627d-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="b627d-125">Si el proveedor o la puerta de enlace necesitan usar los datos de la secuencia TNEF después de la llamada **Finish,** debe restablecer el puntero de la secuencia al principio de los datos de la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="b627d-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="b627d-126">La implementación de TNEF informa de problemas de codificación de secuencias TNEF sin detener el **proceso finalizar.**</span><span class="sxs-lookup"><span data-stu-id="b627d-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="b627d-127">La [estructura STnefProblemArray](stnefproblemarray.md) devuelta en el parámetro  _lpProblem_ indica qué atributos TNEF o propiedades MAPI, si las hay, no se pudieron procesar.</span><span class="sxs-lookup"><span data-stu-id="b627d-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="b627d-128">El valor devuelto en el **miembro scode** de una de las estructuras **STnefProblem** contenidas en **STnefProblemArray** indica el problema específico.</span><span class="sxs-lookup"><span data-stu-id="b627d-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="b627d-129">El proveedor o la puerta de enlace pueden trabajar en la suposición de que todas las propiedades o atributos para los que **Finish** no devuelve un informe de problemas se procesaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="b627d-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="b627d-130">Si un proveedor o puerta de enlace no funciona con matrices de problemas, puede pasar NULL en  _lpProblem_; En este caso, no se devuelve ninguna matriz problemática.</span><span class="sxs-lookup"><span data-stu-id="b627d-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="b627d-131">El valor devuelto en  _lpProblem_ solo es válido si la llamada devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="b627d-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="b627d-132">Cuando S_OK se devuelve, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura **STnefProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="b627d-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="b627d-133">Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor de llamadas o la puerta de enlace no deben usar ni liberar la estructura.</span><span class="sxs-lookup"><span data-stu-id="b627d-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="b627d-134">Si no se produce ningún error en la llamada, el proveedor de llamadas o la puerta de enlace debe liberar la memoria de **STnefProblemArray** llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="b627d-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b627d-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b627d-135">MFCMAPI reference</span></span>

<span data-ttu-id="b627d-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b627d-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b627d-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b627d-137">**File**</span></span>|<span data-ttu-id="b627d-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="b627d-138">**Function**</span></span>|<span data-ttu-id="b627d-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b627d-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b627d-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="b627d-140">File.cpp</span></span>  <br/> |<span data-ttu-id="b627d-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="b627d-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="b627d-142">MFCMAPI usa el **método ITnef::Finish** para finalizar el procesamiento de la nueva secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="b627d-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b627d-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b627d-143">See also</span></span>



[<span data-ttu-id="b627d-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="b627d-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="b627d-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b627d-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b627d-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="b627d-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="b627d-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="b627d-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="b627d-148">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="b627d-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="b627d-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="b627d-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="b627d-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b627d-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="b627d-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b627d-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

