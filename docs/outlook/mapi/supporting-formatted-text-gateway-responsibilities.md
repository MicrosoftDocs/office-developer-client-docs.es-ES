---
title: Compatibilidad con responsabilidades de puerta de enlace de texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419432"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="95d2b-103">Admitir texto con formato: responsabilidades de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="95d2b-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="95d2b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95d2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="95d2b-105">**Para controlar el formato de texto enriquecido para mensajes salientes, puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="95d2b-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="95d2b-106">Recupera solo la propiedad de **PR_RTF_COMPRESSED** de un mensaje ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="95d2b-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="95d2b-107">La principal ventaja de recuperar solo la propiedad **PR_RTF_COMPRESSED** es que no es necesario enviar el texto del mensaje entre máquinas si la puerta de enlace y el almacén de mensajes existen en máquinas diferentes.</span><span class="sxs-lookup"><span data-stu-id="95d2b-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="95d2b-108">Genere el texto del mensaje a partir del texto con formato llamando a la función de biblioteca RTF **HrTextFromCompressedRTFStream** o, si el mensaje se almacena localmente, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="95d2b-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="95d2b-109">La RTF_SYNC_RTF_CHANGED debe establecerse en la llamada a **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="95d2b-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="95d2b-110">Para obtener más información, vea [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="95d2b-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="95d2b-111">Realice modificaciones irreversibles en el texto del mensaje, como colocar caracteres no admitidos.</span><span class="sxs-lookup"><span data-stu-id="95d2b-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="95d2b-112">Asegúrese de que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y todas las propiedades auxiliares RTF estén establecidas o ausentes.</span><span class="sxs-lookup"><span data-stu-id="95d2b-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="95d2b-113">Si se realizaron modificaciones, llama a **RTFSync** con las marcas RTF_SYNC_RTF_CHANGED y RTF_SYNC_BODY_CHANGED establecidas.</span><span class="sxs-lookup"><span data-stu-id="95d2b-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="95d2b-114">**RTFSync** recalculará las propiedades auxiliares RTF del texto modificado.</span><span class="sxs-lookup"><span data-stu-id="95d2b-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="95d2b-115">Realice modificaciones invertibles en el texto del mensaje, como insertar marcadores de posición de datos adjuntos y realizar conversiones de páginas de código no destructivas.</span><span class="sxs-lookup"><span data-stu-id="95d2b-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="95d2b-116">Envíe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="95d2b-116">Send the message.</span></span>
    
 <span data-ttu-id="95d2b-117">**Para controlar el formato de texto enriquecido para mensajes entrantes, puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="95d2b-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="95d2b-118">Invierta las modificaciones de texto del mensaje que se realizaron directamente antes de enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="95d2b-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="95d2b-119">Llame **a RTFSync** si el mensaje contiene las propiedades **PR_RTF_COMPRESSED** y **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="95d2b-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="95d2b-120">Actualice el mensaje en el almacén de mensajes con **la PR_RTF_COMPRESSED** propiedad si el mensaje lo contiene; actualizar con la **propiedad PR_BODY** solo **si PR_RTF_COMPRESSED** está ausente.</span><span class="sxs-lookup"><span data-stu-id="95d2b-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="95d2b-121">Descarte **PR_BODY** si el mensaje contiene esta propiedad y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="95d2b-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="95d2b-122">Las puertas de enlace llaman a **RTFSync** para evitar transmitir el texto del mensaje y el texto con formato si el almacén de mensajes está en un equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="95d2b-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="95d2b-123">Si la puerta de enlace es local, puede establecer ambas propiedades y permitir que el almacén de mensajes realice la sincronización.</span><span class="sxs-lookup"><span data-stu-id="95d2b-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

