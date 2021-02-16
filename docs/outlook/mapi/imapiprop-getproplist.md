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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414791"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="29ff9-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="29ff9-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="29ff9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29ff9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29ff9-105">Devuelve etiquetas de propiedad para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="29ff9-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="29ff9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29ff9-106">Parameters</span></span>

 <span data-ttu-id="29ff9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="29ff9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="29ff9-108">[entrada] Máscara de bits de marcas que controla el formato de las cadenas de las etiquetas de propiedad devueltas.</span><span class="sxs-lookup"><span data-stu-id="29ff9-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="29ff9-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="29ff9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="29ff9-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="29ff9-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="29ff9-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="29ff9-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="29ff9-112">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="29ff9-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="29ff9-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="29ff9-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="29ff9-114">[salida] Puntero a un puntero a la matriz de etiquetas de propiedades que contiene etiquetas para todas las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="29ff9-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29ff9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29ff9-115">Return value</span></span>

<span data-ttu-id="29ff9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="29ff9-116">S_OK</span></span> 
  
> <span data-ttu-id="29ff9-117">Todas las etiquetas de propiedad se devolvieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="29ff9-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="29ff9-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="29ff9-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="29ff9-119">Se estableció MAPI_UNICODE marca y la implementación no admite Unicode o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="29ff9-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="29ff9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29ff9-120">Remarks</span></span>

<span data-ttu-id="29ff9-121">El **método IMAPIProp::GetPropList** recupera la etiqueta de propiedad de cada propiedad admitida actualmente por un objeto.</span><span class="sxs-lookup"><span data-stu-id="29ff9-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="29ff9-122">Si el objeto no admite actualmente ninguna propiedad, **GetPropList** devuelve una matriz de etiquetas de propiedad con el miembro **cValues** establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="29ff9-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="29ff9-123">El ámbito de las propiedades devueltas **por GetPropList** varía de un proveedor a otro.</span><span class="sxs-lookup"><span data-stu-id="29ff9-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="29ff9-124">Algunos proveedores de servicios excluyen aquellas propiedades para las que el autor de la llamada no tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="29ff9-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="29ff9-125">Todos los proveedores devuelven propiedades de **tipo PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="29ff9-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="29ff9-126">Si el objeto no admite Unicode, **GetPropList** devuelve MAPI_E_BAD_CHARWIDTH, incluso si no hay ninguna propiedad de cadena definida para el objeto.</span><span class="sxs-lookup"><span data-stu-id="29ff9-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="29ff9-127">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="29ff9-127">Notes to implementers</span></span>

<span data-ttu-id="29ff9-128">Los proveedores de transporte remoto **implementan GetPropList** exactamente como se especifica aquí.</span><span class="sxs-lookup"><span data-stu-id="29ff9-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="29ff9-129">No hay ningún problema especial.</span><span class="sxs-lookup"><span data-stu-id="29ff9-129">There are no special concerns.</span></span> <span data-ttu-id="29ff9-130">Por supuesto, la implementación debe devolver la misma lista de propiedades que admite el método [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="29ff9-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="29ff9-131">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="29ff9-131">Notes to callers</span></span>

<span data-ttu-id="29ff9-132">Llame a [la función MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de etiquetas de propiedad a la que  _apunta lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="29ff9-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="29ff9-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="29ff9-133">MFCMAPI reference</span></span>

<span data-ttu-id="29ff9-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="29ff9-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="29ff9-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="29ff9-135">**File**</span></span>|<span data-ttu-id="29ff9-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="29ff9-136">**Function**</span></span>|<span data-ttu-id="29ff9-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="29ff9-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="29ff9-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="29ff9-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="29ff9-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="29ff9-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="29ff9-140">MFCMAPI usa el **método IMAPIProp::GetPropList** para obtener una lista de propiedades para pasar a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="29ff9-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29ff9-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="29ff9-141">See also</span></span>



[<span data-ttu-id="29ff9-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="29ff9-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="29ff9-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="29ff9-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="29ff9-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29ff9-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="29ff9-145">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="29ff9-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

