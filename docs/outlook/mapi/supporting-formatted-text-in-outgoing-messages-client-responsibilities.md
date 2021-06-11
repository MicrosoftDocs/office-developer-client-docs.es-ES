---
title: Admitir texto con formato en las responsabilidades del cliente de mensajes salientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431606"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="283c5-103">Admitir texto con formato en mensajes salientes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="283c5-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="283c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="283c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="283c5-105">Las aplicaciones cliente establecen la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o la propiedad **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="283c5-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="283c5-106">Los clientes que solo admiten texto sin formato establecen **solo la PR_BODY** propiedad.</span><span class="sxs-lookup"><span data-stu-id="283c5-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="283c5-107">Los clientes con formato de texto  enriquecido (RTF)  pueden establecer propiedades PR_BODY y PR_RTF_COMPRESSED, o solo **PR_RTF_COMPRESSED**, según el proveedor de almacén de mensajes que se esté utilizando.</span><span class="sxs-lookup"><span data-stu-id="283c5-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="283c5-108">Los clientes con html establecen la **PR_HTML** propiedad.</span><span class="sxs-lookup"><span data-stu-id="283c5-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="283c5-109">Es importante que un cliente compruebe la propiedad PR_STORE_SUPPORT_MASK **del** almacén de mensajes ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para determinar si el almacén admite RTF.</span><span class="sxs-lookup"><span data-stu-id="283c5-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="283c5-110">Si el almacén de mensajes no es compatible con RTF, un cliente compatible con RTF establece las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** para cada mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="283c5-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="283c5-111">Si el almacén de mensajes es compatible con RTF, solo se debe establecer **la PR_RTF_COMPRESSED** propiedad.</span><span class="sxs-lookup"><span data-stu-id="283c5-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="283c5-112">**Para establecer PR_RTF_COMPRESSED y asegurarse de que el proceso de sincronización se produzca según sea necesario, los clientes con rtf-aware**</span><span class="sxs-lookup"><span data-stu-id="283c5-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="283c5-113">Llame al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED,** estableciendo las marcas MAPI_CREATE y MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="283c5-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="283c5-114">MAPI_CREATE garantiza que los nuevos datos reemplazan a los datos antiguos y MAPI_MODIFY permite realizar esos reemplazos.</span><span class="sxs-lookup"><span data-stu-id="283c5-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="283c5-115">Llame a la función [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) pasando STORE_UNCOMPRESSED_RTF si el almacén de mensajes establece el bit STORE_UNCOMPRESSED_RTF en su propiedad **PR_STORE_SUPPORT_MASK,** para obtener una versión sin comprimir de la secuencia **PR_RTF_COMPRESSED** devuelta de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="283c5-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="283c5-116">Escriba los datos de texto del mensaje en la secuencia sin comprimir devuelta de **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="283c5-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="283c5-117">Confirmar y liberar las secuencias sin comprimir y comprimidas.</span><span class="sxs-lookup"><span data-stu-id="283c5-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="283c5-118">En este momento, si el proveedor del almacén de mensajes admite RTF, ha hecho todo lo necesario.</span><span class="sxs-lookup"><span data-stu-id="283c5-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="283c5-119">Puede depender del proveedor del almacén de mensajes para controlar el proceso de sincronización y la creación de **la propiedad PR_BODY, si** es necesario.</span><span class="sxs-lookup"><span data-stu-id="283c5-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="283c5-120">Sin embargo, si el proveedor del almacén de mensajes no admite RTF, debe llamar a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato, estableciendo la marca RTF_SYNC_RTF_CHANGED mensaje.</span><span class="sxs-lookup"><span data-stu-id="283c5-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

