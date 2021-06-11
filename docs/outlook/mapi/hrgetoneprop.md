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
ms.openlocfilehash: 95273bf6025d6ef995d7c21c0e44bdbbf59072f6
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589176"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="d4afa-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="d4afa-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="d4afa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4afa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4afa-105">Recupera el valor de una sola propiedad de una interfaz de propiedad, es decir, una interfaz derivada de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d4afa-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4afa-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d4afa-106">Header file:</span></span>  <br/> |<span data-ttu-id="d4afa-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d4afa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d4afa-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d4afa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d4afa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d4afa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d4afa-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d4afa-110">Called by:</span></span>  <br/> |<span data-ttu-id="d4afa-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d4afa-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="d4afa-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d4afa-112">Parameters</span></span>

 <span data-ttu-id="d4afa-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="d4afa-113">_pmp_</span></span>
  
> <span data-ttu-id="d4afa-114">[in] Puntero a la [interfaz IMAPIProp](imapipropiunknown.md) desde la que se va a recuperar el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4afa-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="d4afa-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d4afa-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="d4afa-116">[in] Etiqueta de propiedad de la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d4afa-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="d4afa-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="d4afa-117">_ppprop_</span></span>
  
> <span data-ttu-id="d4afa-118">[salida] Puntero a un puntero a la estructura [SPropValue](spropvalue.md) devuelta que define el valor de la propiedad recuperada.</span><span class="sxs-lookup"><span data-stu-id="d4afa-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d4afa-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4afa-119">Return value</span></span>

<span data-ttu-id="d4afa-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d4afa-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d4afa-121">La propiedad solicitada no está disponible desde la interfaz especificada.</span><span class="sxs-lookup"><span data-stu-id="d4afa-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4afa-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4afa-122">Remarks</span></span>

<span data-ttu-id="d4afa-123">A diferencia [del método IMAPIProp::GetProps,](imapiprop-getprops.md) la **función HrGetOneProp** nunca devuelve ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="d4afa-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="d4afa-124">Dado que solo recupera una propiedad, simplemente se realiza correctamente o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d4afa-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="d4afa-125">Para recuperar varias propiedades, **GetProps** es más rápido.</span><span class="sxs-lookup"><span data-stu-id="d4afa-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="d4afa-126">Puede establecer o cambiar una sola propiedad con la [función HrSetOneProp.](hrsetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="d4afa-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d4afa-127">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d4afa-127">MFCMAPI reference</span></span>

<span data-ttu-id="d4afa-128">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d4afa-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d4afa-129">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d4afa-129">**File**</span></span>|<span data-ttu-id="d4afa-130">**Función**</span><span class="sxs-lookup"><span data-stu-id="d4afa-130">**Function**</span></span>|<span data-ttu-id="d4afa-131">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d4afa-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4afa-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d4afa-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d4afa-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="d4afa-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="d4afa-134">MFCMAPI usa el **método HrGetOneProp** para recuperar el tipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="d4afa-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4afa-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4afa-135">See also</span></span>



[<span data-ttu-id="d4afa-136">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d4afa-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

