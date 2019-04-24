---
title: 'Capítulo 5: Actualización y persistencia de datos'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18dd63acd733624fba522ee7382f305d34019905
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296433"
---
# <a name="chapter-5-updating-and-persisting-data"></a><span data-ttu-id="b310a-102">Capítulo 5: Actualización y persistencia de datos</span><span class="sxs-lookup"><span data-stu-id="b310a-102">Chapter 5: Updating and persisting data</span></span>

<span data-ttu-id="b310a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b310a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b310a-p101">En capítulos anteriores, se explicó cómo usar ADO para obtener datos de un origen de datos, cómo desplazarse por ellos y cómo modificarlos. Por supuesto, si un objetivo de la aplicación es permitir que los usuarios realicen cambios en los datos, deberá saber cómo guardar esos cambios. Puede hacer que los cambios realizados en un **Recordset** se conserven en un archivo mediante el método **Save**, o bien, puede enviar los cambios de vuelta al origen de datos para su almacenamiento mediante los métodos **Update** o **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="b310a-p101">The preceding chapters have discussed how to use ADO to get to data in a data source, how to move around in the data, and even how to edit the data. Of course, if the goal of your application is to allow users to make changes to the data, you will need to understand how to save those changes. You can either persist the **Recordset** changes to a file using the **Save** method, or you can send the changes back to the data source for storage using the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="b310a-p102">En los capítulos anteriores, se cambiaron datos en varias filas de un **Recordset**. ADO admite dos nociones básicas relacionadas con la adición, la eliminación y la modificación de filas de datos.</span><span class="sxs-lookup"><span data-stu-id="b310a-p102">In the preceding chapters, you changed the data in several rows of the **Recordset**. ADO supports two basic notions relating to the addition, deletion, and modification of rows of data.</span></span>

<span data-ttu-id="b310a-p103">La primera noción es que los cambios no se implementan inmediatamente en el **Recordset**; en vez de ello, se realizan en un *búfer de copia* interno. Si no desea conservarlos, se descartan en el búfer de copia. Por el contrario, si decide conservarlos, se aplicarán desde el búfer de copia al **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b310a-p103">The first notion is that changes aren't immediately made to the **Recordset**; instead, they are made to an internal *copy buffer*. If you decide you don't want the changes, the modifications in the copy buffer are discarded. If you decide to keep the changes, the changes in the copy buffer are applied to the **Recordset**.</span></span>

<span data-ttu-id="b310a-p104">La segunda noción es que los cambios se propagan al origen de datos en cuanto se declara el trabajo completado en una fila (modo *inmediato*), o que todos los cambios en un conjunto de filas se recopilan hasta que el trabajo para el conjunto completo se declara finalizado (modo *proceso por lotes*). La propiedad **LockType** determina cuándo se realizan los cambios en el origen de datos subyacente. **adLockOptimistic** o **adLockPessimistic** especifican el modo inmediato, mientras que **adLockBatchOptimistic** especifica el modo de proceso por lotes. La propiedad **CursorLocation** puede determinar qué configuraciones de **LockType** están disponibles. Por ejemplo, el valor **adLockPessimistic** no se admite si la propiedad **CursorLocation** se establece en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="b310a-p104">The second notion is that changes are either propagated to the data source as soon as you declare the work on a row complete (that is, *immediate* mode), or all changes to a set of rows are collected until you declare the work for the set complete (that is, *batch* mode). The **LockType** property determines when the changes are made to the underlying data source. **adLockOptimistic** or **adLockPessimistic** specifies immediate mode, while **adLockBatchOptimistic** specifies batch mode. The **CursorLocation** property can affect which **LockType** settings are available. For instance, the **adLockPessimistic** setting is not supported if the **CursorLocation** property is set to **adUseClient**.</span></span>

<span data-ttu-id="b310a-p105">En el modo inmediato, cada llamada al método **Update** propaga los cambios al origen de datos. En el modo de proceso por lotes, cada llamada a **Update** o movimiento de la posición actual de fila guarda los cambios en el búfer de copia, pero sólo el método **UpdateBatch** propaga los cambios al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="b310a-p105">In immediate mode, each invocation of the **Update** method propagates the changes to the data source. In batch mode, each invocation of **Update** or movement of the current row position saves the changes to the copy buffer, but only the **UpdateBatch** method propagates the changes to the data source.</span></span>

<span data-ttu-id="b310a-119">En este capítulo, se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b310a-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="b310a-120">Actualización de datos (ADO)</span><span class="sxs-lookup"><span data-stu-id="b310a-120">Updating data (ADO)</span></span>](updating-data.md)
- [<span data-ttu-id="b310a-121">Almacenar datos (ADO)</span><span class="sxs-lookup"><span data-stu-id="b310a-121">Persisting data (ADO)</span></span>](persisting-data.md)
