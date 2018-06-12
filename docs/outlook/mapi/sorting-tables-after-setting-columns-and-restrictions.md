---
title: Ordenación de tablas después de establecer las columnas y restricciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820742"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="aafb6-103">Ordenación de tablas después de establecer las columnas y restricciones</span><span class="sxs-lookup"><span data-stu-id="aafb6-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="aafb6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aafb6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aafb6-105">Cuando se necesita limitar la vista de una tabla ordenada, siempre realizar las llamadas de **IMAPITable** siguientes en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="aafb6-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="aafb6-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="aafb6-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="aafb6-107">[IMAPITable:: Restrict](imapitable-restrict.md) a fin de aplicar la restricción.</span><span class="sxs-lookup"><span data-stu-id="aafb6-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="aafb6-108">[SortTable](imapitable-sorttable.md) para llevar a cabo a la ordenación.</span><span class="sxs-lookup"><span data-stu-id="aafb6-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="aafb6-109">Si la tabla ordenada se clasifica por categorías, realice una llamada a [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), si es necesario, después de la llamada **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="aafb6-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="aafb6-110">En este orden de las llamadas es importante porque la mayoría de los proveedores de servicio ordena una tabla como la última tarea para lograr el mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="aafb6-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="aafb6-111">Si, por ejemplo, un proveedor de almacén de mensajes debe clasificar una tabla de contenido de la carpeta antes de que se puede imponer una restricción, se quitará este categorización durante el procesamiento de la restricción.</span><span class="sxs-lookup"><span data-stu-id="aafb6-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="aafb6-112">Una segunda categorización será necesaria.</span><span class="sxs-lookup"><span data-stu-id="aafb6-112">A second categorization will be necessary.</span></span> 
  

