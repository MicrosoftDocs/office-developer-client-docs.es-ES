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
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423863"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="c2ac7-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="c2ac7-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="c2ac7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2ac7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2ac7-105">Prepara una lista de destinatarios para su uso posterior por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="c2ac7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c2ac7-106">Parameters</span></span>

<span data-ttu-id="c2ac7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2ac7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c2ac7-108">[in] Máscara de bits de marcas que controla el tipo de texto de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="c2ac7-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="c2ac7-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="c2ac7-110">MAPI_CACHE_ONLY: use solo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="c2ac7-111">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="c2ac7-112">Esta marca solo es compatible con el Exchange libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="c2ac7-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c2ac7-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c2ac7-114">[in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indican las propiedades que requieren actualización, si las hay.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="c2ac7-115">El  _parámetro lpPropTagArray_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="c2ac7-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="c2ac7-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="c2ac7-117">[in] Puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2ac7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2ac7-118">Return value</span></span>

<span data-ttu-id="c2ac7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2ac7-119">S_OK</span></span> 
  
> <span data-ttu-id="c2ac7-120">La lista de destinatarios se preparó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="c2ac7-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c2ac7-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c2ac7-122">Uno o varios de los destinatarios del parámetro  _lpRecipList_ no existen.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2ac7-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2ac7-123">Return value</span></span>

<span data-ttu-id="c2ac7-124">Un cliente llama al método [MAPI IAddrBook::P repareRecips](iaddrbook-preparerecips.md) para modificar o reorganizar un conjunto de propiedades para uno o varios destinatarios.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="c2ac7-125">Los destinatarios pueden o no formar parte de la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="c2ac7-126">MAPI transfiere esta llamada al método **IABLogon::P repareRecips** de un proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="c2ac7-127">**IABLogon::P repareRecips** realiza cuatro tareas principales:</span><span class="sxs-lookup"><span data-stu-id="c2ac7-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="c2ac7-128">Garantiza que todos los destinatarios de la lista de direcciones a los que apunta el parámetro  _lpRecipList_ tengan un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="c2ac7-129">Garantiza que todos los destinatarios tengan las propiedades especificadas en la matriz de valores de propiedad a la que apunta el _parámetro lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="c2ac7-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="c2ac7-130">Garantiza que las propiedades de la matriz de valores de propiedad aparezcan antes que cualquier otra propiedad que existiera antes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="c2ac7-131">Garantiza que el orden de las propiedades de la estructura [ADRENTRY](adrentry.md) de cada destinatario en la estructura **ADRLIST** sea el mismo que en la matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="c2ac7-132">La **estructura ADRENTRY** del parámetro  _lpRecipList_ contiene una **estructura ADRENTRY** para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="c2ac7-133">Cada **estructura ADRENTRY** contiene una matriz de [estructuras SPropValue](spropvalue.md) para describir las propiedades del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="c2ac7-134">Cuando **devuelve IABLogon::P repareRecips,** la matriz de estructura **SPropValue** para cada destinatario incluye las propiedades de  _lpPropTagArray_ seguidas de las demás propiedades del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c2ac7-135">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="c2ac7-135">Notes to implementers</span></span>

<span data-ttu-id="c2ac7-136">La implementación de **IABLogon::P repareRecips** implica poner propiedades en un orden específico, recuperar valores de propiedad y convertir identificadores de entrada a corto plazo en identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="c2ac7-137">Las propiedades que se solicitan en el parámetro _lpPropTagArray_ deben estar al principio de la matriz de valores de propiedad asociada con la estructura **ADRENTRY** de cada destinatario en el _parámetro lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="c2ac7-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="c2ac7-138">Si los valores de estas propiedades no existen, abra la lista de distribución o el usuario de mensajería asociado mediante su identificador de entrada y recupere los valores de propiedad que faltan.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="c2ac7-139">Asigne cada **estructura SPropValue** pasada en  _lpRecipList_ por separado para que las estructuras se puedan liberar individualmente.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="c2ac7-140">Si debe asignar espacio adicional para cualquier estructura **SPropValue,** por ejemplo, para almacenar los datos de una propiedad de cadena, use la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar espacio adicional para la matriz de valores de propiedad completa.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="c2ac7-141">Use la [función MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de valores de propiedad original y, a continuación, use la [función MAPIAllocateMore](mapiallocatemore.md) para asignar cualquier memoria adicional que sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="c2ac7-142">Para implementar **IABLogon::P repareRecips**, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="c2ac7-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="c2ac7-143">Compruebe si hay entradas en el _parámetro lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="c2ac7-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="c2ac7-144">Si la matriz de valores de propiedad está vacía, no hay trabajo que hacer.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="c2ac7-145">Devuelve un valor correcto.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="c2ac7-146">Procese cada destinatario en el _parámetro lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="c2ac7-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="c2ac7-147">Hay un miembro **de la estructura ADRENTRY** para cada destinatario de la lista.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="c2ac7-148">Ignore los siguientes tipos de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="c2ac7-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="c2ac7-149">Destinatarios sin identificador de entrada en el **miembro rgPropVals** de su estructura **ADRENTRY** (es decir, destinatarios sin resolver).</span><span class="sxs-lookup"><span data-stu-id="c2ac7-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="c2ac7-150">Destinatarios con un identificador de entrada que no pertenece a su proveedor.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="c2ac7-151">Estos destinatarios se pasarán a otro proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="c2ac7-152">Abra el destinatario y recupere las propiedades que ya están establecidas para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="c2ac7-153">Combine la matriz de valores de propiedad especificada en  _lpRecipList_ con la matriz de propiedades devueltas de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="c2ac7-154">Si se produce la misma propiedad en ambas matrices de propiedades, use el valor de  _lpRecipList_.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="c2ac7-155">Si la matriz de valores de propiedad  _lpRecipList_ es lo suficientemente grande como para contener todas las propiedades necesarias, simplemente reemplázcala por la matriz combinada.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="c2ac7-156">Si la matriz de valores de propiedad  _lpRecipList_ no es lo suficientemente grande, reemplázcala por una matriz recién asignada.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="c2ac7-157">Asegúrese de que la nueva matriz tiene un valor actualizado en cada uno de sus **miembros de cValues.**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="c2ac7-158">Si no reconoce una o varias de las propiedades del parámetro  _lpPropTagArray,_ establezca el tipo de propiedad en la estructura **ADRENTRY** del destinatario en PT_ERROR y el valor de la propiedad en MAPI_E_NOT_FOUND o en otro valor que dé una razón más específica para la indisponibilidad de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="c2ac7-159">Para obtener información sobre PT_ERROR, vea [Tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="c2ac7-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="c2ac7-160">Nunca volver a la estructura **ADRLIST** que se pasa a **IABLogon::P repareRecips** o cambiar su número de entradas.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2ac7-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2ac7-161">See also</span></span>

- [<span data-ttu-id="c2ac7-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c2ac7-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="c2ac7-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c2ac7-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="c2ac7-164">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="c2ac7-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="c2ac7-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c2ac7-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="c2ac7-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2ac7-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

