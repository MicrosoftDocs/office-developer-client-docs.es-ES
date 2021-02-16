---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5e36cf12b7a5b1643f5a0ec97223030718195a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433440"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="7f6df-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="7f6df-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="7f6df-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f6df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f6df-105">Recupera el nivel de acceso y el estado de una o varias de las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="7f6df-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="7f6df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f6df-106">Parameters</span></span>

 <span data-ttu-id="7f6df-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="7f6df-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="7f6df-p101">[entrada, salida] En la entrada, una matriz de etiquetas de propiedad que indican las propiedades para el que se va a recuperar los niveles de acceso y el estado; de lo contrario, un puntero a un valor NULL, que indica que **HrGetPropAccess** debe recuperar los niveles de acceso y el estado de todas las propiedades. En la salida, se recupera una matriz de etiquetas de propiedad para los indicadores de acceso y el estado. Las marcas se almacenan en la matriz que apunta el par�metro  _lprgulAccess_.</span><span class="sxs-lookup"><span data-stu-id="7f6df-p101">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties. On output, an array of property tags for which access and status flags were retrieved. The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="7f6df-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="7f6df-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="7f6df-p102">[out] Un puntero a una matriz de m�scaras de bits de indicador. Cada m�scara de bits indica los niveles de acceso, estado o ambos, para cada una de las propiedades identificadas en la matriz que apunta el par�metro  _lpPropTagArray_. Las dos matrices son posici�n en que la primera m�scara de bits que  _lprgulAccess_ puntos que describe la primera propiedad que  _lpPropTagArray_ apunta a, y as� sucesivamente. Para cada etiqueta de propiedad, se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="7f6df-p102">[out] A pointer to an array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter. The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="7f6df-116">**Indicador de nivel de acceso**</span><span class="sxs-lookup"><span data-stu-id="7f6df-116">**Access-level flag**</span></span>|<span data-ttu-id="7f6df-117">**Indicador de estado**</span><span class="sxs-lookup"><span data-stu-id="7f6df-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f6df-118">IPROP_READONLY, que indica que no se puede modificar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7f6df-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="7f6df-119">IPROP_CLEAN, que indica que la propiedad no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="7f6df-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="7f6df-120">IPROP_READWRITE, que indica que se puede modificar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7f6df-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="7f6df-121">IPROP_DIRTY, que indica que se ha modificado la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7f6df-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="7f6df-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f6df-122">Return value</span></span>

<span data-ttu-id="7f6df-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f6df-123">S_OK</span></span> 
  
> <span data-ttu-id="7f6df-124">Los indicadores de estado y el nivel de acceso para las propiedades correctamente se han devuelto.</span><span class="sxs-lookup"><span data-stu-id="7f6df-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f6df-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f6df-125">Remarks</span></span>

<span data-ttu-id="7f6df-126">El m�todo **IPropData::HrGetPropAccess** recupera un conjunto de marcadores que indica el nivel de acceso y el estado de una o m�s propiedades.</span><span class="sxs-lookup"><span data-stu-id="7f6df-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7f6df-127">Notas para autores de llamada:</span><span class="sxs-lookup"><span data-stu-id="7f6df-127">Notes to callers:</span></span>

<span data-ttu-id="7f6df-128">Puede usar **HrGetPropAccess** para los siguientes prop�sitos:</span><span class="sxs-lookup"><span data-stu-id="7f6df-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="7f6df-129">Para determinar si un cliente cambia o elimina una propiedad de escritura.</span><span class="sxs-lookup"><span data-stu-id="7f6df-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="7f6df-130">Para evitar que a un cliente cambiar o eliminar una propiedad mediante el uso de los m�todos de [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6df-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="7f6df-p103">Si se ha eliminado una de las propiedades en la matriz de etiqueta de propiedad que se�ala  _lppPropTagArray_, **HrGetPropAccess** establece la entrada de la matriz en 0 en el resultado. Si se establece  _lppPropTagArray_ en NULL y una de las propiedades del objeto se ha eliminado, se devuelve la propiedad eliminada en la matriz.</span><span class="sxs-lookup"><span data-stu-id="7f6df-p103">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output. If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="7f6df-p104">Si se ha modificado una propiedad, su marca IPROP_DIRTY se establece en la entrada correspondiente en la matriz que se�ala  _lprgulAccess_ en. Se establecer� IPROP_READONLY ni IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="7f6df-p104">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to. Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="7f6df-135">Si una propiedad no se ha modificado o eliminado, se establecer� el indicador IPROP_READONLY o IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="7f6df-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f6df-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7f6df-136">See also</span></span>



[<span data-ttu-id="7f6df-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="7f6df-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="7f6df-138">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7f6df-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

