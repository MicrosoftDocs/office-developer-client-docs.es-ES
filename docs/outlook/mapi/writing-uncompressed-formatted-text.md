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
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426327"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="cbcdf-103">Escribir texto con formato sin comprimir</span><span class="sxs-lookup"><span data-stu-id="cbcdf-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="cbcdf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbcdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbcdf-105">Cuando se prepara para enviar un mensaje con texto con formato, establezca la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje en texto comprimido o descomprimido.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="cbcdf-106">Escribir texto comprimido en la propiedad **PR_RTF_COMPRESSED** es una operación que conSUME mucha CPU y puede afectar considerablemente al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="cbcdf-107">Para mejorar el rendimiento del envío de mensajes con formato, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbcdf-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="cbcdf-108">Actualizar la CPU, una solución que no siempre es plausible.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="cbcdf-109">O</span><span class="sxs-lookup"><span data-stu-id="cbcdf-109">Or -</span></span>
    
- <span data-ttu-id="cbcdf-110">Escribir texto sin comprimir en la propiedad **PR_RTF_COMPRESSED**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="cbcdf-111">El procedimiento para establecer **PR_RTF_COMPRESSED** con texto sin comprimir es el mismo que para configurarlo con texto comprimido, con una excepción.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="cbcdf-112">Al llamar a [WrapCompressedRTFStream](wrapcompressedrtfstream.md), establezca la marca STORE_UNCOMPRESSED_RTF en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="cbcdf-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="cbcdf-113">La configuración del texto sin comprimir tiene el inconveniente de que aumenta el tamaño de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

