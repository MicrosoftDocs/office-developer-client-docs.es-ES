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
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816503"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="c7e81-103">Evite usar IStream::SetSize para extender una secuencia</span><span class="sxs-lookup"><span data-stu-id="c7e81-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="c7e81-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7e81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7e81-105">Al escribir en secuencias, en ocasiones, es necesario ampliar ellos porque su tamaño inicial ya no es suficiente.</span><span class="sxs-lookup"><span data-stu-id="c7e81-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="c7e81-106">Usar el método OLE **IStream::Write** para hacerlo en lugar de **IStream:: SetSize**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="c7e81-107">**IStream::Write** extiende automáticamente la secuencia, realizar ** IStream:: SetSize ** innecesarios.</span><span class="sxs-lookup"><span data-stu-id="c7e81-107">**IStream::Write** automatically extends the stream, making ** IStream::SetSize ** unnecessary.</span></span> <span data-ttu-id="c7e81-108">Al llamar a **IStream::Write** sin **IStream:: SetSize** puede ser más rápido que hacer el **SetSize** llamada antes de **escribir**hasta tres veces.</span><span class="sxs-lookup"><span data-stu-id="c7e81-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

