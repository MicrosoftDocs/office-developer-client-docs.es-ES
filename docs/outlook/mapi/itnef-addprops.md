---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396319"
---
# <a name="itnefaddprops"></a><span data-ttu-id="7f747-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="7f747-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="7f747-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f747-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f747-105">Permite que el proveedor de servicios de llamada o la puerta de enlace Agregar propiedades a la encapsulación de un mensaje o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7f747-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="7f747-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="7f747-106">Parameters</span></span>

 <span data-ttu-id="7f747-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7f747-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7f747-108">[entrada] Una máscara de bits de indicadores que controla cómo se incluyen o excluyen de encapsulación propiedades.</span><span class="sxs-lookup"><span data-stu-id="7f747-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="7f747-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="7f747-109">The following flags can be set:</span></span>
    
<span data-ttu-id="7f747-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="7f747-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="7f747-111">Codifica sólo las propiedades en el parámetro _lpPropList_ que forman parte de los datos adjuntos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="7f747-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="7f747-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="7f747-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="7f747-113">Codifica sólo las propiedades de los datos adjuntos especificados por el parámetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="7f747-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="7f747-114">Si el parámetro _lpvData_ no es nulo, se escriben los datos que apunta en encapsulación de los datos adjuntos en el archivo indicado por la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7f747-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="7f747-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="7f747-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="7f747-116">Codifica sólo las propiedades desde el mensaje o adjunto especificado por el parámetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="7f747-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="7f747-117">Si se establece este indicador, el valor de _lpvData_ debe ser un puntero de [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="7f747-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="7f747-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="7f747-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="7f747-119">Codifica todas las propiedades que no se especifica en el parámetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="7f747-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="7f747-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="7f747-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="7f747-121">Codifica todas las propiedades especificadas en _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="7f747-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="7f747-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="7f747-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="7f747-123">Codifica sólo las propiedades especificadas en _lpPropList_ que forman parte del propio mensaje.</span><span class="sxs-lookup"><span data-stu-id="7f747-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="7f747-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="7f747-124">_ulElemID_</span></span>
  
> <span data-ttu-id="7f747-125">[entrada] Propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de un documento adjunto, que contiene un número que identifica de forma exclusiva identifica los datos adjuntos en el mensaje de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="7f747-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="7f747-126">El parámetro _ulElemID_ se usa cuando se solicita un tratamiento especial para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7f747-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="7f747-127">El parámetro _ulElemID_ debe ser 0, a menos que se establece la marca TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7f747-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="7f747-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="7f747-128">_lpvData_</span></span>
  
> <span data-ttu-id="7f747-129">[entrada] Un puntero a datos adjuntos que usar para reemplazar los datos de los datos adjuntos especificados en _ulElemID_.</span><span class="sxs-lookup"><span data-stu-id="7f747-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="7f747-130">El parámetro _lpvData_ debe ser NULL a menos que TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF está establecida en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="7f747-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="7f747-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="7f747-131">_lpPropList_</span></span>
  
> <span data-ttu-id="7f747-132">[entrada] Un puntero a la lista de propiedades para incluir o excluir de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="7f747-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7f747-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f747-133">Return value</span></span>

<span data-ttu-id="7f747-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f747-134">S_OK</span></span> 
  
> <span data-ttu-id="7f747-135">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="7f747-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f747-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f747-136">Remarks</span></span>

<span data-ttu-id="7f747-137">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::AddProps** a las propiedades de lista para que se incluyan o excluyan del procesamiento de formato de encapsulación neutro para el transporte (TNEF) de un mensaje o un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="7f747-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="7f747-138">Mediante llamadas sucesivas, el proveedor o la puerta de enlace puede especificar una lista de propiedades para agregar y codificar o para impedir que se codifica.</span><span class="sxs-lookup"><span data-stu-id="7f747-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="7f747-139">Los proveedores y las puertas de enlace también pueden usar **AddProps** para proporcionar deben proporcionar información sobre cualquier tratamiento especial de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7f747-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="7f747-140">**AddProps** sólo se admite para objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="7f747-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="7f747-141">Tenga en cuenta que no hay codificación TNEF real ocurre para **AddProps** hasta que se llama al método [ITnef::Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="7f747-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="7f747-142">Esta funcionalidad significa que punteros pasados a **AddProps** deben permanecer válidos hasta después de que se realiza la llamada al **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="7f747-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="7f747-143">En ese momento, todos los objetos y datos pasadas con las llamadas de **AddProps** pueden publicados o liberados.</span><span class="sxs-lookup"><span data-stu-id="7f747-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7f747-144">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7f747-144">MFCMAPI reference</span></span>

<span data-ttu-id="7f747-145">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7f747-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7f747-146">**File**</span><span class="sxs-lookup"><span data-stu-id="7f747-146">**File**</span></span>|<span data-ttu-id="7f747-147">**Función**</span><span class="sxs-lookup"><span data-stu-id="7f747-147">**Function**</span></span>|<span data-ttu-id="7f747-148">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7f747-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f747-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="7f747-149">File.cpp</span></span>  <br/> |<span data-ttu-id="7f747-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="7f747-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="7f747-151">MFCMAPI usa el método **ITnef::AddProps** para copiar las propiedades de un mensaje a una secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="7f747-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f747-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f747-152">See also</span></span>



[<span data-ttu-id="7f747-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="7f747-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="7f747-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="7f747-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="7f747-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="7f747-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="7f747-156">Propiedad canónico PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="7f747-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="7f747-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f747-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="7f747-158">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="7f747-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

