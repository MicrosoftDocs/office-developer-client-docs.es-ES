---
title: Crear un asunto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332966"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="d0aa8-103">Crear un asunto del mensaje</span><span class="sxs-lookup"><span data-stu-id="d0aa8-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="d0aa8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0aa8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0aa8-105">El asunto de un mensaje, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), es una propiedad opcional que se usa para resumir la intención de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d0aa8-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="d0aa8-106">Si decide establecerla, puede convertirla en una cadena de caracteres de 128 bytes como máximo.</span><span class="sxs-lookup"><span data-stu-id="d0aa8-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="d0aa8-107">El límite de bytes 128 no es un límite impuesto por MAPI; se trata de un límite impuesto por algunos proveedores de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d0aa8-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="d0aa8-108">Para garantizar la interoperabilidad con los proveedores que la imponen, limite los asuntos a 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="d0aa8-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="d0aa8-109">Tenga en cuenta que algunos proveedores de almacenamiento de mensajes no permiten escribir **PR_SUBJECT** en un objeto Stream con la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d0aa8-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="d0aa8-110">No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Esta propiedad se establece sólo en las respuestas y los mensajes reenviados.</span><span class="sxs-lookup"><span data-stu-id="d0aa8-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

