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
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435463"
---
# <a name="message-content"></a><span data-ttu-id="46ea2-103">Contenido del mensaje</span><span class="sxs-lookup"><span data-stu-id="46ea2-103">Message Content</span></span>

  
  
<span data-ttu-id="46ea2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46ea2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46ea2-105">Hay dos codificaciones posibles para el contenido del mensaje: una con MIME y otra con uuencode.</span><span class="sxs-lookup"><span data-stu-id="46ea2-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="46ea2-106">MIME es la codificación preferida.</span><span class="sxs-lookup"><span data-stu-id="46ea2-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="46ea2-107">Además, MAPI define una propiedad por destinatario, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que rige si la información de TNEF debe incluirse o no en un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="46ea2-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="46ea2-108">Por lo tanto, hay un total de cuatro formas de codificar el contenido del mensaje:</span><span class="sxs-lookup"><span data-stu-id="46ea2-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="46ea2-109">MIME con TNEF</span><span class="sxs-lookup"><span data-stu-id="46ea2-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="46ea2-110">MIME sin TNEF</span><span class="sxs-lookup"><span data-stu-id="46ea2-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="46ea2-111">uuencode con TNEF</span><span class="sxs-lookup"><span data-stu-id="46ea2-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="46ea2-112">uuencode sin TNEF</span><span class="sxs-lookup"><span data-stu-id="46ea2-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="46ea2-113">No se especifica cómo elegir MIME o uuencode para los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="46ea2-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="46ea2-114">Las siguientes propiedades se excluyen de TNEF: **\* PR_SENDER_**, **PR_ATTACH_DATA_ \***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="46ea2-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="46ea2-115">Todas las demás propiedades de mensaje transmitibles se incluyen en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="46ea2-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="46ea2-116">Las siguientes sugerencias están diseñadas para proporcionar una lista de parámetros que la implementación puede decidir cómo admitir:</span><span class="sxs-lookup"><span data-stu-id="46ea2-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="46ea2-117">Si se codifica mediante MIME o uuencode para mensajes salientes: booleano.</span><span class="sxs-lookup"><span data-stu-id="46ea2-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="46ea2-118">Juego de caracteres que se usará para los mensajes salientes: cadena (copiada directamente en el parámetro charset) o enumeración (traducida internamente a cadena charset).</span><span class="sxs-lookup"><span data-stu-id="46ea2-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

