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
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816626"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="0bd94-103">Crear un asunto del mensaje</span><span class="sxs-lookup"><span data-stu-id="0bd94-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="0bd94-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bd94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0bd94-105">El asunto de un mensaje, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), es una propiedad opcional, que se usa para resumir la intención de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0bd94-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="0bd94-106">Si decide establecer, convertirla en una cadena de caracteres 128 bytes o menos.</span><span class="sxs-lookup"><span data-stu-id="0bd94-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="0bd94-107">El límite de 128 bytes no es un límite impuesto por MAPI; es un límite impuesto por algunos proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0bd94-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="0bd94-108">Para asegurar la interoperabilidad con los proveedores que se imponen, limitar sujetos a 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="0bd94-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="0bd94-109">Tenga en cuenta que algunos proveedores de almacén de mensajes no permitir **PR_SUBJECT** se escriban en un objeto stream con la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0bd94-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="0bd94-110">No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Esta propiedad se establezca sólo en las respuestas y los mensajes reenviada.</span><span class="sxs-lookup"><span data-stu-id="0bd94-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

