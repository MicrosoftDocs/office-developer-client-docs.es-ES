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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357004"
---
# <a name="message-content"></a><span data-ttu-id="64fe1-103">Contenido del mensaje</span><span class="sxs-lookup"><span data-stu-id="64fe1-103">Message Content</span></span>

  
  
<span data-ttu-id="64fe1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64fe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64fe1-105">Hay dos posibles codificaciones para el contenido del mensaje: uno con MIME, el otro con uuencode.</span><span class="sxs-lookup"><span data-stu-id="64fe1-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="64fe1-106">MIME es la codificación preferida.</span><span class="sxs-lookup"><span data-stu-id="64fe1-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="64fe1-107">Además, MAPI define una propiedad por destinatario, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que controla si se debe incluir la información de TNEF en un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="64fe1-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="64fe1-108">Por lo tanto, hay un total de cuatro formas de codificar el contenido del mensaje:</span><span class="sxs-lookup"><span data-stu-id="64fe1-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="64fe1-109">MIME con TNEF</span><span class="sxs-lookup"><span data-stu-id="64fe1-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="64fe1-110">MIME sin TNEF</span><span class="sxs-lookup"><span data-stu-id="64fe1-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="64fe1-111">uuencode con TNEF</span><span class="sxs-lookup"><span data-stu-id="64fe1-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="64fe1-112">uuencode sin TNEF</span><span class="sxs-lookup"><span data-stu-id="64fe1-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="64fe1-113">No se ha especificado el modo de elegir MIME o uuencode para los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="64fe1-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="64fe1-114">Las siguientes propiedades se excluyen de TNEF **:\*PR_SENDER_**, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="64fe1-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="64fe1-115">El resto de las propiedades de los mensajes transmitibles se incluyen en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="64fe1-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="64fe1-116">Las siguientes sugerencias tienen como objetivo proporcionar una lista de parámetros que la implementación puede usar para decidir cómo:</span><span class="sxs-lookup"><span data-stu-id="64fe1-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="64fe1-117">Si se va a codificar mediante MIME o uuencode para los mensajes salientes: Boolean.</span><span class="sxs-lookup"><span data-stu-id="64fe1-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="64fe1-118">Juego de caracteres que se va a usar para los mensajes salientes: String (que se copia directamente al parámetro charset) o enumeración (se traduce internamente a la cadena del juego de caracteres).</span><span class="sxs-lookup"><span data-stu-id="64fe1-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

