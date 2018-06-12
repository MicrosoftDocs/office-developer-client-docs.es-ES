---
title: Escribir sin comprimir texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821000"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="14a06-103">Escribir sin comprimir texto con formato</span><span class="sxs-lookup"><span data-stu-id="14a06-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="14a06-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14a06-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14a06-105">Cuando se prepare para enviar un mensaje con texto con formato, establezca la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) al texto comprimido o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="14a06-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="14a06-106">Escribir texto comprimido en la propiedad **PR_RTF_COMPRESSED** es una operación de un uso intensivo de CPU muy y considerablemente puede afectar al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="14a06-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="14a06-107">Para mejorar el rendimiento de envío de mensajes con formato, ya sea:</span><span class="sxs-lookup"><span data-stu-id="14a06-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="14a06-108">Actualización de la CPU, una solución que no siempre pueda suceder.</span><span class="sxs-lookup"><span data-stu-id="14a06-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="14a06-109">O bien -</span><span class="sxs-lookup"><span data-stu-id="14a06-109">Or -</span></span>
    
- <span data-ttu-id="14a06-110">Escribir texto sin comprimir en la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="14a06-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="14a06-111">El procedimiento para establecer **PR_RTF_COMPRESSED** con texto sin comprimir es el mismo que si se establece con texto comprimido, con una excepción.</span><span class="sxs-lookup"><span data-stu-id="14a06-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="14a06-112">Cuando se llama a [WrapCompressedRTFStream](wrapcompressedrtfstream.md), establezca el indicador STORE_UNCOMPRESSED_RTF en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="14a06-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="14a06-113">Establecer el texto sin comprimir tiene la desventaja en que aumenta el tamaño de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="14a06-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

