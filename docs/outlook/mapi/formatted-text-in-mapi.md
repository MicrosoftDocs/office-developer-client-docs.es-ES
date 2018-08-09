---
title: Texto con formato de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6b82a755cbf2c8bd0f1d3676d4560e131dce3bd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816872"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="10151-103">Texto con formato de MAPI</span><span class="sxs-lookup"><span data-stu-id="10151-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="10151-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10151-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10151-105">El texto de un mensaje se puede almacenar y transmite utilizando texto sin formato o texto con formato.</span><span class="sxs-lookup"><span data-stu-id="10151-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="10151-106">Texto con formato mejora el texto del mensaje mediante la modificación de su aspecto con, por ejemplo, uno o más fuentes, tamaños de fuente o los colores de texto.</span><span class="sxs-lookup"><span data-stu-id="10151-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="10151-107">Se recomienda que todos los clientes y siempre que sea posible, todos los proveedores de almacén de mensajes, admiten texto con formato.</span><span class="sxs-lookup"><span data-stu-id="10151-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="10151-108">Compatibilidad con texto con formato en los mensajes agrega valor por mejorar la legibilidad de mensaje y facilitan el control de mensajes y más eficaz.</span><span class="sxs-lookup"><span data-stu-id="10151-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="10151-109">Texto con formato se puede implementar en una variedad de formas.</span><span class="sxs-lookup"><span data-stu-id="10151-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="10151-110">La manera más común es con el formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="10151-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="10151-111">MAPI define tres propiedades transmisible para almacenar información de texto de mensaje: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para el texto sin formato, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para HTML y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para el texto RTF que se ha comprimido.</span><span class="sxs-lookup"><span data-stu-id="10151-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="10151-112">Debido a que la versión de un mensaje de texto con formato dos veces puede ser tan grande como la versión sin formato, se comprime el texto RTF antes de que se transfiere con el mensaje y se almacena en la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="10151-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="10151-113">Cuando sea la hora para mostrar el mensaje en la pantalla, es sin comprimir con una función de utilidad proporcionada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="10151-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="10151-114">MAPI define estas dos propiedades de texto de mensaje y mecanismos para la conversión entre ellas para que los clientes de tener en cuenta RTF pueden interoperar con los clientes y los sistemas de mensajería que no es compatible con formato de texto.</span><span class="sxs-lookup"><span data-stu-id="10151-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="10151-115">Sincronizar texto y formato</span><span class="sxs-lookup"><span data-stu-id="10151-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="10151-116">Describe cómo mantener sincronizado con el formato el texto de mensaje RTF.</span><span class="sxs-lookup"><span data-stu-id="10151-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="10151-117">Admitir texto con formato en los mensajes salientes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="10151-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="10151-118">Describe las responsabilidades de la aplicación de cliente para la compatibilidad con texto con formato en los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="10151-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="10151-119">Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="10151-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="10151-120">Describe las responsabilidades de la aplicación de cliente para la compatibilidad con texto con formato en los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="10151-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="10151-121">Admitir texto con formato: responsabilidades de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="10151-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="10151-122">Describe las responsabilidades del almacén de mensaje para admitir texto con formato.</span><span class="sxs-lookup"><span data-stu-id="10151-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="10151-123">Admitir texto con formato: representar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="10151-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="10151-124">Describe cómo elegir donde se representan los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="10151-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="10151-125">Admitir texto con formato: responsabilidades de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="10151-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="10151-126">Describe las responsabilidades de puerta de enlace para los mensajes de texto con formato entrante y saliente.</span><span class="sxs-lookup"><span data-stu-id="10151-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

