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
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339224"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="19ae8-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="19ae8-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="19ae8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19ae8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19ae8-105">Prepara una lista de destinatarios para su uso posterior por parte del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="19ae8-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="19ae8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="19ae8-106">Parameters</span></span>

 <span data-ttu-id="19ae8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19ae8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="19ae8-108">a Máscara de máscara de marcadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="19ae8-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="19ae8-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="19ae8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="19ae8-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="19ae8-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="19ae8-111">Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="19ae8-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="19ae8-112">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo de intercambio en caché y obtenga acceso a una entrada de dicha libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="19ae8-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="19ae8-113">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="19ae8-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="19ae8-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="19ae8-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="19ae8-115">a Un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedades que indican las propiedades, si las hay, que requieren actualización.</span><span class="sxs-lookup"><span data-stu-id="19ae8-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="19ae8-116">El parámetro _lpSPropTagArray_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="19ae8-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="19ae8-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="19ae8-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="19ae8-118">a Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="19ae8-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19ae8-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19ae8-119">Return value</span></span>

<span data-ttu-id="19ae8-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="19ae8-120">S_OK</span></span> 
  
> <span data-ttu-id="19ae8-121">La lista de destinatarios se ha preparado correctamente.</span><span class="sxs-lookup"><span data-stu-id="19ae8-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19ae8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19ae8-122">Remarks</span></span>

<span data-ttu-id="19ae8-123">Los clientes y los proveedores de servicios llaman al método **PrepareRecips** para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="19ae8-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="19ae8-124">Asegúrese de que todos los destinatarios del parámetro _lpRecipList_ tienen identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="19ae8-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="19ae8-125">Asegúrese de que cada uno de los destinatarios del parámetro _lpRecipList_ tiene las propiedades enumeradas en el parámetro _lpSPropTagArray_ y que estas propiedades aparecen al principio de la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="19ae8-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="19ae8-126">MAPI convierte los identificadores de entrada a corto plazo de cada destinatario en identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="19ae8-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="19ae8-127">Si es necesario, los identificadores de entrada a largo plazo de los destinatarios se recuperan del proveedor de libreta de direcciones adecuado y se solicitan propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="19ae8-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="19ae8-128">En una entrada de destinatario individual, las propiedades solicitadas se ordenan primero, seguidas de las propiedades que ya estaban presentes para la entrada.</span><span class="sxs-lookup"><span data-stu-id="19ae8-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="19ae8-129">Si una o varias de las propiedades solicitadas en el parámetro _lpSPropTagArray_ no están controladas por el proveedor de libreta de direcciones adecuado, sus tipos de propiedad se establecerán en PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="19ae8-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="19ae8-130">Sus valores de propiedad se establecerán en MAPI_E_NOT_FOUND o en otro valor que proporcione una razón más específica por la que las propiedades no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="19ae8-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="19ae8-131">Cada estructura [SPropValue](spropvalue.md) incluida en el parámetro _lpRecipList_ debe asignarse por separado mediante las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) , de modo que se pueda liberar de forma individual.</span><span class="sxs-lookup"><span data-stu-id="19ae8-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="19ae8-132">Para obtener información sobre PT_ERROR, vea [tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="19ae8-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19ae8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="19ae8-133">See also</span></span>



[<span data-ttu-id="19ae8-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="19ae8-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="19ae8-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="19ae8-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="19ae8-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="19ae8-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="19ae8-137">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="19ae8-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="19ae8-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="19ae8-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="19ae8-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="19ae8-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="19ae8-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="19ae8-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

