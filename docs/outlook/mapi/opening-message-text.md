---
title: Abrir un mensaje de texto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348583"
---
# <a name="opening-message-text"></a><span data-ttu-id="7ec9e-103">Abrir un mensaje de texto</span><span class="sxs-lookup"><span data-stu-id="7ec9e-103">Opening message text</span></span>

<span data-ttu-id="7ec9e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ec9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ec9e-105">El texto de un mensaje se almacena en la propiedad **del\_cuerpo del RP** o en la propiedad **comprimida de\_RTF\_de CP** .</span><span class="sxs-lookup"><span data-stu-id="7ec9e-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="7ec9e-106">Para obtener más información, vea el **cuerpo de PR\_** ([PidTagBody](pidtagbody-canonical-property.md)), el **HTML de PR\_** ([PidTagHtml](pidtaghtml-canonical-property.md)) y el archivo. **\_\_RTF comprimido** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7ec9e-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="7ec9e-107">Si admite el formato de texto enriquecido (RTF), Abra **PR\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="7ec9e-108">Si no admite RTF, abra el **cuerpo del\_PR**.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="7ec9e-109">Dado que el texto de un mensaje puede ser grande independientemente de si tiene o no formato, use **IMAPIProp:: OpenProperty** para abrir estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="7ec9e-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7ec9e-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="7ec9e-111">Para mostrar el texto del mensaje con formato</span><span class="sxs-lookup"><span data-stu-id="7ec9e-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="7ec9e-112">Si usa un almacén de mensajes no compatible con RTF, tal y como indica la ausencia de la marca STORE_RTF_OK en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la tienda:</span><span class="sxs-lookup"><span data-stu-id="7ec9e-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="7ec9e-113">Llame al método **IMAPIProp:: GetProps** del mensaje para recuperar la propiedad **PR_RTF_IN_SYNC** .</span><span class="sxs-lookup"><span data-stu-id="7ec9e-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="7ec9e-114">Para obtener más información, vea [IMAPIProp:: GetProps](imapiprop-getprops.md) y **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7ec9e-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="7ec9e-115">Llame a RTFSync para sincronizar la propiedad PR_BODY del mensaje con la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="7ec9e-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="7ec9e-116">Para obtener más información, vea [RTFSync](rtfsync.md), **PR_BODY**y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="7ec9e-117">Pasar la marca RTF_SYNC_BODY_CHANGED si se produce un error en la llamada para recuperar **PR_RTF_IN_SYNC** porque la propiedad no existe o se establece en false.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="7ec9e-118">Si **RTFSync** devuelve true (lo que indica que se realizaron cambios), llame al método **IMAPIProp:: SaveChanges** del mensaje para almacenarlos de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="7ec9e-119">Para obtener más información, vea [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="7ec9e-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="7ec9e-120">Independientemente de si usa o no un almacén de mensajes que reconozca el formato RTF:</span><span class="sxs-lookup"><span data-stu-id="7ec9e-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="7ec9e-121">Llame a **IMAPIProp:: OpenProperty** para abrir la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="7ec9e-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="7ec9e-122">Para obtener más información, vea [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="7ec9e-123">Si **PR_RTF_COMPRESSED** no está disponible, llame a **OpenProperty** para abrir la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="7ec9e-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="7ec9e-124">Llame a la función **WrapCompressedRTFStream** para crear una versión sin comprimir de los datos RTF comprimidos, si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="7ec9e-125">Para obtener más información, vea [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="7ec9e-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="7ec9e-126">Copie el texto con formato del flujo en el punto adecuado en el formulario de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="7ec9e-127">Para mostrar texto de mensaje sin formato</span><span class="sxs-lookup"><span data-stu-id="7ec9e-127">To display plain message text</span></span>
  
1. <span data-ttu-id="7ec9e-128">Llame al método **IMAPIProp:: GetProps** del mensaje para recuperar la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="7ec9e-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="7ec9e-129">Para obtener más información, vea [IMAPIProp:: GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="7ec9e-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="7ec9e-130">Si **GetProps** devuelve PT_ERROR para el tipo de propiedad en la MAPI_E_NOT_ENOUGH_MEMORY o la estructura del valor de la propiedad, llame al método **IMAPIProp:: OpenProperty** del mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="7ec9e-131">Pase **PR_BODY** como la etiqueta Property y IID_IStream como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="7ec9e-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7ec9e-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="7ec9e-133">Copie el texto sin formato del flujo en el punto adecuado del formulario de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ec9e-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

