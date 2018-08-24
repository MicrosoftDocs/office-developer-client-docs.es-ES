---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c42077528a4f7227321d8f987cc5dd0ccd4c966c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589745"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="6b744-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="6b744-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="6b744-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b744-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b744-105">Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="6b744-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="6b744-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6b744-106">Parameters</span></span>

<span data-ttu-id="6b744-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b744-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6b744-108">[entrada] Una máscara de bits de indicadores que controla el tipo de texto de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="6b744-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="6b744-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b744-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="6b744-110">MAPI_CACHE_ONLY: Usar solo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="6b744-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="6b744-111">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6b744-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="6b744-112">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b744-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6b744-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="6b744-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="6b744-114">[entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indican las propiedades que requieren la actualización, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="6b744-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="6b744-115">El parámetro _lpPropTagArray_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="6b744-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="6b744-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="6b744-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="6b744-117">[entrada] Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="6b744-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b744-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b744-118">Return value</span></span>

<span data-ttu-id="6b744-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b744-119">S_OK</span></span> 
  
> <span data-ttu-id="6b744-120">La lista de destinatarios se ha preparado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b744-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="6b744-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6b744-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6b744-122">No existen uno o varios de los destinatarios en el parámetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="6b744-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b744-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b744-123">Return value</span></span>

<span data-ttu-id="6b744-124">Un cliente llama al método MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) para modificar o reorganizar un conjunto de propiedades para uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="6b744-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="6b744-125">Los destinatarios pueden o no pueden formar parte de la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="6b744-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="6b744-126">MAPI transfiere esta llamada al método **IABLogon::PrepareRecips** de un proveedor libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6b744-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="6b744-127">**IABLogon::PrepareRecips** realiza cuatro tareas principales:</span><span class="sxs-lookup"><span data-stu-id="6b744-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="6b744-128">Se asegura de que todos los destinatarios en la lista de direcciones apunta por el parámetro _lpRecipList_ tiene un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="6b744-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="6b744-129">Se asegura de que todos los destinatarios tienen las propiedades especificadas en la matriz de valores de la propiedad indicada por el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="6b744-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="6b744-130">Se asegura de que las propiedades de la matriz de valores de propiedad aparecen antes de las demás propiedades que existían antes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6b744-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="6b744-131">Se asegura de que el orden de las propiedades de [ADRENTRY](adrentry.md) estructura cada destinatario de la estructura de **ADRLIST** es la misma que en la matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6b744-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="6b744-132">La estructura **ADRENTRY** en el parámetro _lpRecipList_ contiene una estructura **ADRENTRY** para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="6b744-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="6b744-133">Cada estructura **ADRENTRY** contiene una matriz de estructuras [SPropValue](spropvalue.md) para describir las propiedades del destinatario.</span><span class="sxs-lookup"><span data-stu-id="6b744-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="6b744-134">Cuando se devuelve **IABLogon::PrepareRecips** , la matriz de la estructura de **SPropValue** para cada destinatario incluye las propiedades de la _lpPropTagArray_ seguido de las demás propiedades para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="6b744-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6b744-135">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="6b744-135">Notes to implementers</span></span>

<span data-ttu-id="6b744-136">La implementación de **IABLogon::PrepareRecips** implica la colocación de propiedades en un orden específico, recuperación de valores de propiedad y convertir los identificadores de entrada a corto plazo a los identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="6b744-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="6b744-137">Las propiedades que se solicitan en el parámetro _lpPropTagArray_ deben ser al principio de la matriz de valores de propiedad asociado con la estructura **ADRENTRY** de cada destinatario en el parámetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="6b744-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="6b744-138">Si no existen valores de estas propiedades, abra la lista de usuarios o distribución mensajería asociada mediante su identificador de entrada y recuperar los valores de propiedad que faltan.</span><span class="sxs-lookup"><span data-stu-id="6b744-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="6b744-139">Asigne cada estructura **SPropValue** pasada por separado en _lpRecipList_ para que se pueden liberar las estructuras de forma individual.</span><span class="sxs-lookup"><span data-stu-id="6b744-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="6b744-140">Si debe asignar espacio adicional para cualquier estructura **SPropValue** , por ejemplo, para almacenar los datos para una propiedad de cadena, use la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar espacio adicional para la matriz de valores de propiedad completa.</span><span class="sxs-lookup"><span data-stu-id="6b744-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="6b744-141">Utilice la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de valores de propiedad original y, a continuación, utilice la función [MAPIAllocateMore](mapiallocatemore.md) para asignar cualquier memoria adicional que se requiere.</span><span class="sxs-lookup"><span data-stu-id="6b744-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="6b744-142">Para implementar **IABLogon::PrepareRecips**, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b744-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="6b744-143">Compruebe si hay entradas en el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="6b744-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="6b744-144">Si la matriz de valores de propiedad está vacía, no hay ningún trabajo que hacer.</span><span class="sxs-lookup"><span data-stu-id="6b744-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="6b744-145">Devolver un valor correcto.</span><span class="sxs-lookup"><span data-stu-id="6b744-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="6b744-146">Proceso de cada destinatario en el parámetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="6b744-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="6b744-147">Hay un miembro de la estructura **ADRENTRY** para cada destinatario en la lista.</span><span class="sxs-lookup"><span data-stu-id="6b744-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="6b744-148">Omitir los siguientes tipos de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="6b744-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="6b744-149">Destinatarios sin un identificador de entrada en el miembro **rgPropVals** de su estructura **ADRENTRY** (es decir, los destinatarios sin resolver).</span><span class="sxs-lookup"><span data-stu-id="6b744-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="6b744-150">Destinatarios con un identificador de entrada que no pertenecen a su proveedor.</span><span class="sxs-lookup"><span data-stu-id="6b744-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="6b744-151">Estos destinatarios se pasan a otro proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6b744-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="6b744-152">Abra al destinatario y recuperar las propiedades que ya están configuradas para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="6b744-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="6b744-153">Combinar la matriz de valores de propiedad especificada en la _lpRecipList_ con la matriz de propiedades devuelto desde **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="6b744-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="6b744-154">Si se produce la misma propiedad en ambas matrices de propiedad, utilice el valor de _lpRecipList_.</span><span class="sxs-lookup"><span data-stu-id="6b744-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="6b744-155">Si la matriz de valores de propiedad _lpRecipList_ es lo suficientemente grande como para contener todas las propiedades necesarias, reemplace acaba con la matriz combinada.</span><span class="sxs-lookup"><span data-stu-id="6b744-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="6b744-156">Si la matriz de valores de propiedad _lpRecipList_ no es lo suficientemente grande, reemplace con una matriz recién asignada.</span><span class="sxs-lookup"><span data-stu-id="6b744-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="6b744-157">Asegúrese de que la nueva matriz tiene un valor actualizado en cada uno de sus miembros **cValues** .</span><span class="sxs-lookup"><span data-stu-id="6b744-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="6b744-158">Si no reconoce una o varias de las propiedades en el parámetro _lpPropTagArray_ , establecer el tipo de propiedad en estructura **ADRENTRY** del destinatario a PT_ERROR y el valor de la propiedad a MAPI_E_NOT_FOUND o a otro valor que proporciona un mayor motivo específico de la no disponibilidad de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6b744-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="6b744-159">Para obtener información sobre PT_ERROR, vea [Tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="6b744-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="6b744-160">Reasignar nunca en la estructura **ADRLIST** que se pasó a **IABLogon::PrepareRecips** o cambiar su número de entradas.</span><span class="sxs-lookup"><span data-stu-id="6b744-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b744-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b744-161">See also</span></span>

- [<span data-ttu-id="6b744-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="6b744-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="6b744-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6b744-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="6b744-164">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="6b744-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="6b744-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6b744-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="6b744-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b744-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

