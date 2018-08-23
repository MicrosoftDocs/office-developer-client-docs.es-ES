---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 524bbfe5f40a66585fb4ed4463b057ca6a0c881a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586805"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="811d9-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="811d9-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="811d9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="811d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="811d9-105">Muestra el cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="811d9-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="811d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="811d9-106">Parameters</span></span>

 <span data-ttu-id="811d9-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="811d9-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="811d9-108">[entrada, salida] Un puntero al controlador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="811d9-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="811d9-109">En la entrada, siempre se debe pasar un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="811d9-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="811d9-110">En la salida, si se establece la marca DIALOG_SDI en la estructura [ADRPARM](adrparm.md) indicada por el parámetro _lpAdrParms_ , se devuelve el identificador de ventana del cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="811d9-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="811d9-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="811d9-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="811d9-112">[entrada, salida] Un puntero a una estructura **ADRPARM** que controla la presentación y el comportamiento del cuadro de diálogo dirección.</span><span class="sxs-lookup"><span data-stu-id="811d9-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="811d9-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="811d9-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="811d9-114">[entrada, salida] Un puntero a un puntero a una lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="811d9-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="811d9-115">En la entrada, esta lista es la lista actual de los destinatarios de un mensaje o NULL, si no existe ninguna dicha lista.</span><span class="sxs-lookup"><span data-stu-id="811d9-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="811d9-116">En la salida, _lppAdrList_ apunta a una lista actualizada de los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="811d9-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="811d9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="811d9-117">Return value</span></span>

<span data-ttu-id="811d9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="811d9-118">S_OK</span></span> 
  
> <span data-ttu-id="811d9-119">El cuadro de diálogo dirección se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="811d9-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="811d9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="811d9-120">Remarks</span></span>

<span data-ttu-id="811d9-121">El método **IMAPISupport::Address** se implementa para objetos de compatibilidad con de proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="811d9-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="811d9-122">Los proveedores de la libreta de direcciones, llame a **dirección** para crear o actualizar una lista de destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="811d9-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="811d9-123">Cada destinatario se describe en una estructura [ADRENTRY](adrentry.md) que se incluye en la estructura [ADRLIST](adrlist.md) indicada por el parámetro _lppAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="811d9-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="811d9-124">La estructura **ADRENTRY** contiene una matriz de valores de propiedades de los destinatarios, uno de los cuales es el destinatario tipo o propiedad de **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="811d9-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="811d9-125">Esta estructura **ADRLIST** se puede pasar a un cliente para usar como el parámetro _lpMods_ en una llamada a [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="811d9-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="811d9-126">Cada destinatario de la estructura de **ADRLIST** puede ser ya sea resuelto, lo que indica que uno de sus valores de propiedad es de su propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), o sin resolver, lo que indica que la propiedad de **entrada del objeto** es falta.</span><span class="sxs-lookup"><span data-stu-id="811d9-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="811d9-127">Además de **entrada del objeto**resueltos destinatarios incluyen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="811d9-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="811d9-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="811d9-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="811d9-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="811d9-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="811d9-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="811d9-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="811d9-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="811d9-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="811d9-132">Destinatarios sin resolver suelen incluyen solo **PR_DISPLAY_NAME** y **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="811d9-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="811d9-133">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="811d9-133">Notes to callers</span></span>

<span data-ttu-id="811d9-134">Es posible que la estructura **ADRLIST** que el autor de la llamada que se pasa en un tamaño diferente de la estructura que se devuelve de MAPI.</span><span class="sxs-lookup"><span data-stu-id="811d9-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="811d9-135">Al asignar memoria para la estructura **ADRLIST** , asignar la memoria para cada estructura [SPropValue](spropvalue.md) por separado.</span><span class="sxs-lookup"><span data-stu-id="811d9-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="811d9-136">Use los punteros a las funciones de asignación de memoria MAPI que se pasó a la función [ABProviderInit](abproviderinit.md) para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="811d9-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="811d9-137">Asignar memoria con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para cada estructura de valor de propiedad en las estructuras **ADRENTRY** en **ADRLIST**y **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="811d9-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="811d9-138">Si **dirección** debe devolver una estructura **ADRLIST** más grande, o si han transcurrido NULL para _lppAdrList_, **dirección** libera la estructura original y asigna una nueva.</span><span class="sxs-lookup"><span data-stu-id="811d9-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="811d9-139">**Dirección** también asigna las estructuras de valor de propiedad adicional en la estructura **ADRLIST** y libera los antiguos según corresponda.</span><span class="sxs-lookup"><span data-stu-id="811d9-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="811d9-140">Para obtener más información acerca de cómo se administra la memoria para las estructuras **ADRLIST** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="811d9-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="811d9-141">**Dirección** se devuelve inmediatamente si se ha establecido el indicador DIALOG_SDI en la estructura **ADRPARM** en el parámetro _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="811d9-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="811d9-142">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="811d9-142">See also</span></span>



[<span data-ttu-id="811d9-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="811d9-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="811d9-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="811d9-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="811d9-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="811d9-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="811d9-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="811d9-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="811d9-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="811d9-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="811d9-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="811d9-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="811d9-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="811d9-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="811d9-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="811d9-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="811d9-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="811d9-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="811d9-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="811d9-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="811d9-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="811d9-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="811d9-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="811d9-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="811d9-155">Propiedad canónica PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="811d9-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="811d9-156">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="811d9-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="811d9-157">Propiedad canónica PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="811d9-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="811d9-158">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="811d9-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="811d9-159">Propiedad canónica PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="811d9-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="811d9-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="811d9-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="811d9-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="811d9-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="811d9-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="811d9-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="811d9-163">Administrar memoria para ADRLIST y estructuras SRowSet</span><span class="sxs-lookup"><span data-stu-id="811d9-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

