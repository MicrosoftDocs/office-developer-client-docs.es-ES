---
title: Compatibilidad con las responsabilidades de puerta de enlace de texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d369093589ffad03bf087b02905c443cf6f46c34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564272"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="557da-103">Admitir texto con formato: responsabilidades de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="557da-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="557da-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="557da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="557da-105">**Para controlar el formato de texto enriquecido para los mensajes salientes, las puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="557da-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="557da-106">Recuperar sólo la propiedad de un mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) desde el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="557da-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="557da-107">La principal ventaja de recuperación sólo la propiedad **PR_RTF_COMPRESSED** es que el texto del mensaje no es necesario que se envíen entre máquinas si existen la puerta de enlace y el almacén de mensajes en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="557da-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="557da-108">Generar el texto del mensaje de texto con formato ya sea mediante una llamada a la función de biblioteca RTF **HrTextFromCompressedRTFStream** o, si el mensaje se almacena localmente, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="557da-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="557da-109">El indicador RTF_SYNC_RTF_CHANGED debe establecerse en la llamada a **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="557da-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="557da-110">Para obtener más información, vea [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="557da-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="557da-111">Realizar modificaciones irreversibles en el texto del mensaje, como eliminarla de caracteres no admitidos.</span><span class="sxs-lookup"><span data-stu-id="557da-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="557da-112">Asegúrese de que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y todas las propiedades de auxilliary RTF se establecen o ausente.</span><span class="sxs-lookup"><span data-stu-id="557da-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="557da-113">Si se han realizado las modificaciones, llame al método **RTFSync** con el RTF_SYNC_RTF_CHANGED y el RTF_SYNC_BODY_CHANGED conjunto de indicadores.</span><span class="sxs-lookup"><span data-stu-id="557da-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="557da-114">**RTFSync** se volverá a calcular las propiedades de auxilliary RTF desde el texto modificado.</span><span class="sxs-lookup"><span data-stu-id="557da-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="557da-115">Realice las modificaciones en el texto del mensaje, como la inserción de los marcadores de posición de datos adjuntos y realizar las conversiones de página de código no destructiva irreversible.</span><span class="sxs-lookup"><span data-stu-id="557da-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="557da-116">Enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="557da-116">Send the message.</span></span>
    
 <span data-ttu-id="557da-117">**Para controlar el formato de texto enriquecido para los mensajes entrantes, las puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="557da-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="557da-118">Invertir las modificaciones de texto de mensaje que se han realizado directamente antes de que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="557da-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="557da-119">Llamar a **RTFSync** si el mensaje contiene las propiedades de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="557da-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="557da-120">Actualizar el mensaje en el almacén de mensajes con la propiedad **PR_RTF_COMPRESSED** si el mensaje contiene actualizar con la propiedad **PR_BODY** sólo si está ausente **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="557da-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="557da-121">Descartar **PR_BODY** si el mensaje contiene esta propiedad y la **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="557da-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="557da-122">Las puertas de enlace, llame a **RTFSync** para evitar transmitir el texto del mensaje y el texto con formato si se encuentra el almacén de mensajes en un equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="557da-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="557da-123">Si la puerta de enlace es local, puede establecer las dos propiedades y permitir que el almacén de mensajes para llevar a cabo la sincronización.</span><span class="sxs-lookup"><span data-stu-id="557da-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

