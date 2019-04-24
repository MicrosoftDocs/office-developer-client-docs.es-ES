---
title: Multiproceso y administración de memoria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310391"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="ee144-103">Multiproceso y administración de memoria</span><span class="sxs-lookup"><span data-stu-id="ee144-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="ee144-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ee144-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ee144-105">El control adecuado de la memoria es fundamental para crear complementos XLL fiables para Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ee144-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="ee144-106">No se pueden asignar los búferes de memoria apropiados y liberarlos cuando ya no son necesarios reduce el rendimiento, crea contención de recursos y desestabiliza Excel.</span><span class="sxs-lookup"><span data-stu-id="ee144-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="ee144-107">A partir de Microsoft Office Excel 2007, puede configurar Excel para usar hasta 1.024 subprocesos simultáneos al actualizar.</span><span class="sxs-lookup"><span data-stu-id="ee144-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="ee144-108">En algunos casos, especialmente cuando hay varios procesadores disponibles o con funciones definidas por el usuario que se ejecutan en servidores agrupados, el subprocesamiento múltiple puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ee144-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="ee144-109">En los siguientes temas se describe cómo administrar la memoria y los subprocesos en los XLL:</span><span class="sxs-lookup"><span data-stu-id="ee144-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="ee144-110">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="ee144-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="ee144-111">Multiproceso y conflictos de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="ee144-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="ee144-112">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="ee144-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="ee144-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee144-113">See also</span></span>



[<span data-ttu-id="ee144-114">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="ee144-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

