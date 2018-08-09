---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817069"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="1b619-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="1b619-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="1b619-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b619-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b619-105">Recupera el valor de una propiedad única de una interfaz (propiedad), es decir, una interfaz que se deriva de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1b619-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b619-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1b619-106">Header file:</span></span>  <br/> |<span data-ttu-id="1b619-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1b619-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1b619-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="1b619-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b619-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1b619-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1b619-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1b619-110">Called by:</span></span>  <br/> |<span data-ttu-id="1b619-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="1b619-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="1b619-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b619-112">Parameters</span></span>

 <span data-ttu-id="1b619-113">_médico principal_</span><span class="sxs-lookup"><span data-stu-id="1b619-113">_pmp_</span></span>
  
> <span data-ttu-id="1b619-114">[entrada] Puntero a la interfaz de [IMAPIProp](imapipropiunknown.md) desde la que es el valor de la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1b619-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="1b619-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="1b619-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="1b619-116">[entrada] Etiqueta de la propiedad de la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1b619-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="1b619-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="1b619-117">_ppprop_</span></span>
  
> <span data-ttu-id="1b619-118">[out] Puntero a un puntero a la estructura [SPropValue](spropvalue.md) devuelta define el valor de la propiedad recuperada.</span><span class="sxs-lookup"><span data-stu-id="1b619-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b619-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b619-119">Return value</span></span>

<span data-ttu-id="1b619-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1b619-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1b619-121">La propiedad solicitada no está disponible desde la interfaz especificada.</span><span class="sxs-lookup"><span data-stu-id="1b619-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b619-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b619-122">Remarks</span></span>

<span data-ttu-id="1b619-123">A diferencia del método [IMAPIProp::GetProps](imapiprop-getprops.md) , la función **HrGetOneProp** no devuelve nunca ningún mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="1b619-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="1b619-124">Debido a que recupera sólo una propiedad, que simplemente se realiza correctamente o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="1b619-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="1b619-125">Para recuperar las propiedades de varios, **GetProps** es más rápido.</span><span class="sxs-lookup"><span data-stu-id="1b619-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="1b619-126">Puede establecer o cambiar una propiedad única con la función [HrSetOneProp](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="1b619-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1b619-127">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1b619-127">MFCMAPI reference</span></span>

<span data-ttu-id="1b619-128">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1b619-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1b619-129">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1b619-129">**File**</span></span>|<span data-ttu-id="1b619-130">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="1b619-130">**Function**</span></span>|<span data-ttu-id="1b619-131">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1b619-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b619-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1b619-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1b619-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="1b619-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="1b619-134">MFCMAPI usa el método **HrGetOneProp** para recuperar el tipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="1b619-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b619-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b619-135">See also</span></span>



[<span data-ttu-id="1b619-136">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1b619-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

