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
# <a name="multithreading-and-memory-management"></a>Multiproceso y administración de la memoria

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Tratamiento adecuado de memoria es esencial para crear complementos XLL confiables para Microsoft Excel. Error al asignar los búferes de memoria apropiado y liberarlos cuando ya no sean necesarios reduce el rendimiento, crea la contención de recursos y desetabilice Excel.
  
A partir de Microsoft Office Excel 2007, puede configurar Excel para usar hasta 1.024 subprocesos simultáneos al volver a calcular. En algunos casos, especialmente cuando existen varios procesadores o con definidas por el usuario que se ejecuta en servidores agrupados en clúster, subprocesamiento múltiple de funciones pueden mejorar el rendimiento.
  
Los siguientes temas describen cómo administrar la memoria y subprocesos en XLL:
  
- [Administración de memoria en Excel](memory-management-in-excel.md)
    
- [Multiproceso y conflictos de memoria en Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Vea también



[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

