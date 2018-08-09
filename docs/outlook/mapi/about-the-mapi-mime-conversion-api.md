---
title: Información sobre la API de conversión de MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816362"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="af1b7-103">Información sobre la API de conversión de MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="af1b7-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="af1b7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af1b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af1b7-105">La API de conversión de MIME a MAPI permite a los proveedores de correo convertir entre los mensajes MAPI y objetos MIME.</span><span class="sxs-lookup"><span data-stu-id="af1b7-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="af1b7-106">Proporciona definiciones de constantes, los identificadores de clase y los identificadores de interfaz tal como se muestra en [Las constantes de MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="af1b7-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="af1b7-107">Proveedores de correo deben cocreate una instancia de **[IConverterSession](iconvertersessioniunknown.md)** mediante una llamada a la función **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="af1b7-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

