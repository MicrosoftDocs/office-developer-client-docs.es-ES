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
# <a name="multithreading-and-memory-management"></a>Multithreading y administración de memoria

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Un control adecuado de la memoria es fundamental para crear complementos XLL confiables para Microsoft Excel. Si no se asignan búferes de memoria adecuados y se liberan cuando ya no son necesarios, se reduce el rendimiento, se crea contención de recursos y se desestabiliza Excel.
  
A partir Microsoft Office Excel 2007, puede configurar Excel para que use hasta 1.024 subprocesos simultáneos al recalcular. En algunos casos, especialmente cuando hay varios procesadores disponibles o con funciones definidas por el usuario que se ejecutan en servidores en clúster, el multithreading puede mejorar el rendimiento.
  
En los siguientes temas se describe cómo administrar la memoria y los subprocesos en XLL:
  
- [Administración de memoria en Excel](memory-management-in-excel.md)
    
- [Multiproceso y conflictos de memoria en Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Consulte también



[Desarrollar archivos XLL de Excel](developing-excel-xlls.md)

