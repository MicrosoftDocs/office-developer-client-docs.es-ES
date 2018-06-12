---
title: Texto del mensaje de apertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818443"
---
# <a name="opening-message-text"></a><span data-ttu-id="a8785-103">Texto del mensaje de apertura</span><span class="sxs-lookup"><span data-stu-id="a8785-103">Opening message text</span></span>

<span data-ttu-id="a8785-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8785-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8785-105">El texto de un mensaje se almacena en su **PR\_cuerpo** (propiedad) o **PR\_RTF\_COMPRIMIDO** (propiedad).</span><span class="sxs-lookup"><span data-stu-id="a8785-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="a8785-106">Para obtener más información, vea **PR\_cuerpo** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), y **PR\_RTF\_COMPRIMIDO** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8785-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="a8785-107">Si admite el formato de texto enriquecido (RTF), abra **PR\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a8785-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="a8785-108">Si no se admiten RTF, abra **PR\_cuerpo**.</span><span class="sxs-lookup"><span data-stu-id="a8785-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="a8785-109">Debido a que el texto de un mensaje puede ser grande, independientemente de si o no tiene el formato, use **IMAPIProp::OpenProperty** para abrir estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a8785-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="a8785-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a8785-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="a8785-111">Para mostrar con formato de texto del mensaje</span><span class="sxs-lookup"><span data-stu-id="a8785-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="a8785-112">Si está utilizando un almacén de mensajes de tener en cuenta que no sean RTF, tal como se indica por la ausencia de la marca STORE_RTF_OK en propiedad de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la tienda:</span><span class="sxs-lookup"><span data-stu-id="a8785-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="a8785-113">Llamar al método **IMAPIProp::GetProps** del mensaje para recuperar la propiedad **PR_RTF_IN_SYNC** .</span><span class="sxs-lookup"><span data-stu-id="a8785-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="a8785-114">Para obtener más información, vea [IMAPIProp::GetProps](imapiprop-getprops.md) y **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8785-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="a8785-115">Llame a RTFSync para sincronizar la propiedad del mensaje PR_BODY con la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="a8785-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="a8785-116">Para obtener más información, vea [RTFSync](rtfsync.md), **PR_BODY**y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a8785-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="a8785-117">Pase el RTF_SYNC_BODY_CHANGED marcar si falla la llamada para recuperar **PR_RTF_IN_SYNC** debido a que la propiedad no existe o está establecida en FALSE.</span><span class="sxs-lookup"><span data-stu-id="a8785-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="a8785-118">Si **RTFSync** devuelve TRUE, que indica que se han realizado cambios, llamar al método **IMAPIProp::SaveChanges** de los mensajes para almacenarlos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="a8785-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="a8785-119">Para obtener más información, vea [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="a8785-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="a8785-120">Independientemente de si utiliza un mensaje RTF para almacenar:</span><span class="sxs-lookup"><span data-stu-id="a8785-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="a8785-121">Llame a **IMAPIProp::OpenProperty** para abrir la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="a8785-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="a8785-122">Para obtener más información, vea [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a8785-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="a8785-123">Si **PR_RTF_COMPRESSED** no está disponible, llamar **OpenProperty** para abrir la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="a8785-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="a8785-124">Llame a la función **WrapCompressedRTFStream** para crear una versión sin comprimir de los datos RTF comprimidos, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="a8785-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="a8785-125">Para obtener más información, vea [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="a8785-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="a8785-126">Copiar el texto con formato de la secuencia al lugar adecuado en el formulario de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8785-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="a8785-127">Para mostrar el texto sin formato del mensaje</span><span class="sxs-lookup"><span data-stu-id="a8785-127">To display plain message text</span></span>
  
1. <span data-ttu-id="a8785-128">Llamar al método **IMAPIProp::GetProps** del mensaje para recuperar la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="a8785-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="a8785-129">Para obtener más información, vea [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="a8785-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="a8785-130">Si **GetProps** devuelve puede ser PT_ERROR para el tipo de propiedad en la estructura de valor de propiedad o MAPI_E_NOT_ENOUGH_MEMORY, llame al método **IMAPIProp::OpenProperty** del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8785-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="a8785-131">Pase **PR_BODY** como la etiqueta de propiedad y IID_IStream como el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="a8785-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="a8785-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a8785-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="a8785-133">Copiar el texto sin formato de la secuencia al lugar adecuado en el formulario de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8785-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

