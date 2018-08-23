---
title: Escribir texto con formato sin comprimir
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577047"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="e70cf-103">Escribir texto con formato sin comprimir</span><span class="sxs-lookup"><span data-stu-id="e70cf-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="e70cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e70cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e70cf-105">Cuando se prepare para enviar un mensaje con texto con formato, establezca la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) al texto comprimido o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="e70cf-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="e70cf-106">Escribir texto comprimido en la propiedad **PR_RTF_COMPRESSED** es una operación de un uso intensivo de CPU muy y considerablemente puede afectar al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e70cf-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="e70cf-107">Para mejorar el rendimiento de envío de mensajes con formato, ya sea:</span><span class="sxs-lookup"><span data-stu-id="e70cf-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="e70cf-108">Actualización de la CPU, una solución que no siempre pueda suceder.</span><span class="sxs-lookup"><span data-stu-id="e70cf-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="e70cf-109">O bien -</span><span class="sxs-lookup"><span data-stu-id="e70cf-109">Or -</span></span>
    
- <span data-ttu-id="e70cf-110">Escribir texto sin comprimir en la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="e70cf-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="e70cf-111">El procedimiento para establecer **PR_RTF_COMPRESSED** con texto sin comprimir es el mismo que si se establece con texto comprimido, con una excepción.</span><span class="sxs-lookup"><span data-stu-id="e70cf-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="e70cf-112">Cuando se llama a [WrapCompressedRTFStream](wrapcompressedrtfstream.md), establezca el indicador STORE_UNCOMPRESSED_RTF en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="e70cf-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e70cf-113">Establecer el texto sin comprimir tiene la desventaja en que aumenta el tamaño de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e70cf-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

