---
title: Compatibilidad con texto con formato en responsabilidades de cliente de los mensajes salientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820781"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="72fcf-103">Compatibilidad con texto con formato en los mensajes salientes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="72fcf-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="72fcf-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72fcf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72fcf-105">Las aplicaciones cliente de establecer la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o la propiedad **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="72fcf-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="72fcf-106">Los clientes que admiten sólo texto sin formato establecer sólo la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="72fcf-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="72fcf-107">Formato de texto de Rich (RTF)-tener en cuenta los clientes pueden establecer **PR_BODY** y propiedades **PR_RTF_COMPRESSED** o sólo **PR_RTF_COMPRESSED**, según el mensaje almacenar proveedor que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="72fcf-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="72fcf-108">Los clientes compatibles con HTML establecer la propiedad **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="72fcf-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="72fcf-109">Es importante para un cliente comprobar la propiedad de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de su almacén de mensajes para determinar si el almacén admite RTF.</span><span class="sxs-lookup"><span data-stu-id="72fcf-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="72fcf-110">Si el almacén de mensajes no es compatible con RTF, un cliente compatible con RTF establece las propiedades de la **PR_BODY** y el **PR_RTF_COMPRESSED** para todos los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="72fcf-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="72fcf-111">Si el almacén de mensajes es compatible con RTF, sólo **PR_RTF_COMPRESSED** necesita la propiedad va a establecer.</span><span class="sxs-lookup"><span data-stu-id="72fcf-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="72fcf-112">**Para establecer PR_RTF_COMPRESSED y asegúrese de que la sincronización se produce el proceso como sea necesarios, tener en cuenta RTF clientes**</span><span class="sxs-lookup"><span data-stu-id="72fcf-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="72fcf-113">Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED** , establecer marcadores de la MAPI_CREATE y la MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="72fcf-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="72fcf-114">MAPI_CREATE garantiza que los datos nuevos reemplazan los datos anteriores y MAPI_MODIFY le permite realizar los reemplazos.</span><span class="sxs-lookup"><span data-stu-id="72fcf-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="72fcf-115">Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , pasando STORE_UNCOMPRESSED_RTF si el almacén de mensajes establece el bit STORE_UNCOMPRESSED_RTF en su propiedad **PR_STORE_SUPPORT_MASK** , para obtener una versión de la **PR_RTF_COMPRESSED sin comprimir **secuencia devuelto desde **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="72fcf-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="72fcf-116">Escribir los datos de texto del mensaje en la secuencia sin comprimir devuelta desde **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="72fcf-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="72fcf-117">Confirmar y liberar las secuencias sin comprimir y comprimidas.</span><span class="sxs-lookup"><span data-stu-id="72fcf-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="72fcf-118">En este momento, si el proveedor de almacén de mensajes es compatible con RTF, ha realizado todo lo que es necesario.</span><span class="sxs-lookup"><span data-stu-id="72fcf-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="72fcf-119">Puede confiar en el proveedor de almacenamiento de mensajes para controlar el proceso de sincronización y la creación de la propiedad **PR_BODY** , si es necesario.</span><span class="sxs-lookup"><span data-stu-id="72fcf-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="72fcf-120">Sin embargo, si el proveedor de almacén de mensajes no es compatible con RTF, debe llamar a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato, se establecer el indicador RTF_SYNC_RTF_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="72fcf-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

