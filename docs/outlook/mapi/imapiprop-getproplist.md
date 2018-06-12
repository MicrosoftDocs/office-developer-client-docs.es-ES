---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0457007334ad8cc69dade3abd5859dd0d5f7af7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817406"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="3193f-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="3193f-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="3193f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3193f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3193f-105">Devuelve las etiquetas de propiedad para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="3193f-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="3193f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="3193f-106">Parameters</span></span>

 <span data-ttu-id="3193f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3193f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3193f-108">[entrada] Una máscara de bits de indicadores que controla el formato de las cadenas en las etiquetas de propiedades que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="3193f-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="3193f-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="3193f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3193f-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="3193f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3193f-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3193f-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="3193f-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3193f-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3193f-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="3193f-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="3193f-114">[out] Un puntero a un puntero a la matriz de la etiqueta de propiedad que contiene las etiquetas para todas las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="3193f-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3193f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3193f-115">Return value</span></span>

<span data-ttu-id="3193f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3193f-116">S_OK</span></span> 
  
> <span data-ttu-id="3193f-117">Se han devuelto todas las etiquetas de propiedad correctamente.</span><span class="sxs-lookup"><span data-stu-id="3193f-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="3193f-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3193f-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3193f-119">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="3193f-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3193f-120">Notas</span><span class="sxs-lookup"><span data-stu-id="3193f-120">Remarks</span></span>

<span data-ttu-id="3193f-121">El método **IMAPIProp::GetPropList** recupera la etiqueta de propiedad para cada propiedad actualmente admitido por un objeto.</span><span class="sxs-lookup"><span data-stu-id="3193f-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="3193f-122">Si el objeto no es compatible actualmente con todas las propiedades, **GetPropList** devuelve una matriz de etiqueta de propiedad con el miembro **cValues** establece en 0.</span><span class="sxs-lookup"><span data-stu-id="3193f-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="3193f-123">El ámbito de las propiedades devueltas por **GetPropList** varía en función de un proveedor a otro.</span><span class="sxs-lookup"><span data-stu-id="3193f-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="3193f-124">Algunos proveedores de servicios de excluyen esas propiedades para que el autor de la llamada no tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="3193f-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="3193f-125">Todos los proveedores de devolverán las propiedades de tipo **pt Object**.</span><span class="sxs-lookup"><span data-stu-id="3193f-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="3193f-126">Si el objeto no es compatible con Unicode, **GetPropList** devuelve MAPI_E_BAD_CHARWIDTH, incluso si no hay ninguna propiedad de cadena definida para el objeto.</span><span class="sxs-lookup"><span data-stu-id="3193f-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3193f-127">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="3193f-127">Notes to implementers</span></span>

<span data-ttu-id="3193f-128">Los proveedores de transporte remoto implementan **GetPropList** exactamente como se especifica aquí.</span><span class="sxs-lookup"><span data-stu-id="3193f-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="3193f-129">No existen problemas especiales.</span><span class="sxs-lookup"><span data-stu-id="3193f-129">There are no special concerns.</span></span> <span data-ttu-id="3193f-130">La implementación debe, devolver por supuesto, la misma lista de propiedades como compatible con el método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3193f-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3193f-131">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3193f-131">Notes to callers</span></span>

<span data-ttu-id="3193f-132">Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de etiqueta de propiedad que señala _lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="3193f-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3193f-133">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3193f-133">MFCMAPI reference</span></span>

<span data-ttu-id="3193f-134">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3193f-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3193f-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3193f-135">**File**</span></span>|<span data-ttu-id="3193f-136">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="3193f-136">**Function**</span></span>|<span data-ttu-id="3193f-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3193f-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3193f-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="3193f-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3193f-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="3193f-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="3193f-140">MFCMAPI usa el método **IMAPIProp::GetPropList** para obtener una lista de propiedades que se pase a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="3193f-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3193f-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="3193f-141">See also</span></span>



[<span data-ttu-id="3193f-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="3193f-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="3193f-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3193f-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3193f-144">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3193f-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="3193f-145">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3193f-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

