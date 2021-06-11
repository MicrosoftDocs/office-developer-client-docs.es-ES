---
title: Ordenar tablas después de establecer columnas y restricciones
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
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="0a075-103">Ordenar tablas después de establecer columnas y restricciones</span><span class="sxs-lookup"><span data-stu-id="0a075-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="0a075-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a075-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a075-105">Cuando necesite limitar la vista de una tabla ordenada, realice siempre las siguientes llamadas **IMAPITable** en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="0a075-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="0a075-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="0a075-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="0a075-107">[IMAPITable::Restrict para](imapitable-restrict.md) imponer la restricción.</span><span class="sxs-lookup"><span data-stu-id="0a075-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="0a075-108">[IMAPITable::SortTable](imapitable-sorttable.md) para realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="0a075-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="0a075-109">Si la tabla ordenada está categorizada, realice una llamada a [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), si es necesario, después de la **llamada SortTable.**</span><span class="sxs-lookup"><span data-stu-id="0a075-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="0a075-110">Este orden de llamadas es importante porque la mayoría de los proveedores de servicios ordenan una tabla como la última tarea para lograr el mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0a075-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="0a075-111">Si, por ejemplo, un proveedor de almacén de mensajes debe clasificar una tabla de contenido de carpeta antes de que se pueda imponer una restricción, esta categorización se quitará durante el procesamiento de la restricción.</span><span class="sxs-lookup"><span data-stu-id="0a075-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="0a075-112">Será necesaria una segunda categorización.</span><span class="sxs-lookup"><span data-stu-id="0a075-112">A second categorization will be necessary.</span></span> 
  

