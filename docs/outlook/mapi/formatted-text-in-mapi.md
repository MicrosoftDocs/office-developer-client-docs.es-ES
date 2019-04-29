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
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408092"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="546a2-103">Texto con formato de MAPI</span><span class="sxs-lookup"><span data-stu-id="546a2-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="546a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="546a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="546a2-105">El texto de un mensaje se puede almacenar y transmitir con texto sin formato o texto con formato.</span><span class="sxs-lookup"><span data-stu-id="546a2-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="546a2-106">El texto con formato mejora el texto del mensaje al modificar su aspecto con, por ejemplo, una o varias fuentes, tamaños de fuente o colores del texto.</span><span class="sxs-lookup"><span data-stu-id="546a2-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="546a2-107">Se recomienda que todos los clientes y siempre que sea posible, todos los proveedores de almacenamiento de mensajes admitan texto con formato.</span><span class="sxs-lookup"><span data-stu-id="546a2-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="546a2-108">La compatibilidad con texto con formato en los mensajes agrega valor mejorando la legibilidad de los mensajes y haciendo que el control de mensajes sea más fácil y eficaz.</span><span class="sxs-lookup"><span data-stu-id="546a2-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="546a2-109">El texto con formato puede implementarse de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="546a2-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="546a2-110">La forma más común es con el formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="546a2-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="546a2-111">MAPI define tres propiedades transmitibles para la retención de información de texto del mensaje: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para texto sin formato, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para HTML y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para el texto RTF que se ha comprimido.</span><span class="sxs-lookup"><span data-stu-id="546a2-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="546a2-112">Debido a que la versión con formato de un texto de mensaje puede ser dos veces mayor que la versión sin formato, el texto RTF se comprime antes de transferirlo con el mensaje y se almacena en la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="546a2-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="546a2-113">Cuando es el momento de mostrar el mensaje en la pantalla, se descomprime con una función de utilidad proporcionada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="546a2-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="546a2-114">MAPI define estas dos propiedades de texto de mensaje y mecanismos de conversión entre ellos para que los clientes compatibles con RTF puedan interoperar con los clientes y los sistemas de mensajería que no admiten el texto con formato.</span><span class="sxs-lookup"><span data-stu-id="546a2-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="546a2-115">Sincronizar texto y formato</span><span class="sxs-lookup"><span data-stu-id="546a2-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="546a2-116">Describe cómo se debe sincronizar el texto del mensaje RTF con el formato.</span><span class="sxs-lookup"><span data-stu-id="546a2-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="546a2-117">Admitir texto con formato en los mensajes salientes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="546a2-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="546a2-118">Describe las responsabilidades de la aplicación cliente para admitir texto con formato en los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="546a2-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="546a2-119">Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="546a2-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="546a2-120">Describe las responsabilidades de la aplicación cliente para admitir texto con formato en los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="546a2-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="546a2-121">Admitir texto con formato: responsabilidades del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="546a2-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="546a2-122">Describe las responsabilidades del almacén de mensajes para admitir texto con formato.</span><span class="sxs-lookup"><span data-stu-id="546a2-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="546a2-123">Compatibilidad con texto con formato: representar datos adJuntos</span><span class="sxs-lookup"><span data-stu-id="546a2-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="546a2-124">Describe cómo elegir dónde se representan los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="546a2-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="546a2-125">Compatibilidad con texto con formato: responsabilidades de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="546a2-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="546a2-126">Describe las responsabilidades de puerta de enlace para los mensajes entrantes y salientes de texto con formato.</span><span class="sxs-lookup"><span data-stu-id="546a2-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

