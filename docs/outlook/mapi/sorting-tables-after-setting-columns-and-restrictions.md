---
title: Ordenar tablas después de establecer las columnas y restricciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409884"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Ordenar tablas después de establecer las columnas y restricciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando necesite limitar la vista de una tabla ordenada, realice siempre las siguientes llamadas al **IMAPITable** en el orden siguiente: 
  
1. [IMAPITable:: SetColumns](imapitable-setcolumns.md) para definir el conjunto de columnas. 
    
2. [IMAPITable:: Restrict](imapitable-restrict.md) para imponer la restricción. 
    
3. [IMAPITable:: SortTable](imapitable-sorttable.md) para realizar la ordenación. 
    
Si la tabla ordenada tiene categorías, realice una llamada a [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md), si es necesario, después de la llamada a **SortTable** . Esta ordenación de llamadas es importante porque la mayoría de los proveedores de servicios ordenan una tabla como la última tarea para obtener el mejor rendimiento. Si, por ejemplo, un proveedor de almacén de mensajes debe clasificar una tabla de contenido de carpeta antes de que se pueda imponer una restricción, esta categorización se quitará durante el procesamiento de la restricción. Se necesitará una segunda categorización. 
  

