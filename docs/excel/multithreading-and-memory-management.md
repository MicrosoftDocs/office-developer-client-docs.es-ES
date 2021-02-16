---
title: Multithreading y administración de memoria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414469"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="16aa8-103">Multithreading y administración de memoria</span><span class="sxs-lookup"><span data-stu-id="16aa8-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="16aa8-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="16aa8-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="16aa8-105">Un control adecuado de la memoria es fundamental para crear complementos XLL confiables para Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="16aa8-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="16aa8-106">Si no se asignan búferes de memoria adecuados y se liberan cuando ya no son necesarios, se reduce el rendimiento, se crea contención de recursos y se desestabiliza Excel.</span><span class="sxs-lookup"><span data-stu-id="16aa8-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="16aa8-107">A partir Microsoft Office Excel 2007, puede configurar Excel para que use hasta 1.024 subprocesos simultáneos al recalcular.</span><span class="sxs-lookup"><span data-stu-id="16aa8-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="16aa8-108">En algunos casos, especialmente cuando hay varios procesadores disponibles o con funciones definidas por el usuario que se ejecutan en servidores en clúster, el multithreading puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="16aa8-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="16aa8-109">En los siguientes temas se describe cómo administrar la memoria y los subprocesos en XLL:</span><span class="sxs-lookup"><span data-stu-id="16aa8-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="16aa8-110">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="16aa8-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="16aa8-111">Multiproceso y conflictos de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="16aa8-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="16aa8-112">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="16aa8-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="16aa8-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="16aa8-113">See also</span></span>



[<span data-ttu-id="16aa8-114">Desarrollar archivos XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="16aa8-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

