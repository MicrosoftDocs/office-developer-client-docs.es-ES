---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 004498ac94aadaa075d87d4dd3c675c8cd5f4feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563880"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="744be-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="744be-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="744be-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="744be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="744be-105">Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="744be-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="744be-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="744be-106">Parameters</span></span>

 <span data-ttu-id="744be-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="744be-107">_ulFlags_</span></span>
  
> <span data-ttu-id="744be-108">[entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="744be-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="744be-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="744be-109">The following flag can be set:</span></span>
    
<span data-ttu-id="744be-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="744be-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="744be-111">Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="744be-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="744be-112">Por ejemplo, puede usar esta marca para permitir que una aplicación de cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y tener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="744be-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="744be-113">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="744be-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="744be-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="744be-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="744be-115">[entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indican las propiedades, si lo hay, que requieren actualización.</span><span class="sxs-lookup"><span data-stu-id="744be-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="744be-116">El parámetro _lpSPropTagArray_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="744be-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="744be-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="744be-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="744be-118">[entrada] Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="744be-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="744be-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="744be-119">Return value</span></span>

<span data-ttu-id="744be-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="744be-120">S_OK</span></span> 
  
> <span data-ttu-id="744be-121">La lista de destinatarios se ha preparado correctamente.</span><span class="sxs-lookup"><span data-stu-id="744be-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="744be-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="744be-122">Remarks</span></span>

<span data-ttu-id="744be-123">Los clientes y proveedores de servicios de llaman al método **PrepareRecips** para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="744be-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="744be-124">Asegúrese de que todos los destinatarios en el parámetro _lpRecipList_ tienen los identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="744be-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="744be-125">Asegúrese de que cada destinatario en el parámetro _lpRecipList_ tiene las propiedades enumeradas en el parámetro _lpSPropTagArray_ y que estas propiedades aparecen al principio de la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="744be-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="744be-126">MAPI convierte los identificadores de entrada a corto plazo de cada destinatario en los identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="744be-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="744be-127">Si es necesario, los identificadores de entrada a largo plazo de los destinatarios se recuperan desde el proveedor de libreta de direcciones adecuado y se solicitan las propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="744be-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="744be-128">En una entrada de destinatarios individual, las propiedades solicitadas se ordenan en primer lugar, seguido de todas las propiedades que ya estaban presentes para la entrada.</span><span class="sxs-lookup"><span data-stu-id="744be-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="744be-129">Si una o varias de las propiedades solicitadas en el parámetro _lpSPropTagArray_ no se controlan mediante el proveedor de libreta de direcciones adecuado, sus tipos de propiedad se establecerá en PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="744be-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="744be-130">Sus valores de propiedad se establecerá en a MAPI_E_NOT_FOUND o a otro valor que proporciona un motivo más específico, ¿por qué las propiedades no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="744be-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="744be-131">Cada estructura [SPropValue](spropvalue.md) incluido en el parámetro _lpRecipList_ debe asignarse por separado mediante el uso de las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) para que se puede liberar de forma individual.</span><span class="sxs-lookup"><span data-stu-id="744be-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="744be-132">Para obtener información sobre PT_ERROR, vea [Tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="744be-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="744be-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="744be-133">See also</span></span>



[<span data-ttu-id="744be-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="744be-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="744be-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="744be-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="744be-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="744be-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="744be-137">Propiedad canónico PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="744be-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="744be-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="744be-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="744be-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="744be-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="744be-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="744be-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

