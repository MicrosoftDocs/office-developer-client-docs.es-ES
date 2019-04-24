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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348625"
---
# <a name="itnefaddprops"></a><span data-ttu-id="be13b-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="be13b-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="be13b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be13b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be13b-105">Permite al proveedor de servicios de llamada o a la puerta de enlace agregar propiedades a la encapsulación de un mensaje o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="be13b-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="be13b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="be13b-106">Parameters</span></span>

 <span data-ttu-id="be13b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be13b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="be13b-108">a Máscara de máscara de marcadores que controla cómo se incluyen o excluyen las propiedades de la encapsulación.</span><span class="sxs-lookup"><span data-stu-id="be13b-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="be13b-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="be13b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="be13b-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="be13b-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="be13b-111">Codifica solo las propiedades del parámetro _lpPropList_ que forman parte de los datos adjuntos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="be13b-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="be13b-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="be13b-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="be13b-113">Codifica solo las propiedades de los datos adjuntos especificados por el parámetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="be13b-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="be13b-114">Si el parámetro _lpvData_ no es null, los datos a los que se apunta se escriben en la encapsulación de los datos adjuntos en el archivo indicado por la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="be13b-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="be13b-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="be13b-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="be13b-116">Codifica solo las propiedades desde el mensaje o datos adjuntos especificados por el parámetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="be13b-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="be13b-117">Si se establece esta marca, el valor de _lpvData_ debe ser un puntero [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="be13b-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="be13b-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="be13b-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="be13b-119">Codifica todas las propiedades no especificadas en el parámetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="be13b-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="be13b-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="be13b-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="be13b-121">Codifica todas las propiedades especificadas en _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="be13b-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="be13b-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="be13b-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="be13b-123">Codifica sólo las propiedades especificadas en _lpPropList_ que forman parte del propio mensaje.</span><span class="sxs-lookup"><span data-stu-id="be13b-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="be13b-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="be13b-124">_ulElemID_</span></span>
  
> <span data-ttu-id="be13b-125">a Propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de datos adjuntos, que contiene un número que identifica de forma única los datos adjuntos en su mensaje primario.</span><span class="sxs-lookup"><span data-stu-id="be13b-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="be13b-126">El parámetro _ulElemID_ se usa cuando se solicita un tratamiento especial para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="be13b-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="be13b-127">El parámetro _ulElemID_ debe ser 0 a menos que se establezca el marcador TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="be13b-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="be13b-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="be13b-128">_lpvData_</span></span>
  
> <span data-ttu-id="be13b-129">a Un puntero a datos de datos adjuntos que se usan para reemplazar los datos de los datos adjuntos especificados en _ulElemID_.</span><span class="sxs-lookup"><span data-stu-id="be13b-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="be13b-130">El parámetro _lpvData_ debe ser nulo a menos que se establezca TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="be13b-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="be13b-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="be13b-131">_lpPropList_</span></span>
  
> <span data-ttu-id="be13b-132">a Puntero a la lista de propiedades que se van a incluir o excluir de la encapsulación.</span><span class="sxs-lookup"><span data-stu-id="be13b-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be13b-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be13b-133">Return value</span></span>

<span data-ttu-id="be13b-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="be13b-134">S_OK</span></span> 
  
> <span data-ttu-id="be13b-135">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="be13b-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be13b-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be13b-136">Remarks</span></span>

<span data-ttu-id="be13b-137">Los proveedores de transporte, los proveedores de almacenamiento de mensajes y las puertas de enlace llaman al método **ITnef:: AddProps** para enumerar las propiedades que se van a incluir o excluir del procesamiento de formato de encapsulación neutro para el transporte (TNEF) de un mensaje o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="be13b-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="be13b-138">Mediante llamadas sucesivas, el proveedor o la puerta de enlace pueden especificar una lista de propiedades para agregar y codificar o excluir de la codificación.</span><span class="sxs-lookup"><span data-stu-id="be13b-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="be13b-139">Los proveedores y las puertas de enlace también pueden usar **AddProps** para proporcionar información sobre los datos adjuntos de tratamiento especial que se deben dar.</span><span class="sxs-lookup"><span data-stu-id="be13b-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="be13b-140">**AddProps** solo se admite para los objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="be13b-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="be13b-141">Tenga en cuenta que no se produce ninguna codificación TNEF real para **AddProps** hasta que se llama al método [ITnef:: Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="be13b-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="be13b-142">Esta funcionalidad significa que los punteros pasados a **AddProps** deben seguir siendo válidos hasta que se realice la llamada a **Finish** .</span><span class="sxs-lookup"><span data-stu-id="be13b-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="be13b-143">En ese momento, se pueden liberar o liberar todos los objetos y datos que se pasan con llamadas de **AddProps** .</span><span class="sxs-lookup"><span data-stu-id="be13b-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="be13b-144">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="be13b-144">MFCMAPI reference</span></span>

<span data-ttu-id="be13b-145">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="be13b-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="be13b-146">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="be13b-146">**File**</span></span>|<span data-ttu-id="be13b-147">**Función**</span><span class="sxs-lookup"><span data-stu-id="be13b-147">**Function**</span></span>|<span data-ttu-id="be13b-148">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="be13b-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="be13b-149">Archivo. cpp</span><span class="sxs-lookup"><span data-stu-id="be13b-149">File.cpp</span></span>  <br/> |<span data-ttu-id="be13b-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="be13b-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="be13b-151">MFCMAPI usa el método **ITnef:: AddProps** para copiar las propiedades de un mensaje en una secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="be13b-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be13b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="be13b-152">See also</span></span>



[<span data-ttu-id="be13b-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="be13b-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="be13b-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="be13b-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="be13b-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="be13b-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="be13b-156">Propiedad canónica PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="be13b-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="be13b-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be13b-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="be13b-158">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="be13b-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

