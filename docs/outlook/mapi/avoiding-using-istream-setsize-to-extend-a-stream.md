---
title: Evitar el uso de IStreamSetSize para extender una secuencia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428917"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="f53b8-103">Evitar el uso de IStream::SetSize para extender una secuencia</span><span class="sxs-lookup"><span data-stu-id="f53b8-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="f53b8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f53b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f53b8-105">Al escribir en secuencias, a veces es necesario ampliarlas porque su tamaño inicial ya no es suficiente.</span><span class="sxs-lookup"><span data-stu-id="f53b8-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="f53b8-106">Use el método OLE **IStream::Write** para lograr esto en lugar de **IStream::SetSize**.</span><span class="sxs-lookup"><span data-stu-id="f53b8-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="f53b8-107">**IStream::Write** amplía automáticamente la secuencia, lo que hace que \*\* IStream::SetSize \*\* no es necesario.</span><span class="sxs-lookup"><span data-stu-id="f53b8-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="f53b8-108">Llamar **a IStream::Write** sin **IStream::SetSize** puede ser hasta tres veces más rápido que realizar la llamada **SetSize** antes de **Escribir**.</span><span class="sxs-lookup"><span data-stu-id="f53b8-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

