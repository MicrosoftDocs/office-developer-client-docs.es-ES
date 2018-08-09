---
title: Creación de texto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816642"
---
# <a name="creating-message-text"></a><span data-ttu-id="56c40-103">Creación de texto del mensaje</span><span class="sxs-lookup"><span data-stu-id="56c40-103">Creating message text</span></span>

<span data-ttu-id="56c40-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56c40-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56c40-105">Aunque algunos mensajes se componen de nada más que una lista de destinatarios y una línea de asunto, el contenido de la mayoría de los mensajes, específicamente IPM. Tenga en cuenta los mensajes, incluye texto.</span><span class="sxs-lookup"><span data-stu-id="56c40-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="56c40-106">Mensaje de texto puede ser sin formato o con formato y se almacena en tres propiedades: **PR\_cuerpo** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56c40-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="56c40-107">Si el cliente está basado en texto sin formato, establezca **PR\_cuerpo**.</span><span class="sxs-lookup"><span data-stu-id="56c40-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="56c40-108">Si admite texto con formato en el formato de texto enriquecido (RTF), establecer **PR_RTF_COMPRESSED** o ambos **PR_RTF_COMPRESSED** y **PR\_cuerpo**, dependiendo de que el proveedor de almacenamiento de mensaje que va a usar.</span><span class="sxs-lookup"><span data-stu-id="56c40-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="56c40-109">Cuando un cliente compatible con RTF está usando un almacén de mensajes compatible con RTF, Establece sólo **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="56c40-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="56c40-110">Cuando un cliente compatible con RTF está usando un almacén de mensajes compatible con RTF, Establece las dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="56c40-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="56c40-111">Si el cliente es compatible con HTML, establezca la propiedad **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="56c40-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="56c40-112">Determinar si el almacén de mensajes es compatible con el formato de texto enriquecido</span><span class="sxs-lookup"><span data-stu-id="56c40-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="56c40-113">Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56c40-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="56c40-114">Compruebe si el bit STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="56c40-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="56c40-115">Si se establece STORE_RTF_OK, el proveedor de almacenamiento de mensaje admite texto RTF.</span><span class="sxs-lookup"><span data-stu-id="56c40-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="56c40-116">Si no está establecido, el proveedor de almacén de mensajes es compatible con sólo texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="56c40-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="56c40-117">Determinar si el almacén de mensajes es compatible con HTML</span><span class="sxs-lookup"><span data-stu-id="56c40-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="56c40-118">Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_STORE_SUPPORT_MASK** .</span><span class="sxs-lookup"><span data-stu-id="56c40-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="56c40-119">Compruebe si el bit STORE_HTML_OK.</span><span class="sxs-lookup"><span data-stu-id="56c40-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="56c40-120">Si se establece STORE_HTML_OK, el proveedor de almacenamiento de mensaje admite texto HTML.</span><span class="sxs-lookup"><span data-stu-id="56c40-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="56c40-121">Establecer PR\_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="56c40-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="56c40-122">Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del mensaje para abrir la propiedad **PR_RTF_COMPRESSED** , especificando IID_IStream como el identificador de interfaz y estableciendo el indicador MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="56c40-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="56c40-123">Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , pasando el indicador STORE_UNCOMPRESSED_RTF si está establecido el bit STORE_UNCOMPRESSED_RTF en propiedad **PR_STORE_SUPPORT_MASK** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="56c40-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="56c40-124">La versión de la secuencia original mediante una llamada a su ** IUnknown:: Release ** (método).</span><span class="sxs-lookup"><span data-stu-id="56c40-124">Release the original stream by calling its ** IUnknown::Release ** method.</span></span> 
    
4. <span data-ttu-id="56c40-125">Llamar a ninguno ** IStream::Write ** o **IStream:: CopyTo** para escribir el texto del mensaje en la secuencia devuelta desde **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="56c40-125">Call either ** IStream::Write ** or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="56c40-126">Llamar a los métodos de **confirmación** y la **versión** en la secuencia devuelta desde el método **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="56c40-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="56c40-127">En este momento, si el proveedor de almacén de mensajes es compatible con RTF, ha realizado todo lo que es necesario.</span><span class="sxs-lookup"><span data-stu-id="56c40-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="56c40-128">Puede confiar en el proveedor de almacenamiento de mensajes para controlar la sincronización del contenido del mensaje y el formato y para crear el **PR\_cuerpo** (propiedad) si es necesario.</span><span class="sxs-lookup"><span data-stu-id="56c40-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="56c40-129">Los almacenes de mensajes RTF para llamar a [RTFSync](rtfsync.md) para controlar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="56c40-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="56c40-130">Si el formato RTF\_marca SYNC_BODY_CHANGED se establece en TRUE, el proveedor va a volver a calcular la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="56c40-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="56c40-131">Si su proveedor de almacén de mensajes no es compatible con RTF, también debe agregar el contenido del mensaje no RTF estableciendo la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="56c40-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="56c40-132">Establecer PR_HTML</span><span class="sxs-lookup"><span data-stu-id="56c40-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="56c40-133">Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_HTML** con la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="56c40-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="56c40-134">Llame a **IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="56c40-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="56c40-135">Llamar a **IStream:: Commit** e **IUnknown:: Release** en la secuencia para confirmar los cambios y liberar su memoria.</span><span class="sxs-lookup"><span data-stu-id="56c40-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="56c40-136">Establecer PR_BODY</span><span class="sxs-lookup"><span data-stu-id="56c40-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="56c40-137">Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_BODY** con la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="56c40-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="56c40-138">Llame a **IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="56c40-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="56c40-139">Llame a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato.</span><span class="sxs-lookup"><span data-stu-id="56c40-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="56c40-140">Puesto que se trata de un nuevo mensaje, establecer marcadores de la RTF_SYNC_RTF_CHANGED y el RTF_SYNC_BODY_CHANGED para indicar que ha cambiado la versión RTF y texto sin formato del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="56c40-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="56c40-141">**RTFSync** va a establecer las propiedades relacionadas que requiere el proveedor de almacenamiento de mensajes, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y escribirlos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="56c40-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="56c40-142">Llamar a **IStream:: Commit** e **IUnknown:: Release** en la secuencia para confirmar los cambios y liberar su memoria.</span><span class="sxs-lookup"><span data-stu-id="56c40-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

