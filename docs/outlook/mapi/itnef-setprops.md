---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430794"
---
# <a name="itnefsetprops"></a><span data-ttu-id="4cf03-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="4cf03-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="4cf03-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cf03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cf03-105">Establece el valor de una o varias propiedades para un mensaje o datos adjuntos encapsulados sin modificar el mensaje o los datos adjuntos originales.</span><span class="sxs-lookup"><span data-stu-id="4cf03-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="4cf03-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4cf03-106">Parameters</span></span>

 <span data-ttu-id="4cf03-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cf03-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4cf03-108">a Máscara de máscara de marcadores que controla cómo se establecen los valores de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4cf03-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="4cf03-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="4cf03-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4cf03-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="4cf03-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="4cf03-111">Codifica solo las propiedades desde el mensaje o datos adjuntos especificados por el parámetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="4cf03-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="4cf03-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="4cf03-112">_ulElemID_</span></span>
  
> <span data-ttu-id="4cf03-113">a Propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de datos adjuntos, que contiene un número que identifica de forma única los datos adjuntos en su mensaje primario.</span><span class="sxs-lookup"><span data-stu-id="4cf03-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="4cf03-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="4cf03-114">_cValues_</span></span>
  
> <span data-ttu-id="4cf03-115">a El número de valores de propiedad de la estructura [SPropValue](spropvalue.md) apuntado por el parámetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="4cf03-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="4cf03-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="4cf03-116">_lpProps_</span></span>
  
> <span data-ttu-id="4cf03-117">a Un puntero a una estructura **SPropValue** que contiene los valores de propiedad de las propiedades que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="4cf03-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4cf03-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cf03-118">Return value</span></span>

<span data-ttu-id="4cf03-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cf03-119">S_OK</span></span> 
  
> <span data-ttu-id="4cf03-120">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="4cf03-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4cf03-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4cf03-121">Remarks</span></span>

<span data-ttu-id="4cf03-122">Los proveedores de transporte, los proveedores de almacenamiento de mensajes y las puertas de enlace llaman al método **ITnef:: SetProps** para establecer las propiedades que se incluirán en la encapsulación de un mensaje o datos adjuntos sin modificar el mensaje original o los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4cf03-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="4cf03-123">Las propiedades establecidas con esta llamada reemplazan las propiedades existentes en el mensaje encapsulado.</span><span class="sxs-lookup"><span data-stu-id="4cf03-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="4cf03-124">**SetProps** solo se admite para los objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="4cf03-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="4cf03-125">Se puede establecer cualquier número de propiedades con esta llamada.</span><span class="sxs-lookup"><span data-stu-id="4cf03-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4cf03-126">No se produce ninguna codificación TNEF real para **SetProps** hasta que se llama al método [ITnef:: Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="4cf03-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="4cf03-127">Esta funcionalidad significa que los punteros pasados a **SetProps** deben seguir siendo válidos hasta que se realice la llamada a **Finish** .</span><span class="sxs-lookup"><span data-stu-id="4cf03-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="4cf03-128">En ese momento, se pueden liberar o liberar todos los objetos y datos que se pasan a llamadas **SetProps** .</span><span class="sxs-lookup"><span data-stu-id="4cf03-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cf03-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="4cf03-129">See also</span></span>



[<span data-ttu-id="4cf03-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="4cf03-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="4cf03-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="4cf03-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="4cf03-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="4cf03-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="4cf03-133">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="4cf03-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="4cf03-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4cf03-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="4cf03-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4cf03-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

