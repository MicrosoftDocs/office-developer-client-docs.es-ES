---
title: Información sobre la API de conversión de MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575269"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="f0b0b-103">Información sobre la API de conversión de MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="f0b0b-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="f0b0b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0b0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0b0b-105">La API de conversión de MIME a MAPI permite a los proveedores de correo convertir entre los mensajes MAPI y objetos MIME.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="f0b0b-106">Proporciona definiciones de constantes, los identificadores de clase y los identificadores de interfaz tal como se muestra en [Las constantes de MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f0b0b-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="f0b0b-107">Proveedores de correo deben cocreate una instancia de **[IConverterSession](iconvertersessioniunknown.md)** mediante una llamada a la función **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="f0b0b-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

