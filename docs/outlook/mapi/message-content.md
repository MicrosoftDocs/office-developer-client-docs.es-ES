---
title: Contenido del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818387"
---
# <a name="message-content"></a><span data-ttu-id="8c484-103">Contenido del mensaje</span><span class="sxs-lookup"><span data-stu-id="8c484-103">Message Content</span></span>

  
  
<span data-ttu-id="8c484-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c484-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c484-105">Hay dos codificaciones posibles para el contenido del mensaje: uno mediante MIME, la otra mediante uuencode.</span><span class="sxs-lookup"><span data-stu-id="8c484-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="8c484-106">MIME es la codificación preferida.</span><span class="sxs-lookup"><span data-stu-id="8c484-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="8c484-107">Además, MAPI define una propiedad por destinatario, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que controla si se debe incluir la información de TNEF en un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="8c484-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="8c484-108">Por tanto, hay un total de cuatro maneras de codificar el contenido de mensaje:</span><span class="sxs-lookup"><span data-stu-id="8c484-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="8c484-109">MIME con TNEF</span><span class="sxs-lookup"><span data-stu-id="8c484-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="8c484-110">MIME sin TNEF</span><span class="sxs-lookup"><span data-stu-id="8c484-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="8c484-111">UUENCODE con TNEF</span><span class="sxs-lookup"><span data-stu-id="8c484-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="8c484-112">UUENCODE sin TNEF</span><span class="sxs-lookup"><span data-stu-id="8c484-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="8c484-113">No se especifica cómo elegir MIME o uuencode para mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="8c484-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="8c484-114">Las siguientes propiedades se excluyen de TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="8c484-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="8c484-115">Todas las demás propiedades de mensaje transmisible se incluyen en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="8c484-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="8c484-116">Las siguientes sugerencias están diseñadas para proporcionar una lista de parámetros que la implementación puede decidir cómo se admite:</span><span class="sxs-lookup"><span data-stu-id="8c484-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="8c484-117">Si se va a codificar con MIME o uuencode para mensajes salientes: boolean.</span><span class="sxs-lookup"><span data-stu-id="8c484-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="8c484-118">Conjunto que se usará para los mensajes salientes de caracteres: cadena (copiados directamente al parámetro charset) o enumeración (traducido internamente en cadena de juego de caracteres).</span><span class="sxs-lookup"><span data-stu-id="8c484-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

