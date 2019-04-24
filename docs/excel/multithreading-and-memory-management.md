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
# <a name="multithreading-and-memory-management"></a>Multiproceso y administración de memoria

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
El control adecuado de la memoria es fundamental para crear complementos XLL fiables para Microsoft Excel. No se pueden asignar los búferes de memoria apropiados y liberarlos cuando ya no son necesarios reduce el rendimiento, crea contención de recursos y desestabiliza Excel.
  
A partir de Microsoft Office Excel 2007, puede configurar Excel para usar hasta 1.024 subprocesos simultáneos al actualizar. En algunos casos, especialmente cuando hay varios procesadores disponibles o con funciones definidas por el usuario que se ejecutan en servidores agrupados, el subprocesamiento múltiple puede mejorar el rendimiento.
  
En los siguientes temas se describe cómo administrar la memoria y los subprocesos en los XLL:
  
- [Administración de memoria en Excel](memory-management-in-excel.md)
    
- [Multiproceso y conflictos de memoria en Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Vea también



[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

