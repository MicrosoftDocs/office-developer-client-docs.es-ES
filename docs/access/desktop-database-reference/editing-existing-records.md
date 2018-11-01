---
title: Editar registros existentes
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c500f89b0f16062e43ace45f55eab9a593d071a2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884236"
---
# <a name="editing-existing-records"></a><span data-ttu-id="ba1d2-102">Editar registros existentes</span><span class="sxs-lookup"><span data-stu-id="ba1d2-102">Editing Existing Records</span></span>


<span data-ttu-id="ba1d2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba1d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba1d2-p101">Para editar registros existentes, vaya a la fila que desea modificar y cambie la propiedad **Valor** de los campos que desea cambiar. Para obtener más información sobre la propiedad **Valor** del objeto **Field**, vea el [Capítulo 3: Examinar datos](chapter-3-examining-data.md). Dependiendo del tipo de cursor, se utilizará **Update** o **UpdateBatch** para enviar los cambios de vuelta al origen de datos. Para obtener más información, vea el [Capítulo 5: Actualizar y almacenar datos.](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="ba1d2-p101">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change. For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md). Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source. For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="ba1d2-p102">Normalmente es más eficaz utilizar un procedimiento almacenado con un objeto de comando para realizar actualizaciones, así como para realizar otras operaciones, ya que un procedimiento almacenado no requiere la creación de un cursor. Para obtener más información acerca de cursores, vea el [Capítulo 8: Cursores y bloqueos](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="ba1d2-p102">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor. For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

