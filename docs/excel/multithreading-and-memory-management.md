---
title: Multiproceso y administración de la memoria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815685"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="acebe-103">Multiproceso y administración de la memoria</span><span class="sxs-lookup"><span data-stu-id="acebe-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="acebe-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="acebe-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="acebe-105">Tratamiento adecuado de memoria es esencial para crear complementos XLL confiables para Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="acebe-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="acebe-106">Error al asignar los búferes de memoria apropiado y liberarlos cuando ya no sean necesarios reduce el rendimiento, crea la contención de recursos y desetabilice Excel.</span><span class="sxs-lookup"><span data-stu-id="acebe-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="acebe-107">A partir de Microsoft Office Excel 2007, puede configurar Excel para usar hasta 1.024 subprocesos simultáneos al volver a calcular.</span><span class="sxs-lookup"><span data-stu-id="acebe-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="acebe-108">En algunos casos, especialmente cuando existen varios procesadores o con definidas por el usuario que se ejecuta en servidores agrupados en clúster, subprocesamiento múltiple de funciones pueden mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="acebe-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="acebe-109">Los siguientes temas describen cómo administrar la memoria y subprocesos en XLL:</span><span class="sxs-lookup"><span data-stu-id="acebe-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="acebe-110">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="acebe-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="acebe-111">Multiproceso y conflictos de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="acebe-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="acebe-112">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="acebe-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="acebe-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="acebe-113">See also</span></span>



[<span data-ttu-id="acebe-114">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="acebe-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

