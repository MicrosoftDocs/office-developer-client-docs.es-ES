---
title: Crear el texto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428007"
---
# <a name="creating-message-text"></a><span data-ttu-id="dc191-103">Crear el texto del mensaje</span><span class="sxs-lookup"><span data-stu-id="dc191-103">Creating message text</span></span>

<span data-ttu-id="dc191-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc191-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc191-105">Aunque algunos mensajes no están hechos de nada más que una lista de destinatarios y una línea de asunto, el contenido de la mayoría de los mensajes, específicamente IPM. Note messages, includes text.</span><span class="sxs-lookup"><span data-stu-id="dc191-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="dc191-106">El texto del mensaje puede ser sin formato o estar almacenado en tres propiedades: **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dc191-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="dc191-107">Si el cliente está basado en texto sin formato, establezca **PR \_ BODY**.</span><span class="sxs-lookup"><span data-stu-id="dc191-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="dc191-108">Si admite texto con formato en formato de  texto enriquecido (RTF), establezca PR_RTF_COMPRESSED solo o **bien PR_RTF_COMPRESSED** y **PR \_ BODY**, en función del proveedor de almacenamiento de mensajes que use.</span><span class="sxs-lookup"><span data-stu-id="dc191-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="dc191-109">Cuando un cliente compatible con RTF usa un almacén de mensajes compatible con RTF, establece PR_RTF_COMPRESSED **solo.**</span><span class="sxs-lookup"><span data-stu-id="dc191-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="dc191-110">Cuando un cliente compatible con RTF usa un almacén de mensajes no compatible con RTF, establece ambas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc191-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="dc191-111">Si el cliente admite HTML, establezca la **PR_HTML** cliente.</span><span class="sxs-lookup"><span data-stu-id="dc191-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="dc191-112">Determinar si el almacén de mensajes admite el formato de texto enriquecido</span><span class="sxs-lookup"><span data-stu-id="dc191-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="dc191-113">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dc191-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="dc191-114">Compruebe si hay STORE_RTF_OK bits.</span><span class="sxs-lookup"><span data-stu-id="dc191-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="dc191-115">Si STORE_RTF_OK se establece, el proveedor del almacén de mensajes admite texto RTF.</span><span class="sxs-lookup"><span data-stu-id="dc191-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="dc191-116">Si no se establece, el proveedor de almacenamiento de mensajes solo admite texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="dc191-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="dc191-117">Determinar si el almacén de mensajes admite HTML</span><span class="sxs-lookup"><span data-stu-id="dc191-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="dc191-118">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar **PR_STORE_SUPPORT_MASK** propiedad.</span><span class="sxs-lookup"><span data-stu-id="dc191-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="dc191-119">Compruebe si hay STORE_HTML_OK bits.</span><span class="sxs-lookup"><span data-stu-id="dc191-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="dc191-120">Si STORE_HTML_OK se establece, el proveedor de al almacenamiento de mensajes admite texto HTML.</span><span class="sxs-lookup"><span data-stu-id="dc191-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-pr_rtf_compressed"></a><span data-ttu-id="dc191-121">Establecer pr \_ RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="dc191-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="dc191-122">Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del mensaje para abrir la propiedad **PR_RTF_COMPRESSED,** especificando IID_IStream como identificador de interfaz y estableciendo la marca MAPI_CREATE mensaje.</span><span class="sxs-lookup"><span data-stu-id="dc191-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="dc191-123">Llama a [la función WrapCompressedRTFStream](wrapcompressedrtfstream.md) y pasa la marca STORE_UNCOMPRESSED_RTF si el bit STORE_UNCOMPRESSED_RTF está establecido en la propiedad PR_STORE_SUPPORT_MASK del **almacén de** mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc191-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="dc191-124">Libere la secuencia original llamando a su método \*\* IUnknown::Release \*\*.</span><span class="sxs-lookup"><span data-stu-id="dc191-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="dc191-125">Llama a \*\* IStream::Write \*\* o **IStream::CopyTo** para escribir el texto del mensaje en la secuencia devuelta desde **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="dc191-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="dc191-126">Llama a **los métodos Commit** **y Release** en la secuencia devuelta desde el **método OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="dc191-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="dc191-127">En este punto, si el proveedor de almacenamiento de mensajes admite RTF, ha hecho todo lo necesario.</span><span class="sxs-lookup"><span data-stu-id="dc191-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="dc191-128">Puede depender del proveedor del almacén de mensajes para controlar la sincronización del contenido y el formato del mensaje y para crear la propiedad **PR \_ BODY** si es necesario.</span><span class="sxs-lookup"><span data-stu-id="dc191-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="dc191-129">Los almacenes de mensajes rtf-aware llaman [a RTFSync](rtfsync.md) para controlar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="dc191-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="dc191-130">Si la marca de SYNC_BODY_CHANGED RTF se establece en TRUE, el proveedor volverá a \_ compilar **la PR_BODY** propiedad.</span><span class="sxs-lookup"><span data-stu-id="dc191-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="dc191-131">Si el proveedor del almacén de mensajes no admite RTF, también debe agregar contenido de mensajes que no sea RTF estableciendo la **propiedad PR_BODY** mensaje.</span><span class="sxs-lookup"><span data-stu-id="dc191-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-pr_html"></a><span data-ttu-id="dc191-132">Establecer PR_HTML</span><span class="sxs-lookup"><span data-stu-id="dc191-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="dc191-133">Llame al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la **PR_HTML** con la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="dc191-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="dc191-134">Llame **a IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="dc191-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="dc191-135">Llama **a IStream::Commit** **e IUnknown::Release** en la secuencia para confirmar los cambios y liberar su memoria.</span><span class="sxs-lookup"><span data-stu-id="dc191-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-pr_body"></a><span data-ttu-id="dc191-136">Establecer PR_BODY</span><span class="sxs-lookup"><span data-stu-id="dc191-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="dc191-137">Llame al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir **la PR_BODY** con la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="dc191-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="dc191-138">Llame **a IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="dc191-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="dc191-139">Llame a [la función RTFSync](rtfsync.md) para sincronizar el texto con el formato.</span><span class="sxs-lookup"><span data-stu-id="dc191-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="dc191-140">Dado que se trata de un mensaje nuevo, establezca las marcas RTF_SYNC_RTF_CHANGED y RTF_SYNC_BODY_CHANGED para indicar que tanto la versión RTF como la versión de texto sin formato del texto del mensaje han cambiado.</span><span class="sxs-lookup"><span data-stu-id="dc191-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="dc191-141">**RTFSync** establecerá varias propiedades relacionadas que el proveedor de almacenamiento de mensajes requiere, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y las escribirá en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dc191-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="dc191-142">Llama **a IStream::Commit** **e IUnknown::Release** en la secuencia para confirmar los cambios y liberar su memoria.</span><span class="sxs-lookup"><span data-stu-id="dc191-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

