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
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820555"
---
# <a name="rtfsync"></a><span data-ttu-id="eeb7e-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="eeb7e-103">RTFSync</span></span>

<span data-ttu-id="eeb7e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eeb7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eeb7e-105">Se asegura de que el texto del mensaje de formato de texto enriquecido (RTF) coincide con la versión de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="eeb7e-106">Es necesario llamar a esta función antes de leer la versión RTF y después de modificar la versión RTF.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eeb7e-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="eeb7e-107">Header file:</span></span>  <br/> |<span data-ttu-id="eeb7e-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="eeb7e-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="eeb7e-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="eeb7e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="eeb7e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="eeb7e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="eeb7e-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="eeb7e-111">Called by:</span></span>  <br/> |<span data-ttu-id="eeb7e-112">Proveedores de almacén de mensajes y aplicaciones cliente de RTF</span><span class="sxs-lookup"><span data-stu-id="eeb7e-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="eeb7e-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeb7e-113">Parameters</span></span>

<span data-ttu-id="eeb7e-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="eeb7e-114">_lpMessage_</span></span>
  
> <span data-ttu-id="eeb7e-115">[entrada] Puntero al mensaje que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="eeb7e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eeb7e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="eeb7e-117">[entrada] Máscara de bits de indicadores que se utilizan para indicar la versión de texto sin formato del mensaje o RTF ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="eeb7e-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="eeb7e-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="eeb7e-119">RTF_SYNC_BODY_CHANGED: Ha cambiado la versión de texto sin formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="eeb7e-120">RTF_SYNC_RTF_CHANGED: Ha cambiado la versión RTF del mensaje.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="eeb7e-121">Todos los demás bits en el parámetro _ulFlags_ están reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="eeb7e-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="eeb7e-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="eeb7e-123">[out] Puntero a una variable que indica si hay un mensaje actualizado.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="eeb7e-124">Es TRUE si hay un mensaje actualizado, FALSE en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eeb7e-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeb7e-125">Return value</span></span>

<span data-ttu-id="eeb7e-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="eeb7e-126">S_OK</span></span> 
  
> <span data-ttu-id="eeb7e-127">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eeb7e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eeb7e-128">Remarks</span></span>

<span data-ttu-id="eeb7e-129">Si la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) falta o es FALSE, antes de leer la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) en la función **RTFSync** se debe llamar con el RTF_SYNC_BODY_ Puede cambiar el conjunto de marca.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="eeb7e-130">Si no está establecido el indicador STORE_RTF_OK en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), esta función se debe llamar con el indicador RTF_SYNC_RTF_CHANGED establecer después de modificar **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="eeb7e-131">Si se han cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** , debe llamar a la función **RTFSync** con ambos conjunto de indicadores.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="eeb7e-132">Si el valor del parámetro _lpfMessageUpdated_ se establece en TRUE, el método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) debe llamarse para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="eeb7e-133">Si no se llama a **SaveChanges** , las modificaciones no se guardarán en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="eeb7e-134">Los proveedores de almacén de mensajes pueden utilizar **RTFSync** para mantener las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="eeb7e-135">Para obtener más información, vea [Compatibilidad con texto RTF para los proveedores de almacén de mensajes](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="eeb7e-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eeb7e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeb7e-136">See also</span></span>

- [<span data-ttu-id="eeb7e-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="eeb7e-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

