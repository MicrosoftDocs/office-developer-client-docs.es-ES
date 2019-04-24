---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316486"
---
# <a name="rtfsync"></a><span data-ttu-id="d501c-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="d501c-103">RTFSync</span></span>

<span data-ttu-id="d501c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d501c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d501c-105">Garantiza que el texto del mensaje de formato de texto enriquecido (RTF) coincide con la versión de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="d501c-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="d501c-106">Es necesario llamar a esta función antes de leer la versión RTF y después de modificar la versión RTF.</span><span class="sxs-lookup"><span data-stu-id="d501c-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d501c-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d501c-107">Header file:</span></span>  <br/> |<span data-ttu-id="d501c-108">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d501c-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d501c-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d501c-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d501c-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d501c-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d501c-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d501c-111">Called by:</span></span>  <br/> |<span data-ttu-id="d501c-112">Aplicaciones cliente y proveedores de almacenamiento de mensajes compatibles con RTF</span><span class="sxs-lookup"><span data-stu-id="d501c-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="d501c-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="d501c-113">Parameters</span></span>

<span data-ttu-id="d501c-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="d501c-114">_lpMessage_</span></span>
  
> <span data-ttu-id="d501c-115">a Puntero al mensaje que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="d501c-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="d501c-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d501c-116">_ulFlags_</span></span>
  
> <span data-ttu-id="d501c-117">a Máscara de la máscara usada para indicar que se ha cambiado la versión de texto sin formato o RTF del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d501c-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="d501c-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d501c-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="d501c-119">RTF_SYNC_BODY_CHANGED: la versión de texto sin formato del mensaje ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d501c-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="d501c-120">RTF_SYNC_RTF_CHANGED: la versión RTF del mensaje ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d501c-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="d501c-121">Todos los demás bits del parámetro _ulFlags_ están reservados para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="d501c-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="d501c-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="d501c-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="d501c-123">contempla Puntero a una variable que indica si hay un mensaje actualizado.</span><span class="sxs-lookup"><span data-stu-id="d501c-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="d501c-124">TRUE si hay un mensaje actualizado; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="d501c-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d501c-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d501c-125">Return value</span></span>

<span data-ttu-id="d501c-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="d501c-126">S_OK</span></span> 
  
> <span data-ttu-id="d501c-127">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d501c-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d501c-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d501c-128">Remarks</span></span>

<span data-ttu-id="d501c-129">Si falta la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) o es false, antes de leer la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), se debe llamar a la función **RTFSync** con el RTF_SYNC_BODY_ Se ha cambiado el conjunto de marcas.</span><span class="sxs-lookup"><span data-stu-id="d501c-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="d501c-130">Si la marca STORE_RTF_OK no se establece en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), se debe llamar a esta función con la marca RTF_SYNC_RTF_CHANGED establecida después de modificar **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="d501c-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="d501c-131">Si se han cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** , se debe llamar a la función **RTFSync** con ambos marcadores establecidos.</span><span class="sxs-lookup"><span data-stu-id="d501c-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="d501c-132">Si el valor del parámetro _lpfMessageUpdated_ se establece en true, se debe llamar al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d501c-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="d501c-133">Si no se llama a **SaveChanges** , no se guardarán las modificaciones en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d501c-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="d501c-134">Los proveedores de almacenamiento de mensajes pueden usar **RTFSync** para mantener las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="d501c-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="d501c-135">Para obtener más información, vea [compatibilidad con texto RTF para proveedores de almacenamiento de mensajes](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="d501c-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d501c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d501c-136">See also</span></span>

- [<span data-ttu-id="d501c-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="d501c-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

