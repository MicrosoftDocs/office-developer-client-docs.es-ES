---
title: Contenido del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586084"
---
# <a name="message-content"></a><span data-ttu-id="32757-103">Contenido del mensaje</span><span class="sxs-lookup"><span data-stu-id="32757-103">Message Content</span></span>

  
  
<span data-ttu-id="32757-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32757-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32757-105">Hay dos codificaciones posibles para el contenido del mensaje: uno mediante MIME, la otra mediante uuencode.</span><span class="sxs-lookup"><span data-stu-id="32757-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="32757-106">MIME es la codificación preferida.</span><span class="sxs-lookup"><span data-stu-id="32757-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="32757-107">Además, MAPI define una propiedad por destinatario, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que controla si se debe incluir la información de TNEF en un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="32757-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="32757-108">Por tanto, hay un total de cuatro maneras de codificar el contenido de mensaje:</span><span class="sxs-lookup"><span data-stu-id="32757-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="32757-109">MIME con TNEF</span><span class="sxs-lookup"><span data-stu-id="32757-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="32757-110">MIME sin TNEF</span><span class="sxs-lookup"><span data-stu-id="32757-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="32757-111">UUENCODE con TNEF</span><span class="sxs-lookup"><span data-stu-id="32757-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="32757-112">UUENCODE sin TNEF</span><span class="sxs-lookup"><span data-stu-id="32757-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="32757-113">No se especifica cómo elegir MIME o uuencode para mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="32757-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="32757-114">Las siguientes propiedades se excluyen de TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="32757-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="32757-115">Todas las demás propiedades de mensaje transmisible se incluyen en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="32757-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="32757-116">Las siguientes sugerencias están diseñadas para proporcionar una lista de parámetros que la implementación puede decidir cómo se admite:</span><span class="sxs-lookup"><span data-stu-id="32757-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="32757-117">Si se va a codificar con MIME o uuencode para mensajes salientes: boolean.</span><span class="sxs-lookup"><span data-stu-id="32757-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="32757-118">Conjunto que se usará para los mensajes salientes de caracteres: cadena (copiados directamente al parámetro charset) o enumeración (traducido internamente en cadena de juego de caracteres).</span><span class="sxs-lookup"><span data-stu-id="32757-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

