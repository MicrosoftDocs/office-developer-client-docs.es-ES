---
title: Ordenar tablas después de establecer restricciones y columnas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820742"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Ordenar tablas después de establecer restricciones y columnas

  
  
**Hace referencia a**: Outlook 
  
Cuando se necesita limitar la vista de una tabla ordenada, siempre realizar las llamadas de **IMAPITable** siguientes en el orden siguiente: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) para definir el conjunto de columnas. 
    
2. [IMAPITable:: Restrict](imapitable-restrict.md) a fin de aplicar la restricción. 
    
3. [SortTable](imapitable-sorttable.md) para llevar a cabo a la ordenación. 
    
Si la tabla ordenada se clasifica por categorías, realice una llamada a [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), si es necesario, después de la llamada **SortTable** . En este orden de las llamadas es importante porque la mayoría de los proveedores de servicio ordena una tabla como la última tarea para lograr el mejor rendimiento. Si, por ejemplo, un proveedor de almacén de mensajes debe clasificar una tabla de contenido de la carpeta antes de que se puede imponer una restricción, se quitará este categorización durante el procesamiento de la restricción. Una segunda categorización será necesaria. 
  

