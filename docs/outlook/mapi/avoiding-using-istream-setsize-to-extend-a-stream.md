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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331643"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="6de22-103">Evitar el uso de IStream:: setSize para extender una secuencia</span><span class="sxs-lookup"><span data-stu-id="6de22-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="6de22-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6de22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6de22-105">Al escribir en secuencias, a veces es necesario agrandarlas porque su tamaño inicial ya no es suficiente.</span><span class="sxs-lookup"><span data-stu-id="6de22-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="6de22-106">Use el método OLE **IStream:: Write** para lograr esto en lugar de **IStream:: setSize**.</span><span class="sxs-lookup"><span data-stu-id="6de22-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="6de22-107">**IStream:: Write** amplía automáticamente la secuencia, lo que hace que \* \* IStream:: setSize \* \* no sea necesario.</span><span class="sxs-lookup"><span data-stu-id="6de22-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="6de22-108">Llamar a **IStream:: Write** sin **IStream:: setSize** puede ser hasta tres veces más rápido que realizar la llamada **setSize** antes de **escribir**.</span><span class="sxs-lookup"><span data-stu-id="6de22-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

