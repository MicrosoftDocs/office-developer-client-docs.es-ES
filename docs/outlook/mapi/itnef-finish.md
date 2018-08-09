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
ms.openlocfilehash: 2b95e0dd62d83dd83a064ee4627811fcb24af921
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817998"
---
# <a name="itneffinish"></a><span data-ttu-id="ff7a2-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="ff7a2-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="ff7a2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff7a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff7a2-105">Termina de procesamiento para todas las operaciones de formato de encapsulación neutro para el transporte (TNEF) que se ponen en cola y a la espera.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="ff7a2-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ff7a2-106">Parameters</span></span>

 <span data-ttu-id="ff7a2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff7a2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ff7a2-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ff7a2-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="ff7a2-109">_lpKey_</span></span>
  
> <span data-ttu-id="ff7a2-110">[out] Un puntero a la propiedad clave **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="ff7a2-111">El objeto de encapsulación TNEF utiliza esta clave para que coincida con un archivo adjunto a la etiqueta de colocación de datos adjuntos en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="ff7a2-112">Esta clave debe ser única para cada dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="ff7a2-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="ff7a2-113">_lpProblem_</span></span>
  
> <span data-ttu-id="ff7a2-114">[out] Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="ff7a2-115">La estructura **STnefProblemArray** indica qué propiedades, si hay alguna, no codificados correctamente.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="ff7a2-116">Si se pasa NULL en el parámetro _lpProblem_ , no hay ninguna matriz de problema (propiedad) se devuelve.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff7a2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff7a2-117">Return value</span></span>

<span data-ttu-id="ff7a2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff7a2-118">S_OK</span></span> 
  
> <span data-ttu-id="ff7a2-119">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff7a2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff7a2-120">Remarks</span></span>

<span data-ttu-id="ff7a2-121">Los proveedores, los proveedores de almacén de mensajes y el método **ITnef::Finish** para llevar a cabo la codificación de todas las propiedades de la codificación que se solicitó en las llamadas a los métodos [ITnef::AddProps](itnef-addprops.md) y [ITnef::SetProps](itnef-setprops.md) de llamada de las puertas de enlace de transporte.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="ff7a2-122">Si el objeto TNEF se abrió con la marca TNEF_ENCODE para la función de [OpenTnefStreamEx](opentnefstreamex.md) o [OpenTnefStream](opentnefstream.md) , el método **de finalización** codifica las propiedades solicitadas en el flujo de encapsulación pasado a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="ff7a2-123">Si el objeto TNEF se abrió con la marca TNEF_DECODE, el método **de finalización** descodifica las propiedades de la secuencia TNEF y escriba de nuevo en el mensaje que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="ff7a2-124">Después de la llamada **de finalización** , el puntero a la secuencia de encapsulación apunta al final de los datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="ff7a2-125">Si la puerta de enlace o un proveedor necesita usar los datos de secuencia TNEF después de la **finalización** de llamadas, debe restablecer el puntero de secuencia al principio de los datos de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="ff7a2-126">La implementación de TNEF informa de problemas de codificación de secuencia TNEF sin detener el proceso **de finalización** .</span><span class="sxs-lookup"><span data-stu-id="ff7a2-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="ff7a2-127">La estructura de [STnefProblemArray](stnefproblemarray.md) devuelta en el parámetro _lpProblem_ indica qué atributos TNEF o las propiedades MAPI, si hay alguna, no se podrían procesar.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="ff7a2-128">El valor devuelto en el miembro **scode** de una de las estructuras de **STnefProblem** contenidos en **STnefProblemArray** indica el problema específico.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="ff7a2-129">El proveedor o la puerta de enlace puede trabajar en la suposición de que todas las propiedades o atributos para el que **Finalizar** no devuelve un informe de problemas se procesaran correctamente.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="ff7a2-130">Si un proveedor o una puerta de enlace no funciona con matrices de problema, puede pasar NULL en _lpProblem_; en este caso, no se devuelve la matriz de ningún problema.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="ff7a2-131">El valor devuelto en _lpProblem_ es válido sólo si la llamada devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="ff7a2-132">Cuando se devuelve S_OK, el proveedor o la puerta de enlace debe comprobar los valores devueltos en la estructura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="ff7a2-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="ff7a2-133">Si se produce un error en la llamada, no se rellena la estructura **STnefProblemArray** y el proveedor o la puerta de enlace realiza la llamada no debe utilizar o libre la estructura.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="ff7a2-134">Si se produce ningún error en la llamada, el proveedor o la puerta de enlace realiza la llamada debe liberar la memoria para el **STnefProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ff7a2-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff7a2-135">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff7a2-135">MFCMAPI reference</span></span>

<span data-ttu-id="ff7a2-136">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff7a2-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ff7a2-137">**File**</span></span>|<span data-ttu-id="ff7a2-138">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ff7a2-138">**Function**</span></span>|<span data-ttu-id="ff7a2-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ff7a2-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff7a2-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="ff7a2-140">File.cpp</span></span>  <br/> |<span data-ttu-id="ff7a2-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="ff7a2-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="ff7a2-142">MFCMAPI, utiliza el método **ITnef::Finish** para finalizar el procesamiento de la nueva secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="ff7a2-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff7a2-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff7a2-143">See also</span></span>



[<span data-ttu-id="ff7a2-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="ff7a2-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="ff7a2-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ff7a2-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ff7a2-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="ff7a2-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="ff7a2-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="ff7a2-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="ff7a2-148">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="ff7a2-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="ff7a2-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="ff7a2-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="ff7a2-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff7a2-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="ff7a2-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ff7a2-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

