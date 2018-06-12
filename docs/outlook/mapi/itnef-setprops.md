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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817992"
---
# <a name="itnefsetprops"></a><span data-ttu-id="ec9e9-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="ec9e9-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="ec9e9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec9e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec9e9-105">Establece el valor de una o más propiedades para un mensaje encapsulado o adjunto sin modificar el mensaje original o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="ec9e9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ec9e9-106">Parameters</span></span>

 <span data-ttu-id="ec9e9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec9e9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ec9e9-108">[entrada] Una máscara de bits de indicadores que controla cómo se establecen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="ec9e9-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="ec9e9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ec9e9-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="ec9e9-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="ec9e9-111">Codifica sólo las propiedades desde el mensaje o adjunto especificado por el parámetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="ec9e9-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="ec9e9-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="ec9e9-112">_ulElemID_</span></span>
  
> <span data-ttu-id="ec9e9-113">[entrada] Propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de un documento adjunto, que contiene un número que identifica de forma exclusiva identifica los datos adjuntos en el mensaje de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="ec9e9-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="ec9e9-114">_cValues_</span></span>
  
> <span data-ttu-id="ec9e9-115">[entrada] El número de valores de propiedad en la estructura de [SPropValue](spropvalue.md) indicada por el parámetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="ec9e9-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="ec9e9-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="ec9e9-116">_lpProps_</span></span>
  
> <span data-ttu-id="ec9e9-117">[entrada] Un puntero a una estructura **SPropValue** que contiene los valores de propiedad de las propiedades para establecer.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ec9e9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec9e9-118">Return value</span></span>

<span data-ttu-id="ec9e9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec9e9-119">S_OK</span></span> 
  
> <span data-ttu-id="ec9e9-120">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec9e9-121">Notas</span><span class="sxs-lookup"><span data-stu-id="ec9e9-121">Remarks</span></span>

<span data-ttu-id="ec9e9-122">Transporte proveedores, los proveedores de almacén de mensajes y las puertas de enlace llamada al método **ITnef::SetProps** para establecer las propiedades que deben incluirse en la encapsulación de un mensaje o un archivo adjunto sin modificar el mensaje o adjunto original.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="ec9e9-123">Las propiedades establecidas con esta llamada invalidar las propiedades existentes en el mensaje encapsulado.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="ec9e9-124">**SetProps** sólo se admite para objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="ec9e9-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="ec9e9-125">Cualquier número de propiedades se puede establecer con esta llamada.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ec9e9-126">No hay real la codificación TNEF para **SetProps** sucede hasta después de que se llama al método [ITnef::Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="ec9e9-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="ec9e9-127">Esta funcionalidad significa que punteros pasados **SetProps** deben siguen siendo válidos hasta después de que se realiza la llamada al **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="ec9e9-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="ec9e9-128">En ese momento, todos los objetos y datos que se pasan en **SetProps** llamadas pueden publicada el o liberados.</span><span class="sxs-lookup"><span data-stu-id="ec9e9-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec9e9-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="ec9e9-129">See also</span></span>



[<span data-ttu-id="ec9e9-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="ec9e9-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="ec9e9-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="ec9e9-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="ec9e9-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="ec9e9-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="ec9e9-133">Propiedad canónico PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="ec9e9-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="ec9e9-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ec9e9-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="ec9e9-135">ITnef: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec9e9-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

