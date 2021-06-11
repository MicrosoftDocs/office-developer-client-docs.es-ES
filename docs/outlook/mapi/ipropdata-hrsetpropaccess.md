---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9e443302e49bad4a586b657a6de298dafbeefab4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437857"
---
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="021fb-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="021fb-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="021fb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="021fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="021fb-105">Establece el nivel de acceso o el estado de una o varias de las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="021fb-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="021fb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="021fb-106">Parameters</span></span>

 <span data-ttu-id="021fb-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="021fb-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="021fb-108">[entrada] Un puntero a una matriz de etiquetas de propiedad que indican las propiedades que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="021fb-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="021fb-109">_rgulAccess_</span><span class="sxs-lookup"><span data-stu-id="021fb-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="021fb-p101">[entrada] Una matriz de m�scaras de bits de indicador. Cada m�scara de bits indica los niveles de acceso, estado o ambos, para cada una de las propiedades identificadas en la matriz que se�ala el par�metro  _lpPropTagArray_. Las dos matrices son posici�n en que la primera m�scara de bits en  _rgulAccess_ describe la primera propiedad que se�ala  _lpPropTagArray_, y as� sucesivamente. Para cada etiqueta de propiedad, se puede establecer un indicador de nivel de acceso y el indicador de estado de uno. En la siguiente tabla muestra los indicadores de posibles.</span><span class="sxs-lookup"><span data-stu-id="021fb-p101">[in] An array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to. The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, one access-level flag and one status flag can be set. The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="021fb-115">**Indicador de nivel de acceso**</span><span class="sxs-lookup"><span data-stu-id="021fb-115">**Access-level flag**</span></span>|<span data-ttu-id="021fb-116">**Indicador de estado**</span><span class="sxs-lookup"><span data-stu-id="021fb-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="021fb-117">IPROP_READONLY, que indica que no se puede modificar la propiedad</span><span class="sxs-lookup"><span data-stu-id="021fb-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="021fb-118">IPROP_CLEAN, que indica que la propiedad no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="021fb-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="021fb-119">IPROP_READWRITE, que indica que se puede modificar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="021fb-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="021fb-120">IPROP_DIRTY, que indica que se ha modificado la propiedad.</span><span class="sxs-lookup"><span data-stu-id="021fb-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="021fb-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="021fb-121">Return value</span></span>

<span data-ttu-id="021fb-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="021fb-122">S_OK</span></span> 
  
> <span data-ttu-id="021fb-123">Los indicadores de estado y el nivel de acceso se han establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="021fb-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="021fb-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="021fb-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="021fb-125">Se intent� establecer una propiedad en un objeto de s�lo lectura o un objeto para el que el llamador no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="021fb-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="021fb-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="021fb-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="021fb-127">El par�metro  _rgulAccess_ contiene una combinaci�n no v�lida de indicadores, como IPROP_READONLY y IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="021fb-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="021fb-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="021fb-128">Remarks</span></span>

<span data-ttu-id="021fb-p102">El m�todo **IPropData::HrSetPropAccess** cambia el nivel de acceso y el estado de las propiedades que se identifican mediante las etiquetas de propiedad en la estructura del [elemento SPropTagArray](sproptagarray.md) que apunta el par�metro  _lpPropTagArray_. Para cada propiedad, hay una entrada correspondiente en la matriz  _rgulAccess_. La entrada se puede establecer en una marca que indica el nivel de acceso de la propiedad y otra marca que indica su estado.</span><span class="sxs-lookup"><span data-stu-id="021fb-p102">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter. For each property, there is a corresponding entry in the  _rgulAccess_ array. The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="021fb-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="021fb-132">Notes to callers</span></span>

<span data-ttu-id="021fb-133">Utilice **HrSetPropAccess** para determinar cuando cambia un valor de esa propiedad y cambiar el nivel de acceso para una o varias de las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="021fb-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="021fb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="021fb-134">See also</span></span>



[<span data-ttu-id="021fb-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="021fb-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="021fb-136">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="021fb-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

