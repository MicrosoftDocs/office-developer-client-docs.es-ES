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
# <a name="itnefsetprops"></a><span data-ttu-id="9a4f2-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="9a4f2-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="9a4f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a4f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a4f2-105">Establece el valor de una o más propiedades para un mensaje encapsulado o datos adjuntos sin modificar el mensaje o los datos adjuntos originales.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="9a4f2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a4f2-106">Parameters</span></span>

 <span data-ttu-id="9a4f2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a4f2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9a4f2-108">[in] Máscara de bits de marcas que controla cómo se establecen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="9a4f2-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="9a4f2-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9a4f2-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="9a4f2-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="9a4f2-111">Codifica solo las propiedades del mensaje o los datos adjuntos especificados por _el parámetro ulElemID._</span><span class="sxs-lookup"><span data-stu-id="9a4f2-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="9a4f2-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="9a4f2-112">_ulElemID_</span></span>
  
> <span data-ttu-id="9a4f2-113">[in] Propiedad de **PR_ATTACH_NUM** datos adjuntos ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), que contiene un número que identifica de forma única los datos adjuntos en su mensaje primario.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="9a4f2-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="9a4f2-114">_cValues_</span></span>
  
> <span data-ttu-id="9a4f2-115">[in] El número de valores de propiedad en la [estructura SPropValue](spropvalue.md) a la que apunta el _parámetro lpProps._</span><span class="sxs-lookup"><span data-stu-id="9a4f2-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="9a4f2-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="9a4f2-116">_lpProps_</span></span>
  
> <span data-ttu-id="9a4f2-117">[in] Puntero a una **estructura SPropValue** que contiene los valores de propiedad de las propiedades que se establecerán.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9a4f2-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a4f2-118">Return value</span></span>

<span data-ttu-id="9a4f2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a4f2-119">S_OK</span></span> 
  
> <span data-ttu-id="9a4f2-120">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a4f2-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a4f2-121">Remarks</span></span>

<span data-ttu-id="9a4f2-122">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::SetProps** para establecer las propiedades que se incluirán en la encapsulación de un mensaje o datos adjuntos sin modificar el mensaje o los datos adjuntos originales.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="9a4f2-123">Las propiedades establecidas con esta llamada invalidan las propiedades existentes en el mensaje encapsulado.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="9a4f2-124">**SetProps** solo se admite para objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="9a4f2-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="9a4f2-125">Cualquier número de propiedades se puede establecer con esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9a4f2-126">No se produce ninguna codificación TNEF real para **SetProps** hasta después de llamar al método [ITnef::Finish.](itnef-finish.md)</span><span class="sxs-lookup"><span data-stu-id="9a4f2-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="9a4f2-127">Esta funcionalidad significa que los punteros que se pasan a **SetProps** deben seguir siendo válidos hasta después de realizar la llamada a **Finish.**</span><span class="sxs-lookup"><span data-stu-id="9a4f2-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="9a4f2-128">En ese momento, todos los objetos y datos pasados a **llamadas SetProps** se pueden liberar o liberar.</span><span class="sxs-lookup"><span data-stu-id="9a4f2-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a4f2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a4f2-129">See also</span></span>



[<span data-ttu-id="9a4f2-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="9a4f2-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="9a4f2-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="9a4f2-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="9a4f2-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="9a4f2-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="9a4f2-133">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="9a4f2-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="9a4f2-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9a4f2-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9a4f2-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a4f2-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

